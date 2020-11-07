---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935944"
---
# <span data-ttu-id="090e9-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="090e9-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="090e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="090e9-102">SYNOPSIS</span></span>
<span data-ttu-id="090e9-103">Kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="090e9-103">Updates an availability set.</span></span>

## <span data-ttu-id="090e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="090e9-104">SYNTAX</span></span>

### <span data-ttu-id="090e9-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="090e9-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="090e9-106">Managedparamset</span><span class="sxs-lookup"><span data-stu-id="090e9-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="090e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="090e9-107">DESCRIPTION</span></span>
<span data-ttu-id="090e9-108">**Update-AzAvailabilitySet** cmdlet 'i bir kullanılabilirlik kümesini günceller.</span><span class="sxs-lookup"><span data-stu-id="090e9-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="090e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="090e9-109">EXAMPLES</span></span>

### <span data-ttu-id="090e9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="090e9-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="090e9-111">Bu komut, ' ResourceGroup01 ' adındaki kaynak grubundaki ' AvSet01 ' adındaki kullanılabilirlik kümesini yönetilen bir kullanılabilirlik kümesine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="090e9-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="090e9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="090e9-112">PARAMETERS</span></span>

### <span data-ttu-id="090e9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="090e9-113">-AsJob</span></span>
<span data-ttu-id="090e9-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="090e9-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090e9-115">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="090e9-115">-AvailabilitySet</span></span>
<span data-ttu-id="090e9-116">Güncelleştirilecek kullanılabilirlik kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="090e9-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="090e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090e9-117">-DefaultProfile</span></span>
<span data-ttu-id="090e9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="090e9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090e9-119">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="090e9-119">-Managed</span></span>
<span data-ttu-id="090e9-120">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="090e9-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="090e9-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="090e9-121">-Sku</span></span>
<span data-ttu-id="090e9-122">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="090e9-122">The Name of Sku</span></span>

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

### <span data-ttu-id="090e9-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="090e9-123">-Confirm</span></span>
<span data-ttu-id="090e9-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="090e9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="090e9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="090e9-125">-WhatIf</span></span>
<span data-ttu-id="090e9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="090e9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="090e9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="090e9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="090e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090e9-128">CommonParameters</span></span>
<span data-ttu-id="090e9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="090e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090e9-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="090e9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090e9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="090e9-131">INPUTS</span></span>

### <span data-ttu-id="090e9-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="090e9-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="090e9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="090e9-133">OUTPUTS</span></span>

### <span data-ttu-id="090e9-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="090e9-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="090e9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="090e9-135">NOTES</span></span>

## <span data-ttu-id="090e9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="090e9-136">RELATED LINKS</span></span>

