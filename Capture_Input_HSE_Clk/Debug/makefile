################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
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

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
capture_input_external_clk.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
capture_input_external_clk.list \

OBJCOPY_BIN += \
capture_input_external_clk.bin \


# All Target
all: capture_input_external_clk.elf secondary-outputs

# Tool invocations
capture_input_external_clk.elf: $(OBJS) $(USER_OBJS) D:\Aman\ Stuff\CUBE_IDE\STM32_Discovery_Board_Projects\Projects\Capture_Input_HSE_Clk\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "capture_input_external_clk.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Aman Stuff\CUBE_IDE\STM32_Discovery_Board_Projects\Projects\Capture_Input_HSE_Clk\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="capture_input_external_clk.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

capture_input_external_clk.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "capture_input_external_clk.list"
	@echo 'Finished building: $@'
	@echo ' '

capture_input_external_clk.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "capture_input_external_clk.bin"
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
