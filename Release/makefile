################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/usart_lib/subdir.mk
-include src/syscalls/subdir.mk
-include src/kiss/src/subdir.mk
-include src/hal/Src/subdir.mk
-include src/cmsis_boot/startup/subdir.mk
-include src/cmsis_boot/subdir.mk
-include src/SFU/subdir.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
SECONDARY_FLASH += \
Boot_STM32H743_SFU_fast_uart.bin \

SECONDARY_LIST += \
Boot_STM32H743_SFU_fast_uart.lst \

SECONDARY_SIZE += \
Boot_STM32H743_SFU_fast_uart.siz \


# All Target
all: Boot_STM32H743_SFU_fast_uart.elf secondary-outputs

# Tool invocations
Boot_STM32H743_SFU_fast_uart.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: Cross ARM C++ Linker'
	arm-none-eabi-g++ -mthumb -mfloat-abi=hard -mfpu=fpv5-d16 -mcpu=cortex-m7 -O3 -fmessage-length=0 -ffunction-sections -fdata-sections -ffreestanding -fno-builtin -Wunused -Wuninitialized -Wall -Wextra -Wpointer-arith -Wshadow -Wlogical-op -Waggregate-return -Wfloat-equal -Wno-sign-compare -T "D:\Projects\Boot_STM32H743_SFU_fast_uart\ldscripts\STM32H743XIHx_FLASH_RAM_D1.ld" -nostartfiles -Xlinker --gc-sections -Wl,-Map,"Boot_STM32H743_SFU_fast_uart.map" --specs=nano.specs -o "Boot_STM32H743_SFU_fast_uart.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

Boot_STM32H743_SFU_fast_uart.bin: Boot_STM32H743_SFU_fast_uart.elf
	@echo 'Invoking: Cross ARM GNU Create Flash Image'
	arm-none-eabi-objcopy -O binary "Boot_STM32H743_SFU_fast_uart.elf"  "Boot_STM32H743_SFU_fast_uart.bin"
	@echo 'Finished building: $@'
	@echo ' '

Boot_STM32H743_SFU_fast_uart.lst: Boot_STM32H743_SFU_fast_uart.elf
	@echo 'Invoking: Cross ARM GNU Create Listing'
	arm-none-eabi-objdump --demangle --disassemble --wide "Boot_STM32H743_SFU_fast_uart.elf" > "Boot_STM32H743_SFU_fast_uart.lst"
	@echo 'Finished building: $@'
	@echo ' '

Boot_STM32H743_SFU_fast_uart.siz: Boot_STM32H743_SFU_fast_uart.elf
	@echo 'Invoking: Cross ARM GNU Print Size'
	arm-none-eabi-size --format=berkeley "Boot_STM32H743_SFU_fast_uart.elf"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(CC_DEPS)$(C++_DEPS)$(OBJS)$(C_UPPER_DEPS)$(CXX_DEPS)$(SECONDARY_FLASH)$(SECONDARY_LIST)$(SECONDARY_SIZE)$(ASM_DEPS)$(S_UPPER_DEPS)$(C_DEPS)$(CPP_DEPS) Boot_STM32H743_SFU_fast_uart.elf
	-@echo ' '

secondary-outputs: $(SECONDARY_FLASH) $(SECONDARY_LIST) $(SECONDARY_SIZE)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
