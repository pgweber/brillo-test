# Main Makefile to cross compile client for Brillo Armulator

TARGET := client
OBJS := client.o
SRC := client.cc

SYSROOT := /Volumes/Linux/Source/brillo-master/prebuilts/ndk/r11/platforms/android-24/arch-arm/
GCC_PATH := /Volumes/Linux/Source/brillo-master/prebuilts/gcc/darwin-x86/arm/arm-linux-androideabi-4.9/bin/
CROSS_COMPILE := $(GCC_PATH)arm-linux-androideabi-

# Cross compile for ARM change this to point to different compilers as needed
CC := $(CROSS_COMPILE)g++
CFLAGS := -pie --sysroot=$(SYSROOT)
LIBS := 

all: $(TARGET)

$(TARGET): $(SRC)
	$(CC) $(CFLAGS) $(SRC) -o $@ $(LIBS)

clean:
	rm -f $(TARGET) $(OBJS)
