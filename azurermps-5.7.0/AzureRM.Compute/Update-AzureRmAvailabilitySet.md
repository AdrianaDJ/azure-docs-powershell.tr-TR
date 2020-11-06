---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586769"
---
# <span data-ttu-id="d7016-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d7016-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d7016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7016-102">SYNOPSIS</span></span>
<span data-ttu-id="d7016-103">Kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7016-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7016-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7016-104">SYNTAX</span></span>

### <span data-ttu-id="d7016-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7016-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7016-106">Managedparamset</span><span class="sxs-lookup"><span data-stu-id="d7016-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7016-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7016-107">DESCRIPTION</span></span>
<span data-ttu-id="d7016-108">**Update-AzureRmAvailabilitySet** cmdlet 'i bir kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7016-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="d7016-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7016-109">EXAMPLES</span></span>

### <span data-ttu-id="d7016-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d7016-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="d7016-111">Bu komut, ' ResourceGroup01 ' adındaki kaynak grubundaki ' AvSet01 ' adındaki kullanılabilirlik kümesini yönetilen bir kullanılabilirlik kümesine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7016-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="d7016-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7016-112">PARAMETERS</span></span>

### <span data-ttu-id="d7016-113">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="d7016-113">-AvailabilitySet</span></span>
<span data-ttu-id="d7016-114">Güncelleştirilecek kullanılabilirlik kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7016-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7016-115">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="d7016-115">-Managed</span></span>
<span data-ttu-id="d7016-116">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="d7016-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7016-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="d7016-117">-Sku</span></span>
<span data-ttu-id="d7016-118">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="d7016-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7016-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7016-119">-Confirm</span></span>
<span data-ttu-id="d7016-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7016-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7016-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7016-121">-WhatIf</span></span>
<span data-ttu-id="d7016-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7016-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7016-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7016-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7016-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7016-124">CommonParameters</span></span>
<span data-ttu-id="d7016-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7016-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7016-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7016-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7016-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7016-127">INPUTS</span></span>

### <span data-ttu-id="d7016-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d7016-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d7016-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7016-129">OUTPUTS</span></span>

### <span data-ttu-id="d7016-130">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d7016-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d7016-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7016-131">NOTES</span></span>

## <span data-ttu-id="d7016-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7016-132">RELATED LINKS</span></span>

