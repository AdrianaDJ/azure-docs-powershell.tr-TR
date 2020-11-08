---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267853"
---
# <span data-ttu-id="2ff0d-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="2ff0d-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="2ff0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff0d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff0d-103">CosmosDB hesap özniteliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="2ff0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ff0d-104">SYNTAX</span></span>

### <span data-ttu-id="2ff0d-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ff0d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff0d-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2ff0d-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff0d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff0d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff0d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ff0d-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff0d-109">CosmosDB hesabının özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="2ff0d-110">Diğer özelliklerle simulataneously hesap bölgeleri güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="2ff0d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ff0d-111">EXAMPLES</span></span>

### <span data-ttu-id="2ff0d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ff0d-112">Example 1</span></span>
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

<span data-ttu-id="2ff0d-113">Defaultbir "ad. düzey", "Strong", otomatik yeniden yük devri, etkin çoğul</span><span class="sxs-lookup"><span data-stu-id="2ff0d-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="2ff0d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ff0d-114">PARAMETERS</span></span>

### <span data-ttu-id="2ff0d-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ff0d-115">-AsJob</span></span>
<span data-ttu-id="2ff0d-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2ff0d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ff0d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ff0d-117">-Confirm</span></span>
<span data-ttu-id="2ff0d-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff0d-119">-Default</span><span class="sxs-lookup"><span data-stu-id="2ff0d-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="2ff0d-120">Cosmos DB veritabanı hesabının varsayılan tutarlılık düzeyi.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="2ff0d-121">Kabul edilen değerler: sıçrama durumu, tutarlılık, tutarlılık, son, oturum, güçlü</span><span class="sxs-lookup"><span data-stu-id="2ff0d-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="2ff0d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff0d-122">-DefaultProfile</span></span>
<span data-ttu-id="2ff0d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff0d-124">-Disablekeybasevseçmetadatawriteaccess</span><span class="sxs-lookup"><span data-stu-id="2ff0d-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="2ff0d-125">Hesap anahtarları aracılığıyla meta veri kaynaklarında yazma işlemlerini devre dışı bırakma (veritabanları, kapsayıcılar, üretilen iş)</span><span class="sxs-lookup"><span data-stu-id="2ff0d-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="2ff0d-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="2ff0d-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="2ff0d-127">Bool, hesapta AnalyticalStorage 'in etkinleştirilip etkinleştirilmediğini belirtecek şekilde Boole.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="2ff0d-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="2ff0d-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="2ff0d-129">Nadir olayda, bir kesinti nedeniyle kullanılamaz durumda olan yazma bölgesinin otomatik yük devretmesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="2ff0d-130">Otomatik yük devretme, hesabın yeni bir yazma bölgesine yol açabilir ve hesap için yapılandırılmış yük devretme önceliklerinin temel alınarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="2ff0d-131">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="2ff0d-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="2ff0d-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="2ff0d-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="2ff0d-133">Birden çok yazma konumunu etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="2ff0d-134">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="2ff0d-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="2ff0d-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2ff0d-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="2ff0d-136">Cosmos DB veritabanı hesabında sanal ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="2ff0d-137">Kabul edilen değerler: yanlış, doğru</span><span class="sxs-lookup"><span data-stu-id="2ff0d-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="2ff0d-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ff0d-138">-InputObject</span></span>
<span data-ttu-id="2ff0d-139">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="2ff0d-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2ff0d-140">-Iprule</span><span class="sxs-lookup"><span data-stu-id="2ff0d-140">-IpRule</span></span>
<span data-ttu-id="2ff0d-141">Güvenlik duvarı desteği.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-141">Firewall support.</span></span> <span data-ttu-id="2ff0d-142">Belirli bir veritabanı hesabı için izin verilen istemci IP 'Lerinin listesine eklenecek IP adresleri veya IP adresi aralıkları kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="2ff0d-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="2ff0d-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="2ff0d-144">Tuş Kasası URI 'SI</span><span class="sxs-lookup"><span data-stu-id="2ff0d-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="2ff0d-145">-Maxstalenessıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="2ff0d-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="2ff0d-146">Bu değer, sınırlanmış Stalet tutarlılığı ile kullanıldığında, süre miktarının (TimeSpan olarak) toleranslı süresini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="2ff0d-147">Bu değer için kabul edilen Aralık 5-86400.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="2ff0d-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="2ff0d-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="2ff0d-149">Sınırlanmış uyumluluk tutarlılığı ile kullanıldığında, bu değer, toleransı yapılan eski isteklerin sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="2ff0d-150">Bu değer için kabul edilen Aralık 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="2ff0d-151">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ff0d-151">-Name</span></span>
<span data-ttu-id="2ff0d-152">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ff0d-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2ff0d-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="2ff0d-154">Bu sunucuda genel uç noktası erişimine izin verilip verilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="2ff0d-155">Olası değerler: ' Enabled ', ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="2ff0d-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="2ff0d-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff0d-156">-ResourceGroupName</span></span>
<span data-ttu-id="2ff0d-157">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-157">Name of resource group.</span></span>

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

### <span data-ttu-id="2ff0d-158">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ff0d-158">-ResourceId</span></span>
<span data-ttu-id="2ff0d-159">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2ff0d-160">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2ff0d-160">-Tag</span></span>
<span data-ttu-id="2ff0d-161">Etiketlerin karma değer çiftleri olarak.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="2ff0d-162">Var olan etiketi temizlemek için boş dize kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="2ff0d-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2ff0d-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="2ff0d-164">Sanal ağ için ACL 'nin dize değerleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="2ff0d-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="2ff0d-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="2ff0d-166">Sanal ağ için PSVirtualNetworkRuleObjects dizisi.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="2ff0d-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff0d-167">-WhatIf</span></span>
<span data-ttu-id="2ff0d-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff0d-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff0d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff0d-170">CommonParameters</span></span>
<span data-ttu-id="2ff0d-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff0d-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ff0d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff0d-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ff0d-173">INPUTS</span></span>

### <span data-ttu-id="2ff0d-174">Microsoft. Azure. Commands. CosmosDB. modeller. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="2ff0d-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="2ff0d-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ff0d-175">OUTPUTS</span></span>

### <span data-ttu-id="2ff0d-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2ff0d-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2ff0d-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ff0d-177">NOTES</span></span>

## <span data-ttu-id="2ff0d-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ff0d-178">RELATED LINKS</span></span>
