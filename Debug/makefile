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
projekat_2.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
projekat_2.list \

OBJCOPY_HEX += \
projekat_2.hex \

OBJCOPY_BIN += \
projekat_2.bin \


# All Target
all: projekat_2.elf secondary-outputs

# Tool invocations
projekat_2.elf: $(OBJS) $(USER_OBJS) D:\4.\ godina\Prvi\ semestar\Mikroprocesorski\ sistemi\moji_cube_ide\projekat_2\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "projekat_2.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\4. godina\Prvi semestar\Mikroprocesorski sistemi\moji_cube_ide\projekat_2\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="projekat_2.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

projekat_2.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "projekat_2.list"
	@echo 'Finished building: $@'
	@echo ' '

projekat_2.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "projekat_2.hex"
	@echo 'Finished building: $@'
	@echo ' '

projekat_2.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "projekat_2.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
