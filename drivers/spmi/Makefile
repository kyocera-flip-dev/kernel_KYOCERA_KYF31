#
# This software is contributed or developed by KYOCERA Corporation.
# (C) 2015 KYOCERA Corporation
#
# Makefile for kernel SPMI framework.
#
obj-$(CONFIG_SPMI)			+= spmi.o spmi-resources.o
obj-$(CONFIG_SPMI_MSM_PMIC_ARB)		+= spmi-pmic-arb.o
obj-$(CONFIG_MSM_QPNP_INT)		+= qpnp-int.o

ifdef CONFIG_DEBUG_FS
obj-$(CONFIG_SPMI)			+= spmi-dbgfs.o
endif

ifeq ($(KC_DEBUGTOOL_ENABLED_EXPORT), enable)
CFLAGS_qpnp-int.o += -DKC_BATTERY_LOG_ENABLED
endif
