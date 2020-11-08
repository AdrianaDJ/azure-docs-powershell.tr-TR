---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105497"
---
# <span data-ttu-id="e57c8-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e57c8-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="e57c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e57c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e57c8-103">DiskConfigSet nesnesinden veri diski yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e57c8-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="e57c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e57c8-104">SYNTAX</span></span>

### <span data-ttu-id="e57c8-105">RemoveByDiskName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e57c8-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e57c8-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="e57c8-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e57c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e57c8-107">DESCRIPTION</span></span>
<span data-ttu-id="e57c8-108">**Remove-AzureVMImageDataDiskConfig** cmdlet 'ı **diskconfigset** nesnesinden veri diski yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e57c8-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="e57c8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e57c8-109">EXAMPLES</span></span>

### <span data-ttu-id="e57c8-110">Örnek 1: DiskConfigSet nesnesinden veri diski yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e57c8-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="e57c8-111">Bu örnek **Diskconfigset** oluşturur, yapılandırır ve veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e57c8-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="e57c8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e57c8-112">PARAMETERS</span></span>

### <span data-ttu-id="e57c8-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="e57c8-113">-DataDiskName</span></span>
<span data-ttu-id="e57c8-114">Bu cmdlet 'in kaldırdığı veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e57c8-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57c8-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="e57c8-115">-DiskConfig</span></span>
<span data-ttu-id="e57c8-116">İşletim sistemi diskinin ve veri diskinin nesnelerini kapsülleyen disk yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e57c8-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="e57c8-117">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e57c8-117">-InformationAction</span></span>
<span data-ttu-id="e57c8-118">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e57c8-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e57c8-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e57c8-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e57c8-120">'A</span><span class="sxs-lookup"><span data-stu-id="e57c8-120">Continue</span></span>
- <span data-ttu-id="e57c8-121">Manıza</span><span class="sxs-lookup"><span data-stu-id="e57c8-121">Ignore</span></span>
- <span data-ttu-id="e57c8-122">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e57c8-122">Inquire</span></span>
- <span data-ttu-id="e57c8-123">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e57c8-123">SilentlyContinue</span></span>
- <span data-ttu-id="e57c8-124">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e57c8-124">Stop</span></span>
- <span data-ttu-id="e57c8-125">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e57c8-125">Suspend</span></span>

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

### <span data-ttu-id="e57c8-126">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e57c8-126">-InformationVariable</span></span>
<span data-ttu-id="e57c8-127">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e57c8-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e57c8-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="e57c8-128">-Lun</span></span>
<span data-ttu-id="e57c8-129">Sanal makinede veri sürücüsünün bağlı olduğu yuvayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e57c8-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57c8-130">CommonParameters</span></span>
<span data-ttu-id="e57c8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e57c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57c8-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57c8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57c8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e57c8-133">INPUTS</span></span>

## <span data-ttu-id="e57c8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e57c8-134">OUTPUTS</span></span>

### <span data-ttu-id="e57c8-135">Microsoft. Windowsazde. Commands. ServiceManagement. model. Virtualmachineımagediskconfigset</span><span class="sxs-lookup"><span data-stu-id="e57c8-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="e57c8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e57c8-136">NOTES</span></span>

## <span data-ttu-id="e57c8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e57c8-137">RELATED LINKS</span></span>

[<span data-ttu-id="e57c8-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e57c8-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


