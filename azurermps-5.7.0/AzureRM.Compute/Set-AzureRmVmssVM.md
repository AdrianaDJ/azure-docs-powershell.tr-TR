---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591042"
---
# <span data-ttu-id="c7335-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="c7335-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="c7335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7335-102">SYNOPSIS</span></span>
<span data-ttu-id="c7335-103">Bir VMSS örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c7335-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7335-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7335-104">SYNTAX</span></span>

### <span data-ttu-id="c7335-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7335-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7335-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="c7335-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7335-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7335-107">DESCRIPTION</span></span>
<span data-ttu-id="c7335-108">**Set-AzureRmVmssVM** cmdlet 'ı sanal makine ölçeği KÜMESI (VMSS) örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c7335-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c7335-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7335-109">EXAMPLES</span></span>

## <span data-ttu-id="c7335-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7335-110">PARAMETERS</span></span>

### <span data-ttu-id="c7335-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c7335-111">-InstanceId</span></span>
<span data-ttu-id="c7335-112">Bu cmdlet 'in durumu değiştirdiği VMSS örneğinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7335-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="c7335-113">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="c7335-113">-Reimage</span></span>
<span data-ttu-id="c7335-114">Bu cmdlet 'in VMSS örneğini yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7335-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7335-115">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="c7335-115">-ReimageAll</span></span>
<span data-ttu-id="c7335-116">Cmdlet 'in VMSS örneğindeki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7335-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7335-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7335-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7335-118">VMSS örneğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7335-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="c7335-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c7335-119">-VMScaleSetName</span></span>
<span data-ttu-id="c7335-120">Bu cmdlet 'in değiştirdiği VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7335-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c7335-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7335-121">-Confirm</span></span>
<span data-ttu-id="c7335-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7335-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7335-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7335-123">-WhatIf</span></span>
<span data-ttu-id="c7335-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7335-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7335-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7335-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7335-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7335-126">CommonParameters</span></span>
<span data-ttu-id="c7335-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7335-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7335-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7335-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7335-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7335-129">INPUTS</span></span>

### <span data-ttu-id="c7335-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c7335-130">None</span></span>
<span data-ttu-id="c7335-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c7335-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7335-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7335-132">OUTPUTS</span></span>

## <span data-ttu-id="c7335-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7335-133">NOTES</span></span>

## <span data-ttu-id="c7335-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7335-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7335-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="c7335-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
