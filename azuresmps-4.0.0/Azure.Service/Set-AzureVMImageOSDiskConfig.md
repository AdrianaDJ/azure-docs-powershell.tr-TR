---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105444"
---
# <span data-ttu-id="9f71c-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9f71c-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="9f71c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f71c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f71c-103">Sanal makine yansımasındaki işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9f71c-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="9f71c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f71c-104">SYNTAX</span></span>

### <span data-ttu-id="9f71c-105">UpdateAzureVMImageParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f71c-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9f71c-106">Addazurevmımageparamparam</span><span class="sxs-lookup"><span data-stu-id="9f71c-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9f71c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f71c-107">DESCRIPTION</span></span>
<span data-ttu-id="9f71c-108">**Set-AzureVMImageOSDiskConfig** cmdlet 'i sanal makine yansımasındaki işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9f71c-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="9f71c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f71c-109">EXAMPLES</span></span>

### <span data-ttu-id="9f71c-110">Örnek 1: sanal makine yansımasında işletim sistemi disk özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="9f71c-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="9f71c-111">Bu örnekte, sanal makine yansımasındaki işletim sistemi disk özellikleri ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9f71c-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="9f71c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f71c-112">PARAMETERS</span></span>

### <span data-ttu-id="9f71c-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="9f71c-113">-DiskConfig</span></span>
<span data-ttu-id="9f71c-114">İşletim sistemi diskinin ve veri diskinin nesnelerini kapsülleyen disk yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f71c-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f71c-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="9f71c-115">-HostCaching</span></span>
<span data-ttu-id="9f71c-116">İşletim sistemi diskinin ana bilgisayar önbelleği özniteliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f71c-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="9f71c-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9f71c-117">Valid values are:</span></span>

<span data-ttu-id="9f71c-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9f71c-118">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f71c-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9f71c-119">-InformationAction</span></span>
<span data-ttu-id="9f71c-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f71c-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9f71c-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9f71c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f71c-122">'A</span><span class="sxs-lookup"><span data-stu-id="9f71c-122">Continue</span></span>
- <span data-ttu-id="9f71c-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="9f71c-123">Ignore</span></span>
- <span data-ttu-id="9f71c-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9f71c-124">Inquire</span></span>
- <span data-ttu-id="9f71c-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9f71c-125">SilentlyContinue</span></span>
- <span data-ttu-id="9f71c-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9f71c-126">Stop</span></span>
- <span data-ttu-id="9f71c-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9f71c-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f71c-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9f71c-128">-InformationVariable</span></span>
<span data-ttu-id="9f71c-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f71c-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f71c-130">-Medialınk</span><span class="sxs-lookup"><span data-stu-id="9f71c-130">-MediaLink</span></span>
<span data-ttu-id="9f71c-131">Yeni veri diski eklendiğinde yeni sanal sabit sürücünün oluşturulduğu konumun URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f71c-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f71c-132">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="9f71c-132">-OS</span></span>
<span data-ttu-id="9f71c-133">Disk yapılandırmasının işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f71c-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="9f71c-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9f71c-134">Valid values are:</span></span>

- <span data-ttu-id="9f71c-135">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="9f71c-135">Windows</span></span>
- <span data-ttu-id="9f71c-136">UX</span><span class="sxs-lookup"><span data-stu-id="9f71c-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f71c-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="9f71c-137">-OSState</span></span>
<span data-ttu-id="9f71c-138">Sanal makine görüntüsünün işletim sistemi durumunu belirtir</span><span class="sxs-lookup"><span data-stu-id="9f71c-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="9f71c-139">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9f71c-139">Valid values are:</span></span>

- <span data-ttu-id="9f71c-140">Genelleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="9f71c-140">Generalized</span></span>
- <span data-ttu-id="9f71c-141">Antivirüs</span><span class="sxs-lookup"><span data-stu-id="9f71c-141">Specialized</span></span>

<span data-ttu-id="9f71c-142">Bu parametrenin kullanımı, sanal makine görüntüsünü Azure 'a yakalama amacınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f71c-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f71c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f71c-143">CommonParameters</span></span>
<span data-ttu-id="9f71c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f71c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f71c-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f71c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f71c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f71c-146">INPUTS</span></span>

## <span data-ttu-id="9f71c-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f71c-147">OUTPUTS</span></span>

### <span data-ttu-id="9f71c-148">Microsoft. Windowsazde. Commands. ServiceManagement. model. Virtualmachineımagediskconfigset</span><span class="sxs-lookup"><span data-stu-id="9f71c-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="9f71c-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f71c-149">NOTES</span></span>

## <span data-ttu-id="9f71c-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f71c-150">RELATED LINKS</span></span>

[<span data-ttu-id="9f71c-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9f71c-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


