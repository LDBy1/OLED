ifndef CC
CC = gcc
endif
ifndef LD
LD = ld
endif

SOURCES = SSD1306_OLED_Library/SSD1306_OLED.c Example_Code/Main.c Example_Code/example_app.c I2C_Library/I2C.c
OBJS := $(SOURCES:.c=.o)
CPPFLAGS := -I SSD1306_OLED_Library -I I2C_Library
ifndef CFLAGS
CFLAGS := -O2
endif

oled: $(OBJS)
	$(CC) $^ -o $@

clean:
	rm -rf oled $(OBJS)

compile: oled

install: compile
	mkdir -p $(DESTDIR)/usr/bin
	cp oled $(DESTDIR)/usr/bin/oled
