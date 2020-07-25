################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM4F/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
prj1_YaoWangze.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
prj1_YaoWangze.list \

OBJCOPY_BIN += \
prj1_YaoWangze.bin \


# All Target
all: prj1_YaoWangze.elf secondary-outputs

# Tool invocations
prj1_YaoWangze.elf: $(OBJS) $(USER_OBJS) D:\no_chinese_language\Embbed\prj1_YaoWangze\STM32F429ZITX_FLASH.ld
	arm-none-eabi-gcc -o "prj1_YaoWangze.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\no_chinese_language\Embbed\prj1_YaoWangze\STM32F429ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="prj1_YaoWangze.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

prj1_YaoWangze.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "prj1_YaoWangze.list"
	@echo 'Finished building: $@'
	@echo ' '

prj1_YaoWangze.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "prj1_YaoWangze.bin"
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
