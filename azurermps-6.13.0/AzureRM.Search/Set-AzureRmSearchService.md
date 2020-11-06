---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589352"
---
# <span data-ttu-id="682a8-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="682a8-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="682a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="682a8-102">SYNOPSIS</span></span>
<span data-ttu-id="682a8-103">Azure Search hizmetini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="682a8-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="682a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="682a8-104">SYNTAX</span></span>

### <span data-ttu-id="682a8-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="682a8-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="682a8-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="682a8-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="682a8-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="682a8-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="682a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="682a8-108">DESCRIPTION</span></span>
<span data-ttu-id="682a8-109">**Set-AzureRmSearchService** cmdlet 'ı bir Azure Search hizmetini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="682a8-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="682a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="682a8-110">EXAMPLES</span></span>

### <span data-ttu-id="682a8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="682a8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="682a8-112">Örnek, Azure Search hizmetinin bölüm sayısını ve çoğaltma sayısını 2 olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="682a8-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="682a8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="682a8-113">PARAMETERS</span></span>

### <span data-ttu-id="682a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="682a8-114">-DefaultProfile</span></span>
<span data-ttu-id="682a8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="682a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="682a8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="682a8-116">-InputObject</span></span>
<span data-ttu-id="682a8-117">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="682a8-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="682a8-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="682a8-118">-Name</span></span>
<span data-ttu-id="682a8-119">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="682a8-119">Search Service name.</span></span>

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

### <span data-ttu-id="682a8-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="682a8-120">-PartitionCount</span></span>
<span data-ttu-id="682a8-121">Arama hizmeti bölüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="682a8-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="682a8-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="682a8-122">-ReplicaCount</span></span>
<span data-ttu-id="682a8-123">Arama hizmeti kopya sayısı.</span><span class="sxs-lookup"><span data-stu-id="682a8-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="682a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="682a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="682a8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="682a8-125">Resource Group name.</span></span>

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

### <span data-ttu-id="682a8-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="682a8-126">-ResourceId</span></span>
<span data-ttu-id="682a8-127">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="682a8-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="682a8-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="682a8-128">-Confirm</span></span>
<span data-ttu-id="682a8-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="682a8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="682a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="682a8-130">-WhatIf</span></span>
<span data-ttu-id="682a8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="682a8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="682a8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="682a8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="682a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682a8-133">CommonParameters</span></span>
<span data-ttu-id="682a8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="682a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682a8-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="682a8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682a8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="682a8-136">INPUTS</span></span>

### <span data-ttu-id="682a8-137">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="682a8-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="682a8-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="682a8-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="682a8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="682a8-139">System.String</span></span>

## <span data-ttu-id="682a8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="682a8-140">OUTPUTS</span></span>

### <span data-ttu-id="682a8-141">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="682a8-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="682a8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="682a8-142">NOTES</span></span>

## <span data-ttu-id="682a8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="682a8-143">RELATED LINKS</span></span>

[<span data-ttu-id="682a8-144">Yeni-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="682a8-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="682a8-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="682a8-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="682a8-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="682a8-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
