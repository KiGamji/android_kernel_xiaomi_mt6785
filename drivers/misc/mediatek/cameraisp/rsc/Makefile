#
# Copyright (C) 2015 MediaTek Inc.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 2 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#

MTK_PLATFORM := $(subst ",,$(CONFIG_MTK_PLATFORM))

ccflags-y += -I$(srctree)/drivers/misc/mediatek/m4u/$(MTK_PLATFORM)/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/mmp/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/cmdq/v3/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/cmdq/v3/$(MTK_PLATFORM)/
ccflags-y += -I$(srctree)/drivers/staging/android/ion \
             -I$(srctree)/drivers/staging/android/ion/mtk
ccflags-y += -I$(srctree)/drivers/misc/mediatek/smi/

ccflags-$(CONFIG_MTK_IOMMU_V2) += -I$(srctree)/drivers/iommu
ccflags-$(CONFIG_MTK_IOMMU_V2) += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/
ccflags-$(CONFIG_MTK_IOMMU_V2) += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(MTK_PLATFORM)/include/

obj-y += camera_rsc_dummy.o
obj-y += engine_request.o


ifeq ($(CONFIG_MACH_MT6785),y)
  obj-$(CONFIG_MTK_CAMERA_ISP_RSC_SUPPORT) += mt6785/camera_rsc.o
endif
