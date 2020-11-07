---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 5967ffbb5b0a39a771604c2f456de008d98de5fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759269"
---
# <span data-ttu-id="0746e-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0746e-101">Set-AzSearchService</span></span>

## <span data-ttu-id="0746e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0746e-102">SYNOPSIS</span></span>
<span data-ttu-id="0746e-103">Azure Search hizmetini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="0746e-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="0746e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0746e-104">SYNTAX</span></span>

### <span data-ttu-id="0746e-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0746e-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0746e-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="0746e-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0746e-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0746e-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0746e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0746e-108">DESCRIPTION</span></span>
<span data-ttu-id="0746e-109">**Set-Azaramahizmeti** cmdlet 'ı Azure Search hizmetini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0746e-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="0746e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0746e-110">EXAMPLES</span></span>

### <span data-ttu-id="0746e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0746e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="0746e-112">Örnek, Azure Search hizmetinin bölüm sayısını ve çoğaltma sayısını 2 olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0746e-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="0746e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0746e-113">PARAMETERS</span></span>

### <span data-ttu-id="0746e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0746e-114">-DefaultProfile</span></span>
<span data-ttu-id="0746e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0746e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0746e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0746e-116">-InputObject</span></span>
<span data-ttu-id="0746e-117">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0746e-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0746e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0746e-118">-Name</span></span>
<span data-ttu-id="0746e-119">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="0746e-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0746e-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="0746e-120">-PartitionCount</span></span>
<span data-ttu-id="0746e-121">Arama hizmeti bölüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="0746e-121">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0746e-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0746e-122">-ReplicaCount</span></span>
<span data-ttu-id="0746e-123">Arama hizmeti kopya sayısı.</span><span class="sxs-lookup"><span data-stu-id="0746e-123">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0746e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0746e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0746e-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0746e-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0746e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0746e-126">-ResourceId</span></span>
<span data-ttu-id="0746e-127">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0746e-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0746e-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0746e-128">-Confirm</span></span>
<span data-ttu-id="0746e-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0746e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0746e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0746e-130">-WhatIf</span></span>
<span data-ttu-id="0746e-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0746e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0746e-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0746e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0746e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0746e-133">CommonParameters</span></span>
<span data-ttu-id="0746e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0746e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0746e-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0746e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0746e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0746e-136">INPUTS</span></span>

### <span data-ttu-id="0746e-137">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0746e-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="0746e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0746e-138">System.String</span></span>

## <span data-ttu-id="0746e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0746e-139">OUTPUTS</span></span>

### <span data-ttu-id="0746e-140">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0746e-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="0746e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0746e-141">NOTES</span></span>

## <span data-ttu-id="0746e-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0746e-142">RELATED LINKS</span></span>

[<span data-ttu-id="0746e-143">Yeni-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="0746e-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="0746e-144">Get-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="0746e-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="0746e-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0746e-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)