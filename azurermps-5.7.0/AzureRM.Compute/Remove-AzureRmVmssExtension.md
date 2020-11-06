---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589847"
---
# <span data-ttu-id="95a8b-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="95a8b-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="95a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="95a8b-103">Bir uzantıyı VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95a8b-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95a8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95a8b-104">SYNTAX</span></span>

### <span data-ttu-id="95a8b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95a8b-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95a8b-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="95a8b-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95a8b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="95a8b-107">DESCRIPTION</span></span>
<span data-ttu-id="95a8b-108">**Remove-Azurermvmssextenma** cmdlet 'ı sanal makine ölçek kümesinden (VMSS) uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95a8b-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="95a8b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95a8b-109">EXAMPLES</span></span>

## <span data-ttu-id="95a8b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95a8b-110">PARAMETERS</span></span>

### <span data-ttu-id="95a8b-111">-ID</span><span class="sxs-lookup"><span data-stu-id="95a8b-111">-Id</span></span>
<span data-ttu-id="95a8b-112">Bu cmdlet 'in VMSUBNET 'den kaldırdığı uzantının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="95a8b-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a8b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="95a8b-113">-Name</span></span>
<span data-ttu-id="95a8b-114">Bu cmdlet 'in kaldırıldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95a8b-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a8b-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="95a8b-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="95a8b-116">Uzantısının kaldırılacağı VMSS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="95a8b-116">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95a8b-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="95a8b-117">-Confirm</span></span>
<span data-ttu-id="95a8b-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95a8b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a8b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a8b-119">-WhatIf</span></span>
<span data-ttu-id="95a8b-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95a8b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95a8b-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95a8b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a8b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a8b-122">CommonParameters</span></span>
<span data-ttu-id="95a8b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95a8b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a8b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a8b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a8b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95a8b-125">INPUTS</span></span>

### <span data-ttu-id="95a8b-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="95a8b-126">None</span></span>
<span data-ttu-id="95a8b-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="95a8b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95a8b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95a8b-128">OUTPUTS</span></span>

### <span data-ttu-id="95a8b-129">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="95a8b-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="95a8b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95a8b-130">NOTES</span></span>

## <span data-ttu-id="95a8b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95a8b-131">RELATED LINKS</span></span>

[<span data-ttu-id="95a8b-132">Add-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="95a8b-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
