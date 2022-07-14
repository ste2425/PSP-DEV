PSPSDK=$(shell psp-config --pspsdk-path)
PSPDIR=$(shell psp-config --psp-prefix)

TARGET = controller_basic
OBJS = src/main.o

INCDIR   := $(INCDIR) . src

# Flags:
CFLAGS = -O2 -G0 -Wall -g -DSAMPLE_CONFIG_PLATFORM_PSP
CXXFLAGS = $(CFLAGS) -fno-exceptions -fno-rtti
ASFLAGS = $(CFLAGS)

LIBDIR =
# = -lpspgum_vfpu -lpspvfpu -lpspgu -lm
LDFLAGS =

EXTRA_TARGETS = EBOOT.PBP
PSP_EBOOT_TITLE = Basic controller sample

include $(PSPSDK)/lib/build.mak