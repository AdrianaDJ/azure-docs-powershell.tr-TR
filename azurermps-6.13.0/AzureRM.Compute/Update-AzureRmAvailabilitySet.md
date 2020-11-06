---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592031"
---
# <span data-ttu-id="d6919-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d6919-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d6919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6919-102">SYNOPSIS</span></span>
<span data-ttu-id="d6919-103">Kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d6919-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6919-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6919-104">SYNTAX</span></span>

### <span data-ttu-id="d6919-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6919-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6919-106">Managedparamset</span><span class="sxs-lookup"><span data-stu-id="d6919-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6919-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6919-107">DESCRIPTION</span></span>
<span data-ttu-id="d6919-108">**Update-AzureRmAvailabilitySet** cmdlet 'i bir kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d6919-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="d6919-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6919-109">EXAMPLES</span></span>

### <span data-ttu-id="d6919-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d6919-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="d6919-111">Bu komut, ' ResourceGroup01 ' adındaki kaynak grubundaki ' AvSet01 ' adındaki kullanılabilirlik kümesini yönetilen bir kullanılabilirlik kümesine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d6919-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="d6919-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6919-112">PARAMETERS</span></span>

### <span data-ttu-id="d6919-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d6919-113">-AsJob</span></span>
<span data-ttu-id="d6919-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="d6919-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d6919-115">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="d6919-115">-AvailabilitySet</span></span>
<span data-ttu-id="d6919-116">Güncelleştirilecek kullanılabilirlik kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6919-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="d6919-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6919-117">-DefaultProfile</span></span>
<span data-ttu-id="d6919-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6919-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6919-119">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="d6919-119">-Managed</span></span>
<span data-ttu-id="d6919-120">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="d6919-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="d6919-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="d6919-121">-Sku</span></span>
<span data-ttu-id="d6919-122">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="d6919-122">The Name of Sku</span></span>

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

### <span data-ttu-id="d6919-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d6919-123">-Tag</span></span>
<span data-ttu-id="d6919-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d6919-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="d6919-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6919-125">-Confirm</span></span>
<span data-ttu-id="d6919-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d6919-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6919-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6919-127">-WhatIf</span></span>
<span data-ttu-id="d6919-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6919-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6919-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d6919-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6919-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6919-130">CommonParameters</span></span>
<span data-ttu-id="d6919-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6919-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6919-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6919-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6919-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6919-133">INPUTS</span></span>

### <span data-ttu-id="d6919-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d6919-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d6919-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6919-135">OUTPUTS</span></span>

### <span data-ttu-id="d6919-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d6919-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d6919-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6919-137">NOTES</span></span>

## <span data-ttu-id="d6919-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6919-138">RELATED LINKS</span></span>
