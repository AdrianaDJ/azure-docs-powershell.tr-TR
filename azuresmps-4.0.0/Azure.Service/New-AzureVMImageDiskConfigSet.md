---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106198"
---
# <span data-ttu-id="b8c95-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="b8c95-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="b8c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c95-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c95-103">Disk yapılandırma kümesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8c95-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="b8c95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8c95-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c95-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8c95-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c95-106">**New-AzureVMImageDiskConfigSet** cmdlet 'i, resim Güncelleştirme cmdlet 'ine geçirilen bir disk yapılandırma kümesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8c95-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="b8c95-107">OSDiskConfig ve DataDiskConfig nesnesini kapsüller.</span><span class="sxs-lookup"><span data-stu-id="b8c95-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="b8c95-108">Sanal makine görüntüsünün işletim sistemi disk ve veri diski özelliklerini ayarlamak için **set-AzureVMImageOSDiskConfig** ve **set-AzureVMImageDataDiskConfig** cmdlet 'lerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b8c95-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="b8c95-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8c95-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c95-110">Örnek 1: disk yapılandırma kümesi nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b8c95-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="b8c95-111">Bu komut, bir disk yapılandırma kümesi nesnesi oluşturur ve sonuçları $Disk adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b8c95-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="b8c95-112">Disk yapılandırması oluşturulduktan sonra, OSDiskConfig ve DataDiskConfig 'yi ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b8c95-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="b8c95-113">Ardından sanal makine yapılandırmayla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b8c95-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="b8c95-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8c95-114">PARAMETERS</span></span>

### <span data-ttu-id="b8c95-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b8c95-115">-InformationAction</span></span>
<span data-ttu-id="b8c95-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8c95-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8c95-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b8c95-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8c95-118">'A</span><span class="sxs-lookup"><span data-stu-id="b8c95-118">Continue</span></span>
- <span data-ttu-id="b8c95-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="b8c95-119">Ignore</span></span>
- <span data-ttu-id="b8c95-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b8c95-120">Inquire</span></span>
- <span data-ttu-id="b8c95-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b8c95-121">SilentlyContinue</span></span>
- <span data-ttu-id="b8c95-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b8c95-122">Stop</span></span>
- <span data-ttu-id="b8c95-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b8c95-123">Suspend</span></span>

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

### <span data-ttu-id="b8c95-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b8c95-124">-InformationVariable</span></span>
<span data-ttu-id="b8c95-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8c95-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8c95-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c95-126">CommonParameters</span></span>
<span data-ttu-id="b8c95-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8c95-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c95-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c95-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c95-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8c95-129">INPUTS</span></span>

## <span data-ttu-id="b8c95-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8c95-130">OUTPUTS</span></span>

### <span data-ttu-id="b8c95-131">Microsoft. Windowsazde. Commands. ServiceManagement. model. Virtualmachineımagediskconfigset</span><span class="sxs-lookup"><span data-stu-id="b8c95-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="b8c95-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8c95-132">NOTES</span></span>

## <span data-ttu-id="b8c95-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8c95-133">RELATED LINKS</span></span>

[<span data-ttu-id="b8c95-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="b8c95-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="b8c95-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b8c95-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="b8c95-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b8c95-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


