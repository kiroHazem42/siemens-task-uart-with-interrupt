################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := seimns task uart using interrupt by putty
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
seimns\ task\ uart\ using\ interrupt\ by\ putty.elf \

MAP_FILES += \
seimns\ task\ uart\ using\ interrupt\ by\ putty.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
seimns\ task\ uart\ using\ interrupt\ by\ putty.list \

OBJCOPY_HEX += \
seimns\ task\ uart\ using\ interrupt\ by\ putty.hex \


# All Target
all: main-build

# Main-build Target
main-build: seimns\ task\ uart\ using\ interrupt\ by\ putty.elf secondary-outputs

# Tool invocations
seimns\ task\ uart\ using\ interrupt\ by\ putty.elf seimns\ task\ uart\ using\ interrupt\ by\ putty.map: $(OBJS) $(USER_OBJS) C:\Users\victus\STM32CubeIDE\workspace_1.12.1\seimns\ task\ uart\ using\ interrupt\ by\ putty\STM32F103C8TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "seimns task uart using interrupt by putty.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\victus\STM32CubeIDE\workspace_1.12.1\seimns task uart using interrupt by putty\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="seimns task uart using interrupt by putty.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

seimns\ task\ uart\ using\ interrupt\ by\ putty.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "seimns task uart using interrupt by putty.list"
	@echo 'Finished building: $@'
	@echo ' '

seimns\ task\ uart\ using\ interrupt\ by\ putty.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "seimns task uart using interrupt by putty.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) default.size.stdout seimns\ task\ uart\ using\ interrupt\ by\ putty.elf seimns\ task\ uart\ using\ interrupt\ by\ putty.hex seimns\ task\ uart\ using\ interrupt\ by\ putty.list seimns\ task\ uart\ using\ interrupt\ by\ putty.map seimns\\ task\\ uart\\ using\\ interrupt\\ by\\ putty.elf
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
