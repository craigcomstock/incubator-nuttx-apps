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
MAINSRC = core/cf-agent/cf-agent.c

include $(APPDIR)/Application.mk

