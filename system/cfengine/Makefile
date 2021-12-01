include $(APPDIR)/Make.defs

PROGNAME = cfagent
PRIORITY = SCHED_PRIORITY_DEFAULT
STACKSIZE = 768

CFLAGS += -I core/cf-agent
CFLAGS += -I core/libcfnet
CFLAGS += -I core/cf-check
CFLAGS += -I core/libntech/libutils
CFLAGS += -I core/libpromises
CFLAGS += -I core

CSRCS += $(wildcard core/libntech/libutils/*.c)
CSRCS += $(wildcard core/libntech/libtool/*.c)
CSRCS += $(wildcard core/libntech/misc/*.c)
LIBPROMISES_SRCS := $(wildcard core/libpromises/*.c)
SKIP=core/libpromises/process_aix.c core/libpromises/process_hpux.c core/libpromises/process_linux.c core/libpromises/process_freebsd.c core/libpromises/process_solaris.c
CSRCS += $(filter-out $(SKIP),$(LIBPROMISES_SRCS))
CSRCS += $(wildcard core/cf-net/*.c)
CSRCS += $(wildcard core/cf-agent/*.c)
#MAINSRC = core/cf-agent/cf-agent.c

include $(APPDIR)/Application.mk

