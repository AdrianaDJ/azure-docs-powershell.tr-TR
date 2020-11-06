---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586761"
---
# <span data-ttu-id="b7082-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="b7082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7082-102">SYNOPSIS</span></span>
<span data-ttu-id="b7082-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7082-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7082-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7082-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7082-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7082-105">DESCRIPTION</span></span>
<span data-ttu-id="b7082-106">**Update-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7082-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="b7082-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7082-107">EXAMPLES</span></span>

### <span data-ttu-id="b7082-108">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b7082-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="b7082-109">Bu komut, Group001 adındaki kaynak grubuna ait olan ve VMSS001 adındaki kaynak grubuna ait olan, LocalVMSS adlı yerel bir VMSS nesnesinin durumuna ait durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7082-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="b7082-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7082-110">PARAMETERS</span></span>

### <span data-ttu-id="b7082-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7082-111">-ResourceGroupName</span></span>
<span data-ttu-id="b7082-112">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7082-112">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="b7082-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b7082-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b7082-114">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7082-114">Specifies a local VMSS object.</span></span>
<span data-ttu-id="b7082-115">Bir VMSS nesnesi edinmek için Get-AzureRmVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b7082-115">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="b7082-116">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="b7082-116">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7082-117">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b7082-117">-VMScaleSetName</span></span>
<span data-ttu-id="b7082-118">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7082-118">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7082-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7082-119">-Confirm</span></span>
<span data-ttu-id="b7082-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7082-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7082-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7082-121">-WhatIf</span></span>
<span data-ttu-id="b7082-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7082-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b7082-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7082-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7082-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7082-124">CommonParameters</span></span>
<span data-ttu-id="b7082-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7082-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7082-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7082-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7082-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7082-127">INPUTS</span></span>

### <span data-ttu-id="b7082-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7082-128">None</span></span>
<span data-ttu-id="b7082-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b7082-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7082-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7082-130">OUTPUTS</span></span>

## <span data-ttu-id="b7082-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7082-131">NOTES</span></span>

## <span data-ttu-id="b7082-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7082-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7082-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="b7082-134">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b7082-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b7082-136">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="b7082-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b7082-138">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b7082-139">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7082-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


