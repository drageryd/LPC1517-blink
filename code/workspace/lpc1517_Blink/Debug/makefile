################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: lpc1517_Blink.axf

# Tool invocations
lpc1517_Blink.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\Daniel\Desktop\lpc1517\LPC1517-blink\code\workspace\lpc_chip_15xx\Debug" -L"C:\Users\Daniel\Desktop\lpc1517\LPC1517-blink\code\workspace\CMSIS_DSPLIB_CM3\lib" -Xlinker -Map="lpc1517_Blink.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "lpc1517_Blink_Debug.ld" -o "lpc1517_Blink.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) lpc1517_Blink.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "lpc1517_Blink.axf" ; arm-none-eabi-objcopy -v -O binary "lpc1517_Blink.axf" "lpc1517_Blink.bin" ; checksum -p LPC1549 -d "lpc1517_Blink.bin" ; arm-none-eabi-objcopy -O ihex "lpc1517_Blink.axf" "lpc1517_Blink.hex" ;
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
