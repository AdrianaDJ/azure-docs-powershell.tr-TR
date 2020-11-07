---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4051cbb697625f527afdf2e189953c4d6e776214
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917191"
---
# <span data-ttu-id="496d3-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="496d3-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="496d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496d3-102">SYNOPSIS</span></span>
<span data-ttu-id="496d3-103">Kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="496d3-103">Updates an availability set.</span></span>

## <span data-ttu-id="496d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="496d3-104">SYNTAX</span></span>

### <span data-ttu-id="496d3-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="496d3-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496d3-106">Managedparamset</span><span class="sxs-lookup"><span data-stu-id="496d3-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="496d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="496d3-107">DESCRIPTION</span></span>
<span data-ttu-id="496d3-108">**Update-AzAvailabilitySet** cmdlet 'i bir kullanılabilirlik kümesini günceller.</span><span class="sxs-lookup"><span data-stu-id="496d3-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="496d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="496d3-109">EXAMPLES</span></span>

### <span data-ttu-id="496d3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="496d3-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="496d3-111">Bu komut, ' ResourceGroup01 ' adındaki kaynak grubundaki ' AvSet01 ' adındaki kullanılabilirlik kümesini yönetilen bir kullanılabilirlik kümesine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="496d3-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="496d3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="496d3-112">PARAMETERS</span></span>

### <span data-ttu-id="496d3-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="496d3-113">-AsJob</span></span>
<span data-ttu-id="496d3-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="496d3-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496d3-115">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="496d3-115">-AvailabilitySet</span></span>
<span data-ttu-id="496d3-116">Güncelleştirilecek kullanılabilirlik kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="496d3-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="496d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496d3-117">-DefaultProfile</span></span>
<span data-ttu-id="496d3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="496d3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496d3-119">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="496d3-119">-Managed</span></span>
<span data-ttu-id="496d3-120">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="496d3-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="496d3-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="496d3-121">-Sku</span></span>
<span data-ttu-id="496d3-122">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="496d3-122">The Name of Sku</span></span>

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

### <span data-ttu-id="496d3-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="496d3-123">-Tag</span></span>
<span data-ttu-id="496d3-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="496d3-124">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496d3-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="496d3-125">-Confirm</span></span>
<span data-ttu-id="496d3-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="496d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496d3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496d3-127">-WhatIf</span></span>
<span data-ttu-id="496d3-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="496d3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="496d3-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="496d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496d3-130">CommonParameters</span></span>
<span data-ttu-id="496d3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="496d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496d3-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="496d3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496d3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="496d3-133">INPUTS</span></span>

### <span data-ttu-id="496d3-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="496d3-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="496d3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="496d3-135">OUTPUTS</span></span>

### <span data-ttu-id="496d3-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="496d3-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="496d3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="496d3-137">NOTES</span></span>

## <span data-ttu-id="496d3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="496d3-138">RELATED LINKS</span></span>
