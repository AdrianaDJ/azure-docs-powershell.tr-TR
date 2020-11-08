---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108102"
---
# <span data-ttu-id="61431-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="61431-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="61431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61431-102">SYNOPSIS</span></span>
<span data-ttu-id="61431-103">Kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="61431-103">Updates an availability set.</span></span>

## <span data-ttu-id="61431-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61431-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61431-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61431-105">DESCRIPTION</span></span>
<span data-ttu-id="61431-106">**Update-AzAvailabilitySet** cmdlet 'i bir kullanılabilirlik kümesini günceller.</span><span class="sxs-lookup"><span data-stu-id="61431-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="61431-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61431-107">EXAMPLES</span></span>

### <span data-ttu-id="61431-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61431-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="61431-109">Bu komut, ' ResourceGroup01 ' adındaki kaynak grubundaki ' AvSet01 ' adındaki kullanılabilirlik kümesini yönetilen bir kullanılabilirlik kümesine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="61431-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="61431-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61431-110">PARAMETERS</span></span>

### <span data-ttu-id="61431-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="61431-111">-AsJob</span></span>
<span data-ttu-id="61431-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="61431-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="61431-113">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="61431-113">-AvailabilitySet</span></span>
<span data-ttu-id="61431-114">Güncelleştirilecek kullanılabilirlik kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61431-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="61431-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61431-115">-DefaultProfile</span></span>
<span data-ttu-id="61431-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61431-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61431-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="61431-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="61431-118">Bu kullanılabilirlik kümesiyle kullanılacak yakınlık yerleşimi grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="61431-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61431-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="61431-119">-Sku</span></span>
<span data-ttu-id="61431-120">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="61431-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61431-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="61431-121">-Tag</span></span>
<span data-ttu-id="61431-122">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="61431-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="61431-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="61431-123">-Confirm</span></span>
<span data-ttu-id="61431-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61431-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61431-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61431-125">-WhatIf</span></span>
<span data-ttu-id="61431-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61431-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61431-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61431-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61431-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61431-128">CommonParameters</span></span>
<span data-ttu-id="61431-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61431-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61431-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61431-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61431-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61431-131">INPUTS</span></span>

### <span data-ttu-id="61431-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="61431-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="61431-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61431-133">OUTPUTS</span></span>

### <span data-ttu-id="61431-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="61431-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="61431-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61431-135">NOTES</span></span>

## <span data-ttu-id="61431-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61431-136">RELATED LINKS</span></span>
