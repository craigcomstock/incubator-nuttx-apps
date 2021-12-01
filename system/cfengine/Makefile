include $(APPDIR)/Make.defs

PROGNAME = cfagent
PRIORITY = SCHED_PRIORITY_DEFAULT
STACKSIZE = 768

CFLAGS += -I core/cf-agent
CFLAGS += -I core/libcfnet
CFLAGS += -I core/cf-check
CFLAGS += -I core/libenv
CFLAGS += -I core/libntech/libutils
CFLAGS += -I core/libpromises
CFLAGS += -I core

CSRCS += $(wildcard core/libntech/libutils/*.c)
CSRCS += $(wildcard core/libntech/libtool/*.c)
CSRCS += $(wildcard core/libntech/misc/*.c)
LIBPROMISES_SRCS := $(wildcard core/libpromises/*.c)
LIBPROMISES_SKIP := core/libpromises/process_aix.c core/libpromises/process_hpux.c core/libpromises/process_linux.c core/libpromises/process_freebsd.c core/libpromises/process_solaris.c
CSRCS += $(filter-out $(LIBPROMISES_SKIP),$(LIBPROMISES_SRCS))
CSRCS += $(wildcard core/cf-net/*.c)
CFAGENT_SRCS := $(wildcard core/cf-agent/*.c)
CFAGENT_SKIP := core/cf-agent/load_avahi.c core/cf-agent/findhub.c core/cf-agent/verify_users_pam.c core/cf-agent/cf_sql.c
CSRCS += $(filter-out $(CFAGENT_SKIP),$(CFAGENT_SRCS))
#MAINSRC = core/cf-agent/cf-agent.c

include $(APPDIR)/Application.mk

