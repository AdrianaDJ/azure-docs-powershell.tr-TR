---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267852"
---
# <span data-ttu-id="b30e1-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="b30e1-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="b30e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b30e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b30e1-103">CosmosDB hesabının bölgelerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b30e1-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="b30e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b30e1-104">SYNTAX</span></span>

### <span data-ttu-id="b30e1-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b30e1-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b30e1-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b30e1-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b30e1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b30e1-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b30e1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b30e1-108">DESCRIPTION</span></span>
<span data-ttu-id="b30e1-109">CosmosDB hesabının bölgelerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b30e1-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="b30e1-110">Konum, PSLocation türünde bir nesne veya yük devretme önceliği tarafından sıralanan konum adı dizeleri olarak sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b30e1-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="b30e1-111">LocationObject parametresi, yeni konumlara karşılık gelen yeni LocationObjects 'in eklendiği geçerli konumların (yük devretme öncelik listeleri) listesini bekler.</span><span class="sxs-lookup"><span data-stu-id="b30e1-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="b30e1-112">Location parametresi geçerli konumun (yük devretme önceliğine göre sıralanmış) listesini ve yeni konumları bekler.</span><span class="sxs-lookup"><span data-stu-id="b30e1-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="b30e1-113">Lütfen lütfen bölge eklenmesini destekliyoruz.</span><span class="sxs-lookup"><span data-stu-id="b30e1-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="b30e1-114">Lütfen konum veya LocationObject sağlayın.</span><span class="sxs-lookup"><span data-stu-id="b30e1-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="b30e1-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b30e1-115">EXAMPLES</span></span>

### <span data-ttu-id="b30e1-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b30e1-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="b30e1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b30e1-117">PARAMETERS</span></span>

### <span data-ttu-id="b30e1-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="b30e1-118">-AsJob</span></span>
<span data-ttu-id="b30e1-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b30e1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b30e1-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="b30e1-120">-Confirm</span></span>
<span data-ttu-id="b30e1-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b30e1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b30e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30e1-122">-DefaultProfile</span></span>
<span data-ttu-id="b30e1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b30e1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b30e1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b30e1-124">-InputObject</span></span>
<span data-ttu-id="b30e1-125">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="b30e1-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b30e1-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="b30e1-126">-Location</span></span>
<span data-ttu-id="b30e1-127">Eklenecek yerin adı.</span><span class="sxs-lookup"><span data-stu-id="b30e1-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30e1-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="b30e1-128">-LocationObject</span></span>
<span data-ttu-id="b30e1-129">Cosmos DB veritabanı hesabına konum ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b30e1-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="b30e1-130">PSLocation nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="b30e1-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30e1-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="b30e1-131">-Name</span></span>
<span data-ttu-id="b30e1-132">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b30e1-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b30e1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30e1-133">-ResourceGroupName</span></span>
<span data-ttu-id="b30e1-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b30e1-134">Name of resource group.</span></span>

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

### <span data-ttu-id="b30e1-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b30e1-135">-ResourceId</span></span>
<span data-ttu-id="b30e1-136">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="b30e1-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="b30e1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b30e1-137">-WhatIf</span></span>
<span data-ttu-id="b30e1-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b30e1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b30e1-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b30e1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b30e1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30e1-140">CommonParameters</span></span>
<span data-ttu-id="b30e1-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b30e1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30e1-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b30e1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30e1-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b30e1-143">INPUTS</span></span>

### <span data-ttu-id="b30e1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b30e1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b30e1-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b30e1-145">OUTPUTS</span></span>

### <span data-ttu-id="b30e1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b30e1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b30e1-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b30e1-147">NOTES</span></span>

## <span data-ttu-id="b30e1-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b30e1-148">RELATED LINKS</span></span>
