---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937548"
---
# <span data-ttu-id="53d79-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="53d79-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="53d79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53d79-102">SYNOPSIS</span></span>
<span data-ttu-id="53d79-103">CosmosDB hesabı alın.</span><span class="sxs-lookup"><span data-stu-id="53d79-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="53d79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53d79-104">SYNTAX</span></span>

### <span data-ttu-id="53d79-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="53d79-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53d79-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="53d79-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53d79-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="53d79-107">DESCRIPTION</span></span>
<span data-ttu-id="53d79-108">**Get-AzCosmosDBAccount** cmdlet 'i, belirli bir resourcegroupname için varolan tüm cosmosdb hesaplarının listesini alır ve belirli bir Resourcegroupname ve AccountName için tek bir cosmosdb hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="53d79-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="53d79-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53d79-109">EXAMPLES</span></span>

### <span data-ttu-id="53d79-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53d79-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="53d79-111">ResourceGroup resourceGroupName içinde ad databaseAccountName ile CosmosDB veritabanı hesabını edinin.</span><span class="sxs-lookup"><span data-stu-id="53d79-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="53d79-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53d79-112">PARAMETERS</span></span>

### <span data-ttu-id="53d79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d79-113">-DefaultProfile</span></span>
<span data-ttu-id="53d79-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53d79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d79-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="53d79-115">-Name</span></span>
<span data-ttu-id="53d79-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="53d79-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53d79-117">-ResourceGroupName</span></span>
<span data-ttu-id="53d79-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="53d79-118">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d79-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="53d79-119">-ResourceId</span></span>
<span data-ttu-id="53d79-120">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="53d79-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d79-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d79-121">CommonParameters</span></span>
<span data-ttu-id="53d79-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53d79-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d79-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="53d79-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d79-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53d79-124">INPUTS</span></span>

### <span data-ttu-id="53d79-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="53d79-125">None</span></span>

## <span data-ttu-id="53d79-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53d79-126">OUTPUTS</span></span>

### <span data-ttu-id="53d79-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="53d79-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="53d79-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53d79-128">NOTES</span></span>

## <span data-ttu-id="53d79-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53d79-129">RELATED LINKS</span></span>