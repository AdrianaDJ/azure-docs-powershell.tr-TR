---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594766"
---
# <span data-ttu-id="e9fa8-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e9fa8-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e9fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fa8-103">Kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9fa8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9fa8-104">SYNTAX</span></span>

### <span data-ttu-id="e9fa8-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9fa8-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9fa8-106">Managedparamset</span><span class="sxs-lookup"><span data-stu-id="e9fa8-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9fa8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9fa8-107">DESCRIPTION</span></span>
<span data-ttu-id="e9fa8-108">**Update-AzureRmAvailabilitySet** cmdlet 'i bir kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="e9fa8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9fa8-109">EXAMPLES</span></span>

### <span data-ttu-id="e9fa8-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e9fa8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="e9fa8-111">Bu komut, ' ResourceGroup01 ' adındaki kaynak grubundaki ' AvSet01 ' adındaki kullanılabilirlik kümesini yönetilen bir kullanılabilirlik kümesine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="e9fa8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9fa8-112">PARAMETERS</span></span>

### <span data-ttu-id="e9fa8-113">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="e9fa8-113">-AvailabilitySet</span></span>
<span data-ttu-id="e9fa8-114">Güncelleştirilecek kullanılabilirlik kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fa8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fa8-115">-DefaultProfile</span></span>
<span data-ttu-id="e9fa8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fa8-117">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="e9fa8-117">-Managed</span></span>
<span data-ttu-id="e9fa8-118">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="e9fa8-118">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fa8-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="e9fa8-119">-Sku</span></span>
<span data-ttu-id="e9fa8-120">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="e9fa8-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fa8-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9fa8-121">-Confirm</span></span>
<span data-ttu-id="e9fa8-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fa8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9fa8-123">-WhatIf</span></span>
<span data-ttu-id="e9fa8-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9fa8-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fa8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fa8-126">CommonParameters</span></span>
<span data-ttu-id="e9fa8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9fa8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fa8-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9fa8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fa8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9fa8-129">INPUTS</span></span>

### <span data-ttu-id="e9fa8-130">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e9fa8-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e9fa8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9fa8-131">OUTPUTS</span></span>

### <span data-ttu-id="e9fa8-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e9fa8-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e9fa8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9fa8-133">NOTES</span></span>

## <span data-ttu-id="e9fa8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9fa8-134">RELATED LINKS</span></span>

