PROGRAM = Sonoff_S20_Button

EXTRA_COMPONENTS = \
	extras/http-parser \
	extras/dhcpserver \
    $(abspath ../../external_libs/wolfssl) \
    $(abspath ../../external_libs/cJSON) \
    $(abspath ../../external_libs/homekit) \
    $(abspath ../../libs/led_codes) \
    $(abspath ../../libs/legacy_config)

FLASH_SIZE = 8
FLASH_MODE = dout
FLASH_SPEED = 40
HOMEKIT_SPI_FLASH_BASE_ADDR = 0x7A000

EXTRA_CFLAGS += -I../.. -DHOMEKIT_SHORT_APPLE_UUIDS -DMDNS_RESPONDER_REPLY_SIZE=1500

include $(abspath ../../sdk/esp-open-rtos/common.mk)

monitor:
	$(FILTEROUTPUT) --port $(ESPPORT) --baud 115200 --elf $(PROGRAM_OUT)
