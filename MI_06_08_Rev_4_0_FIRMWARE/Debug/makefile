################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32G0xx_HAL_Driver/Src/subdir.mk
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
MI_06_08.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
MI_06_08.list \

OBJCOPY_BIN += \
MI_06_08.bin \


# All Target
all: MI_06_08.elf secondary-outputs

# Tool invocations
MI_06_08.elf: $(OBJS) $(USER_OBJS) D:\WORK\AutoSignal\MI_06_MCU\MI_04-08\MI_06_08_Rev_4_0_FIRMWARE\STM32G030J6MX_FLASH.ld
	arm-none-eabi-gcc -o "MI_06_08.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0plus -T"D:\WORK\AutoSignal\MI_06_MCU\MI_04-08\MI_06_08_Rev_4_0_FIRMWARE\STM32G030J6MX_FLASH.ld" --specs=nosys.specs -Wl,-Map="MI_06_08.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

MI_06_08.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "MI_06_08.list"
	@echo 'Finished building: $@'
	@echo ' '

MI_06_08.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "MI_06_08.bin"
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
