---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591050"
---
# <span data-ttu-id="a9d62-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="a9d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9d62-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d62-103">Belirtilen bir VMSS 'de belirli eylemleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a9d62-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9d62-104">SYNTAX</span></span>

### <span data-ttu-id="a9d62-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9d62-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d62-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="a9d62-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9d62-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9d62-107">DESCRIPTION</span></span>
<span data-ttu-id="a9d62-108">**Set-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinde belirli eylemleri ayarlar (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a9d62-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a9d62-109">Bu cmdlet 'in desteklediği tek eylem yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a9d62-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="a9d62-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9d62-110">EXAMPLES</span></span>

### <span data-ttu-id="a9d62-111">Örnek 1: VMSS 'yi yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="a9d62-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a9d62-112">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı VMSUBNET 'leri yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a9d62-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="a9d62-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9d62-113">PARAMETERS</span></span>

### <span data-ttu-id="a9d62-114">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="a9d62-114">-Reimage</span></span>
<span data-ttu-id="a9d62-115">Cmdlet 'in VMSS 'yi yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9d62-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-116">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="a9d62-116">-ReimageAll</span></span>
<span data-ttu-id="a9d62-117">Cmdlet 'in VMSS 'deki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9d62-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d62-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9d62-119">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9d62-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a9d62-120">-VMScaleSetName</span></span>
<span data-ttu-id="a9d62-121">Türleri bu cmdlet 'in eylemleri ayarladığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="a9d62-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9d62-122">-Confirm</span></span>
<span data-ttu-id="a9d62-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9d62-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d62-124">-WhatIf</span></span>
<span data-ttu-id="a9d62-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9d62-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9d62-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9d62-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d62-127">CommonParameters</span></span>
<span data-ttu-id="a9d62-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9d62-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d62-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d62-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d62-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9d62-130">INPUTS</span></span>

### <span data-ttu-id="a9d62-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9d62-131">None</span></span>
<span data-ttu-id="a9d62-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a9d62-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9d62-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9d62-133">OUTPUTS</span></span>

### <span data-ttu-id="a9d62-134">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a9d62-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a9d62-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9d62-135">NOTES</span></span>

## <span data-ttu-id="a9d62-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9d62-136">RELATED LINKS</span></span>

[<span data-ttu-id="a9d62-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a9d62-138">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a9d62-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a9d62-140">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a9d62-141">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="a9d62-142">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a9d62-143">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9d62-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


