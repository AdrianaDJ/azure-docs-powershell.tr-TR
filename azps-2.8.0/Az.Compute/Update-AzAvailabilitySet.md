---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: ebb6635cd593e37eedf4a8e70230cbf0f42e0d92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752647"
---
# <span data-ttu-id="9d5d9-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d5d9-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="9d5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5d9-103">Kullanılabilirlik kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-103">Updates an availability set.</span></span>

## <span data-ttu-id="9d5d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d5d9-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5d9-106">**Update-AzAvailabilitySet** cmdlet 'i bir kullanılabilirlik kümesini günceller.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="9d5d9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d5d9-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5d9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9d5d9-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="9d5d9-109">Bu komut, ' ResourceGroup01 ' adındaki kaynak grubundaki ' AvSet01 ' adındaki kullanılabilirlik kümesini yönetilen bir kullanılabilirlik kümesine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="9d5d9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d5d9-110">PARAMETERS</span></span>

### <span data-ttu-id="9d5d9-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="9d5d9-111">-AsJob</span></span>
<span data-ttu-id="9d5d9-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9d5d9-113">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="9d5d9-113">-AvailabilitySet</span></span>
<span data-ttu-id="9d5d9-114">Güncelleştirilecek kullanılabilirlik kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="9d5d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5d9-115">-DefaultProfile</span></span>
<span data-ttu-id="9d5d9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d5d9-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="9d5d9-117">-Sku</span></span>
<span data-ttu-id="9d5d9-118">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="9d5d9-118">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5d9-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9d5d9-119">-Tag</span></span>
<span data-ttu-id="9d5d9-120">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-120">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="9d5d9-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="9d5d9-121">-Confirm</span></span>
<span data-ttu-id="9d5d9-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5d9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5d9-123">-WhatIf</span></span>
<span data-ttu-id="9d5d9-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d5d9-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5d9-126">CommonParameters</span></span>
<span data-ttu-id="9d5d9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5d9-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9d5d9-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5d9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d5d9-129">INPUTS</span></span>

### <span data-ttu-id="9d5d9-130">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d5d9-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9d5d9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d5d9-131">OUTPUTS</span></span>

### <span data-ttu-id="9d5d9-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d5d9-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9d5d9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d5d9-133">NOTES</span></span>

## <span data-ttu-id="9d5d9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d5d9-134">RELATED LINKS</span></span>
