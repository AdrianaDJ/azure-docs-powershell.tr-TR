---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096030"
---
# <span data-ttu-id="4e22b-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="4e22b-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="4e22b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e22b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e22b-103">CosmosDB hesap özniteliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4e22b-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="4e22b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e22b-104">SYNTAX</span></span>

### <span data-ttu-id="4e22b-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4e22b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e22b-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4e22b-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e22b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e22b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e22b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e22b-108">DESCRIPTION</span></span>
<span data-ttu-id="4e22b-109">CosmosDB hesabının özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4e22b-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="4e22b-110">Diğer özelliklerle simulataneously hesap bölgeleri güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="4e22b-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="4e22b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e22b-111">EXAMPLES</span></span>

### <span data-ttu-id="4e22b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4e22b-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="4e22b-113">Defaultbir "ad. düzey", "Strong", otomatik yeniden yük devri, etkin çoğul</span><span class="sxs-lookup"><span data-stu-id="4e22b-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="4e22b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e22b-114">PARAMETERS</span></span>

### <span data-ttu-id="4e22b-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="4e22b-115">-AsJob</span></span>
<span data-ttu-id="4e22b-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4e22b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e22b-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e22b-117">-Confirm</span></span>
<span data-ttu-id="4e22b-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e22b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e22b-119">-Default</span><span class="sxs-lookup"><span data-stu-id="4e22b-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="4e22b-120">Cosmos DB veritabanı hesabının varsayılan tutarlılık düzeyi.</span><span class="sxs-lookup"><span data-stu-id="4e22b-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="4e22b-121">Kabul edilen değerler: sıçrama durumu, tutarlılık, tutarlılık, son, oturum, güçlü</span><span class="sxs-lookup"><span data-stu-id="4e22b-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e22b-122">-DefaultProfile</span></span>
<span data-ttu-id="4e22b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e22b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e22b-124">-Disablekeybasevseçmetadatawriteaccess</span><span class="sxs-lookup"><span data-stu-id="4e22b-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="4e22b-125">Hesap anahtarları aracılığıyla meta veri kaynaklarında yazma işlemlerini devre dışı bırakma (veritabanları, kapsayıcılar, üretilen iş)</span><span class="sxs-lookup"><span data-stu-id="4e22b-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="4e22b-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="4e22b-127">Nadir olayda, bir kesinti nedeniyle kullanılamaz durumda olan yazma bölgesinin otomatik yük devretmesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="4e22b-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="4e22b-128">Otomatik yük devretme, hesabın yeni bir yazma bölgesine yol açabilir ve hesap için yapılandırılmış yük devretme önceliklerinin temel alınarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="4e22b-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="4e22b-129">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="4e22b-129">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="4e22b-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="4e22b-131">Birden çok yazma konumunu etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="4e22b-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="4e22b-132">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="4e22b-132">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4e22b-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="4e22b-134">Cosmos DB veritabanı hesabında sanal ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4e22b-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="4e22b-135">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="4e22b-135">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e22b-136">-InputObject</span></span>
<span data-ttu-id="4e22b-137">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="4e22b-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="4e22b-138">-IpRangeFilter</span></span>
<span data-ttu-id="4e22b-139">Güvenlik duvarı desteği.</span><span class="sxs-lookup"><span data-stu-id="4e22b-139">Firewall support.</span></span>
<span data-ttu-id="4e22b-140">Belirli bir veritabanı hesabı için izin verilen istemci IP 'Lerinin listesine eklenecek IP adresleri veya IP adresi aralıkları kümesini belirtir</span><span class="sxs-lookup"><span data-stu-id="4e22b-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="4e22b-141">-Maxstalenessıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="4e22b-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="4e22b-142">Bu değer, sınırlanmış Stalet tutarlılığı ile kullanıldığında, süre miktarının (TimeSpan olarak) toleranslı süresini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e22b-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="4e22b-143">Bu değer için kabul edilen Aralık 5-86400.</span><span class="sxs-lookup"><span data-stu-id="4e22b-143">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="4e22b-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="4e22b-145">Sınırlanmış uyumluluk tutarlılığı ile kullanıldığında, bu değer, toleransı yapılan eski isteklerin sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="4e22b-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="4e22b-146">Bu değer için kabul edilen Aralık 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="4e22b-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e22b-147">-Name</span></span>
<span data-ttu-id="4e22b-148">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="4e22b-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4e22b-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="4e22b-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="4e22b-150">Bu sunucuda genel uç noktası erişimine izin verilip verilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="4e22b-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="4e22b-151">Olası değerler: ' Enabled ', ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="4e22b-151">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e22b-152">-ResourceGroupName</span></span>
<span data-ttu-id="4e22b-153">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4e22b-153">Name of resource group.</span></span>

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

### <span data-ttu-id="4e22b-154">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4e22b-154">-ResourceId</span></span>
<span data-ttu-id="4e22b-155">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4e22b-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="4e22b-156">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4e22b-156">-Tag</span></span>
<span data-ttu-id="4e22b-157">Etiketlerin karma değer çiftleri olarak.</span><span class="sxs-lookup"><span data-stu-id="4e22b-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="4e22b-158">Var olan etiketi temizlemek için boş dize kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e22b-158">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4e22b-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="4e22b-160">Sanal ağ için ACL 'nin dize değerleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="4e22b-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="4e22b-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="4e22b-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="4e22b-162">Sanal ağ için PSVirtualNetworkRuleObjects dizisi.</span><span class="sxs-lookup"><span data-stu-id="4e22b-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e22b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e22b-163">-WhatIf</span></span>
<span data-ttu-id="4e22b-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e22b-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e22b-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e22b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e22b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e22b-166">CommonParameters</span></span>
<span data-ttu-id="4e22b-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e22b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e22b-168">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4e22b-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e22b-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e22b-169">INPUTS</span></span>

### <span data-ttu-id="4e22b-170">Microsoft. Azure. Commands. CosmosDB. modeller. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="4e22b-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="4e22b-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e22b-171">OUTPUTS</span></span>

### <span data-ttu-id="4e22b-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4e22b-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4e22b-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e22b-173">NOTES</span></span>

## <span data-ttu-id="4e22b-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e22b-174">RELATED LINKS</span></span>
