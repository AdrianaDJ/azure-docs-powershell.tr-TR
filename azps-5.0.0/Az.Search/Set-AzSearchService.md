---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278185"
---
# <span data-ttu-id="11b6c-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="11b6c-101">Set-AzSearchService</span></span>

## <span data-ttu-id="11b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="11b6c-103">Azure Search hizmetini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="11b6c-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="11b6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11b6c-104">SYNTAX</span></span>

### <span data-ttu-id="11b6c-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="11b6c-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b6c-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="11b6c-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b6c-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="11b6c-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b6c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="11b6c-108">DESCRIPTION</span></span>
<span data-ttu-id="11b6c-109">**Set-Azaramahizmeti** cmdlet 'ı Azure Search hizmetini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="11b6c-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="11b6c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11b6c-110">EXAMPLES</span></span>

### <span data-ttu-id="11b6c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11b6c-111">Example 1</span></span>
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

<span data-ttu-id="11b6c-112">Örnek, Azure Search hizmetinin bölüm sayısını ve çoğaltma sayısını 2 olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="11b6c-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="11b6c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11b6c-113">PARAMETERS</span></span>

### <span data-ttu-id="11b6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b6c-114">-DefaultProfile</span></span>
<span data-ttu-id="11b6c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11b6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b6c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11b6c-116">-InputObject</span></span>
<span data-ttu-id="11b6c-117">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="11b6c-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="11b6c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="11b6c-118">-Name</span></span>
<span data-ttu-id="11b6c-119">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="11b6c-119">Search Service name.</span></span>

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

### <span data-ttu-id="11b6c-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="11b6c-120">-PartitionCount</span></span>
<span data-ttu-id="11b6c-121">Arama hizmeti bölüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="11b6c-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="11b6c-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="11b6c-122">-ReplicaCount</span></span>
<span data-ttu-id="11b6c-123">Arama hizmeti kopya sayısı.</span><span class="sxs-lookup"><span data-stu-id="11b6c-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="11b6c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b6c-124">-ResourceGroupName</span></span>
<span data-ttu-id="11b6c-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="11b6c-125">Resource Group name.</span></span>

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

### <span data-ttu-id="11b6c-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="11b6c-126">-ResourceId</span></span>
<span data-ttu-id="11b6c-127">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="11b6c-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="11b6c-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="11b6c-128">-Confirm</span></span>
<span data-ttu-id="11b6c-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11b6c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b6c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b6c-130">-WhatIf</span></span>
<span data-ttu-id="11b6c-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11b6c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11b6c-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11b6c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b6c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b6c-133">CommonParameters</span></span>
<span data-ttu-id="11b6c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11b6c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b6c-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b6c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b6c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11b6c-136">INPUTS</span></span>

### <span data-ttu-id="11b6c-137">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="11b6c-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="11b6c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="11b6c-138">System.String</span></span>

## <span data-ttu-id="11b6c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11b6c-139">OUTPUTS</span></span>

### <span data-ttu-id="11b6c-140">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="11b6c-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="11b6c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11b6c-141">NOTES</span></span>

## <span data-ttu-id="11b6c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11b6c-142">RELATED LINKS</span></span>

[<span data-ttu-id="11b6c-143">Yeni-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="11b6c-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="11b6c-144">Get-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="11b6c-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="11b6c-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="11b6c-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)