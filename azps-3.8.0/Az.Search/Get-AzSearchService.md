---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097496"
---
# <span data-ttu-id="9ac33-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="9ac33-101">Get-AzSearchService</span></span>

## <span data-ttu-id="9ac33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac33-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac33-103">Bir Azure Search hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="9ac33-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="9ac33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ac33-104">SYNTAX</span></span>

### <span data-ttu-id="9ac33-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ac33-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ac33-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9ac33-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac33-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ac33-107">DESCRIPTION</span></span>
<span data-ttu-id="9ac33-108">**Get-Azaramahizmeti** cmdlet 'ı belirtilen Azure Search hizmetini alır.</span><span class="sxs-lookup"><span data-stu-id="9ac33-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="9ac33-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ac33-109">EXAMPLES</span></span>

### <span data-ttu-id="9ac33-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ac33-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="9ac33-111">Belirtilen parametrelerle bir Azure Search hizmeti edinin.</span><span class="sxs-lookup"><span data-stu-id="9ac33-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="9ac33-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ac33-112">PARAMETERS</span></span>

### <span data-ttu-id="9ac33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac33-113">-DefaultProfile</span></span>
<span data-ttu-id="9ac33-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ac33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac33-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ac33-115">-Name</span></span>
<span data-ttu-id="9ac33-116">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="9ac33-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac33-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ac33-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9ac33-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac33-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9ac33-119">-ResourceId</span></span>
<span data-ttu-id="9ac33-120">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9ac33-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="9ac33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac33-121">CommonParameters</span></span>
<span data-ttu-id="9ac33-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ac33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac33-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac33-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac33-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ac33-124">INPUTS</span></span>

### <span data-ttu-id="9ac33-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9ac33-125">System.String</span></span>

## <span data-ttu-id="9ac33-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ac33-126">OUTPUTS</span></span>

### <span data-ttu-id="9ac33-127">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9ac33-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="9ac33-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ac33-128">NOTES</span></span>

## <span data-ttu-id="9ac33-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ac33-129">RELATED LINKS</span></span>

[<span data-ttu-id="9ac33-130">Yeni-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="9ac33-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="9ac33-131">Set-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="9ac33-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="9ac33-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="9ac33-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)