---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106445"
---
# <span data-ttu-id="49950-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="49950-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="49950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49950-102">SYNOPSIS</span></span>
<span data-ttu-id="49950-103">DiskConfigSet nesnesinden işletim sistemi disk yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="49950-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="49950-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49950-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="49950-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49950-105">DESCRIPTION</span></span>
<span data-ttu-id="49950-106">**Remove-AzureVMImageOSDiskConfig** cmdlet 'ı DiskConfigSet nesnesinden işletim sistemi disk yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="49950-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="49950-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49950-107">EXAMPLES</span></span>

### <span data-ttu-id="49950-108">Örnek 1: disk yapılandırmasını DiskConfigSet 'ten kaldırma</span><span class="sxs-lookup"><span data-stu-id="49950-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="49950-109">Bu komut DiskConfigSet nesnesinden işletim sistemi disk yapılandırmasını kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="49950-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="49950-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49950-110">PARAMETERS</span></span>

### <span data-ttu-id="49950-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="49950-111">-DiskConfig</span></span>
<span data-ttu-id="49950-112">İşletim sistemi diskinin ve veri diskinin nesnelerini kapsülleyen disk yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="49950-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="49950-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="49950-113">-InformationAction</span></span>
<span data-ttu-id="49950-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="49950-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49950-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="49950-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49950-116">'A</span><span class="sxs-lookup"><span data-stu-id="49950-116">Continue</span></span>
- <span data-ttu-id="49950-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="49950-117">Ignore</span></span>
- <span data-ttu-id="49950-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="49950-118">Inquire</span></span>
- <span data-ttu-id="49950-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="49950-119">SilentlyContinue</span></span>
- <span data-ttu-id="49950-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="49950-120">Stop</span></span>
- <span data-ttu-id="49950-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="49950-121">Suspend</span></span>

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

### <span data-ttu-id="49950-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="49950-122">-InformationVariable</span></span>
<span data-ttu-id="49950-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="49950-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="49950-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49950-124">CommonParameters</span></span>
<span data-ttu-id="49950-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49950-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49950-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49950-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49950-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49950-127">INPUTS</span></span>

## <span data-ttu-id="49950-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49950-128">OUTPUTS</span></span>

### <span data-ttu-id="49950-129">Microsoft. Windowsazde. Commands. ServiceManagement. model. Virtualmachineımagediskconfigset</span><span class="sxs-lookup"><span data-stu-id="49950-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="49950-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49950-130">NOTES</span></span>

## <span data-ttu-id="49950-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49950-131">RELATED LINKS</span></span>

[<span data-ttu-id="49950-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="49950-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


