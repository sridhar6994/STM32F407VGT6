################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (12.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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


BUILD_ARTIFACT_NAME := PWM_DC_Motor_SPeed_Control
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
PWM_DC_Motor_SPeed_Control.elf \

MAP_FILES += \
PWM_DC_Motor_SPeed_Control.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
PWM_DC_Motor_SPeed_Control.list \

OBJCOPY_HEX += \
PWM_DC_Motor_SPeed_Control.hex \

OBJCOPY_BIN += \
PWM_DC_Motor_SPeed_Control.bin \


# All Target
all: main-build

# Main-build Target
main-build: PWM_DC_Motor_SPeed_Control.elf secondary-outputs

# Tool invocations
PWM_DC_Motor_SPeed_Control.elf PWM_DC_Motor_SPeed_Control.map: $(OBJS) $(USER_OBJS) D:\Project\STM32_PROJECT\PWM_DC_Motor_Speed_Control\PWM_DC_Motor_SPeed_Control\STM32F407VGTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "PWM_DC_Motor_SPeed_Control.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Project\STM32_PROJECT\PWM_DC_Motor_Speed_Control\PWM_DC_Motor_SPeed_Control\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="PWM_DC_Motor_SPeed_Control.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

PWM_DC_Motor_SPeed_Control.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "PWM_DC_Motor_SPeed_Control.list"
	@echo 'Finished building: $@'
	@echo ' '

PWM_DC_Motor_SPeed_Control.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "PWM_DC_Motor_SPeed_Control.hex"
	@echo 'Finished building: $@'
	@echo ' '

PWM_DC_Motor_SPeed_Control.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "PWM_DC_Motor_SPeed_Control.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) PWM_DC_Motor_SPeed_Control.bin PWM_DC_Motor_SPeed_Control.elf PWM_DC_Motor_SPeed_Control.hex PWM_DC_Motor_SPeed_Control.list PWM_DC_Motor_SPeed_Control.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
