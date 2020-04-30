################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
can-sender.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
can-sender.list \

OBJCOPY_BIN += \
can-sender.bin \


# All Target
all: can-sender.elf secondary-outputs

# Tool invocations
can-sender.elf: $(OBJS) $(USER_OBJS) C:\Users\fao9ca\Documents\02\ -\ Start\ Stop\ Retrofit\ -\ Fase\ 3\03\ -\ Placa\ da\ cabine\STM32CubeIDE\workspace\can-sender\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "can-sender.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\fao9ca\Documents\02 - Start Stop Retrofit - Fase 3\03 - Placa da cabine\STM32CubeIDE\workspace\can-sender\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="can-sender.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

can-sender.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "can-sender.list"
	@echo 'Finished building: $@'
	@echo ' '

can-sender.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "can-sender.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
