---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321594"
---
# <span data-ttu-id="b5667-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b5667-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b5667-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5667-102">SYNOPSIS</span></span>
<span data-ttu-id="b5667-103">Yeni bir CosmosDB hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b5667-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="b5667-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5667-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5667-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5667-105">DESCRIPTION</span></span>
<span data-ttu-id="b5667-106">Verilen ResourceGroup 'ta yeni bir CosmosDB hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b5667-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="b5667-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5667-107">EXAMPLES</span></span>

### <span data-ttu-id="b5667-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5667-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="b5667-109">ResourceGroup resourceGroupName içinde adı databaseAccountName olan yeni bir CosmosDB hesabı oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="b5667-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="b5667-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5667-110">PARAMETERS</span></span>

### <span data-ttu-id="b5667-111">-Apıkind</span><span class="sxs-lookup"><span data-stu-id="b5667-111">-ApiKind</span></span>
<span data-ttu-id="b5667-112">Oluşturulacak Cosmos DB veritabanı hesabının türü.</span><span class="sxs-lookup"><span data-stu-id="b5667-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="b5667-113">Kabul edilen değerler: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="b5667-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="b5667-114">Varsayılan değer: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="b5667-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="b5667-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="b5667-115">-AsJob</span></span>
<span data-ttu-id="b5667-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b5667-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5667-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5667-117">-Confirm</span></span>
<span data-ttu-id="b5667-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5667-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5667-119">-Default</span><span class="sxs-lookup"><span data-stu-id="b5667-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="b5667-120">Cosmos DB veritabanı hesabının varsayılan tutarlılık düzeyi.</span><span class="sxs-lookup"><span data-stu-id="b5667-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="b5667-121">Kabul edilen değerler: sıçrama durumu, tutarlılık, tutarlılık, son, oturum, güçlü</span><span class="sxs-lookup"><span data-stu-id="b5667-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="b5667-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5667-122">-DefaultProfile</span></span>
<span data-ttu-id="b5667-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5667-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5667-124">-Disablekeybasevseçmetadatawriteaccess</span><span class="sxs-lookup"><span data-stu-id="b5667-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="b5667-125">Hesap anahtarları aracılığıyla meta veri kaynaklarında yazma işlemlerini devre dışı bırakma (veritabanları, kapsayıcılar, üretilen iş)</span><span class="sxs-lookup"><span data-stu-id="b5667-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="b5667-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="b5667-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="b5667-127">Bool, hesapta AnalyticalStorage 'in etkinleştirilip etkinleştirilmediğini belirtecek şekilde Boole.</span><span class="sxs-lookup"><span data-stu-id="b5667-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="b5667-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="b5667-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="b5667-129">Nadir olayda, bir kesinti nedeniyle kullanılamaz durumda olan yazma bölgesinin otomatik yük devretmesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="b5667-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="b5667-130">Otomatik yük devretme, hesabın yeni bir yazma bölgesine yol açabilir ve hesap için yapılandırılmış yük devretme önceliklerinin temel alınarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="b5667-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="b5667-131">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="b5667-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b5667-132">-Enabsolreetier</span><span class="sxs-lookup"><span data-stu-id="b5667-132">-EnableFreeTier</span></span>
<span data-ttu-id="b5667-133">Bool, hesapta Freren 'in etkinleştirilip etkinleştirilmediğini belirtmek için Boole.</span><span class="sxs-lookup"><span data-stu-id="b5667-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="b5667-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="b5667-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="b5667-135">Birden çok yazma konumunu etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="b5667-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="b5667-136">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="b5667-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b5667-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b5667-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="b5667-138">Cosmos DB veritabanı hesabında sanal ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b5667-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="b5667-139">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="b5667-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b5667-140">-Iprule</span><span class="sxs-lookup"><span data-stu-id="b5667-140">-IpRule</span></span>
<span data-ttu-id="b5667-141">Güvenlik duvarı desteği.</span><span class="sxs-lookup"><span data-stu-id="b5667-141">Firewall support.</span></span> <span data-ttu-id="b5667-142">Belirli bir veritabanı hesabı için izin verilen istemci IP 'Lerinin listesine eklenecek IP adresleri veya IP adresi aralıkları kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5667-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="b5667-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b5667-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="b5667-144">Tuş Kasası URI 'SI</span><span class="sxs-lookup"><span data-stu-id="b5667-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="b5667-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="b5667-145">-Location</span></span>
<span data-ttu-id="b5667-146">Cosmos DB veritabanı hesabına konum ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b5667-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="b5667-147">Yük devretme önceliğine göre sıralanan dizeler dizisi.</span><span class="sxs-lookup"><span data-stu-id="b5667-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="b5667-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="b5667-148">-LocationObject</span></span>
<span data-ttu-id="b5667-149">Cosmos DB veritabanı hesabına konum ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b5667-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="b5667-150">PSLocation nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="b5667-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="b5667-151">-Maxstalenessıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="b5667-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="b5667-152">Bu değer, sınırlanmış Stalet tutarlılığı ile kullanıldığında, süre miktarının (TimeSpan olarak) toleranslı süresini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5667-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="b5667-153">Bu değer için kabul edilen Aralık 5-86400.</span><span class="sxs-lookup"><span data-stu-id="b5667-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="b5667-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="b5667-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="b5667-155">Sınırlanmış uyumluluk tutarlılığı ile kullanıldığında, bu değer, toleransı yapılan eski isteklerin sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b5667-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="b5667-156">Bu değer için kabul edilen Aralık 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="b5667-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="b5667-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5667-157">-Name</span></span>
<span data-ttu-id="b5667-158">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b5667-158">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5667-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b5667-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="b5667-160">Bu sunucuda genel uç noktası erişimine izin verilip verilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="b5667-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="b5667-161">Olası değerler: ' Enabled ', ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="b5667-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="b5667-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5667-162">-ResourceGroupName</span></span>
<span data-ttu-id="b5667-163">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b5667-163">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5667-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b5667-164">-ServerVersion</span></span>
<span data-ttu-id="b5667-165">ServerVersion, yalnızca MongoDB hesaplarında geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b5667-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="b5667-166">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b5667-166">-Tag</span></span>
<span data-ttu-id="b5667-167">Etiketlerin karma değer çiftleri olarak.</span><span class="sxs-lookup"><span data-stu-id="b5667-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="b5667-168">Var olan etiketi temizlemek için boş dize kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5667-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="b5667-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b5667-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="b5667-170">Sanal ağ için ACL 'nin dize değerleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="b5667-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="b5667-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b5667-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="b5667-172">Sanal ağ için PSVirtualNetworkRuleObjects dizisi.</span><span class="sxs-lookup"><span data-stu-id="b5667-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5667-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5667-173">-WhatIf</span></span>
<span data-ttu-id="b5667-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5667-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5667-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5667-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5667-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5667-176">CommonParameters</span></span>
<span data-ttu-id="b5667-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5667-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5667-178">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5667-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5667-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5667-179">INPUTS</span></span>

### <span data-ttu-id="b5667-180">Microsoft. Azure. Commands. CosmosDB. modeller. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="b5667-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="b5667-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5667-181">OUTPUTS</span></span>

### <span data-ttu-id="b5667-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b5667-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b5667-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5667-183">NOTES</span></span>

## <span data-ttu-id="b5667-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5667-184">RELATED LINKS</span></span>
