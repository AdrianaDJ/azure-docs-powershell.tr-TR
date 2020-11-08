---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105436"
---
# <span data-ttu-id="f98af-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f98af-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="f98af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98af-102">SYNOPSIS</span></span>
<span data-ttu-id="f98af-103">Sanal makine yansımasındaki veri diski özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f98af-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="f98af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f98af-104">SYNTAX</span></span>

### <span data-ttu-id="f98af-105">UpdateAzureVMImageParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f98af-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f98af-106">Addazurevmımageparamparam</span><span class="sxs-lookup"><span data-stu-id="f98af-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f98af-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f98af-107">DESCRIPTION</span></span>
<span data-ttu-id="f98af-108">**Set-AzureVMImageDataDiskConfig** cmdlet 'i sanal makine yansımasındaki veri diski özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f98af-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="f98af-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f98af-109">EXAMPLES</span></span>

### <span data-ttu-id="f98af-110">Örnek 1: sanal makine yansımasında veri diski özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f98af-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="f98af-111">Bu komut sanal makinedeki veri diski özelliklerini ayarlar ve ardından sanal makine yansımasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f98af-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="f98af-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f98af-112">PARAMETERS</span></span>

### <span data-ttu-id="f98af-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="f98af-113">-DataDiskName</span></span>
<span data-ttu-id="f98af-114">Bu cmdlet 'in yapılandırdığı veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98af-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98af-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="f98af-115">-DiskConfig</span></span>
<span data-ttu-id="f98af-116">İşletim sistemi diskinin ve veri diskinin nesnelerini kapsülleyen disk yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98af-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="f98af-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="f98af-117">-HostCaching</span></span>
<span data-ttu-id="f98af-118">İşletim sistemi diskinin ana bilgisayar önbelleği özniteliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98af-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="f98af-119">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f98af-119">Valid values are:</span></span>

<span data-ttu-id="f98af-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f98af-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98af-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f98af-121">-InformationAction</span></span>
<span data-ttu-id="f98af-122">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98af-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f98af-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f98af-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f98af-124">'A</span><span class="sxs-lookup"><span data-stu-id="f98af-124">Continue</span></span>
- <span data-ttu-id="f98af-125">Manıza</span><span class="sxs-lookup"><span data-stu-id="f98af-125">Ignore</span></span>
- <span data-ttu-id="f98af-126">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f98af-126">Inquire</span></span>
- <span data-ttu-id="f98af-127">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f98af-127">SilentlyContinue</span></span>
- <span data-ttu-id="f98af-128">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f98af-128">Stop</span></span>
- <span data-ttu-id="f98af-129">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f98af-129">Suspend</span></span>

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

### <span data-ttu-id="f98af-130">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f98af-130">-InformationVariable</span></span>
<span data-ttu-id="f98af-131">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98af-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f98af-132">-LUN</span><span class="sxs-lookup"><span data-stu-id="f98af-132">-Lun</span></span>
<span data-ttu-id="f98af-133">Sanal makinede veri sürücüsünün bağlı olduğu yuvayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98af-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98af-134">-Medialınk</span><span class="sxs-lookup"><span data-stu-id="f98af-134">-MediaLink</span></span>
<span data-ttu-id="f98af-135">Yeni veri diski eklendiğinde yeni sanal sabit sürücünün oluşturulduğu konumun URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98af-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98af-136">CommonParameters</span></span>
<span data-ttu-id="f98af-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f98af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98af-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f98af-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98af-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f98af-139">INPUTS</span></span>

## <span data-ttu-id="f98af-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f98af-140">OUTPUTS</span></span>

### <span data-ttu-id="f98af-141">Microsoft. Windowsazde. Commands. ServiceManagement. model. Virtualmachineımagediskconfigset</span><span class="sxs-lookup"><span data-stu-id="f98af-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="f98af-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f98af-142">NOTES</span></span>

## <span data-ttu-id="f98af-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f98af-143">RELATED LINKS</span></span>

[<span data-ttu-id="f98af-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f98af-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


