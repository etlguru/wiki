---
author: Peter Jonson
title: Archive Action
description: The Archive Action works with compressed files.
draft: false
tags: ['Package', 'Archive', 'zip', 'compression']
date: 2023-05-06
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

The Archive Action works with compressed files. It can be used to backup log files, as in the following example, although compression can be used when sending attachments via email when saving space on servers, and so on.

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/archive-action-1.png" title="Workflow tab" >}}

## Advanced tab

With the compression facility, you can compress items and decompress them as required. The location of the zip file and the files to compress are specified, as illustrated below:
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/archive-action-advanced-2.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/archive-action-variables.png" title="After execution tab" >}}

## Supported decompression formats

- Zip archive (_.zip;_.jar;_.ear;_.war;_.cbz;_.apk;_.wsz;_.wal;_.xpi;_.crx;_.dfsz;_.pcv;_.bsz;  
  _.mskin;_.wmz;_.ipa;_.docx;_.xlsx;_.pptx;_.sxw;_.sxi;_.sxt;_.sxd;_.sxc;_.sxm;_.sxg;_.stw;  
  _.sti;_.std;_.stc;_.odh;_.odd;_.odt;_.odm;_.ods;_.ots;_.odg;_.otg;_.odp;_.otp;_.odf;_.odb)
- BZip2 archive (_.bz2;_.bzip2;_.tbz2;_.tbz)
- Rar archive (_.rar;_.r00;\*.cbr)
- Arj archive (\*.arj)
- Z archive (_.z;_.taz)
- Lzh archive (_.lzh;_.lha)
- 7z archive (\*.7z)
- Cab archive (_.cab;_.fwp)
- Nsis archive (\*.nsis)
- Lzma archive (\*.lzma)
- Lzma86 archive (\*.lzma86)
- Pe archive (_.exe;_.dll;_.sys;_.bpl)
- Elf archive (\*.)
- Mach-O archive (\*.)
- Udf archive (_.iso;_.img)
- Xar archive (_.xar;_.safariextz)
- Mub archive (\*.)
- Hfs archive (\*.hfs)
- Dmg archive (\*.dmg)
- Compound archive (_.msi;_.msp;_.doc;_.xls;\*.ppt)
- Wim archive (_.wim;_.swm)
- Iso archive (_.iso;_.img)
- Chm archive (_.chm;_.chi;_.chq;_.chw;_.hxs;_.hxi;_.hxr;_.hxq;_.hxw;_.lit)
- Split archive (\*.001)
- Rpm archive (\*.rpm)
- Deb archive (\*.deb)
- Cpio archive (\*.cpio)
- Tar archive (\*.tar)
- GZip archive (_.gz;_.gzip;_.tgz;_.tpz)
- Ntfs archive (_.ntfs;_.img)
- Fat archive (_.fat;_.img)
- Mbr archive (\*.mbr)
- Vhd archive (\*.vhd)
- MsLZ archive (\*.)
- Flv archive (\*.flv)
- Swf archive (\*.swf)
- APM archive (\*.)
- PPMD archive (\*.pmd)
- Terse Executable (\*.te)
- UEFIc archive (\*.scap)
- UEFIs archive (\*.)
- SquashFS archive (\*.squashfs)
- CramFS archive (\*.cramfs)
- Ext filesystem archive (_.ext;_.ext2;_.ext3;_.ext4;\*.img)
- Virtual Machine Disk archive (\*.vmdk)
- Virtual Disk Image archive (\*.vdi)
- QEMU Copy On Write archive (_.qcow;_.qcow2;\*.qcow2c)
- GUID Partition Table archive (_.gpt;_.mbr)
- RAR v5 archive (_.rar;_.r00)
- IHex archive (\*.ihex)
- Help 2.0 archive (_.hxs;_.hxi;_.hxr;_.hxq;_.hxw;_.lit)

## Supported compression formats

- Zip archive (_.zip;_.jar;_.ear;_.war;_.cbz;_.apk;_.wsz;_.wal;_.xpi;_.crx;_.dfsz;_.pcv;_.bsz;_.mskin;  
  _.wmz;_.ipa;_.docx;_.xlsx;_.pptx;_.sxw;_.sxi;_.sxt;_.sxd;_.sxc;_.sxm;_.sxg;_.stw;_.sti;_.std;_.stc;  
  _.odh;_.odd;_.odt;_.odm;_.ods;_.ots;_.odg;_.otg;_.odp;_.otp;_.odf;_.odb)|_.zip;_.jar;_.ear;_.war;  
  _.cbz;_.apk;_.wsz;_.wal;_.xpi;_.crx;_.dfsz;_.pcv;_.bsz;_.mskin;_.wmz;_.ipa;_.docx;_.xlsx;_.pptx;  
  _.sxw;_.sxi;_.sxt;_.sxd;_.sxc;_.sxm;_.sxg;_.stw;_.sti;_.std;_.stc;_.odh;_.odd;_.odt;_.odm;_.ods;  
  _.ots;_.odg;_.otg;_.odp;_.otp;_.odf;_.odb|
- BZip2 archive (_.bz2;_.bzip2;_.tbz2;_.tbz)
- 7z archive (\*.7z)
- Tar archive (\*.tar)
- GZip archive (_.gz;_.gzip;_.tgz;_.tpz)
- Swf archive (\*.swf)

{{< aetl >}}
