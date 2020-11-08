---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRm.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyalias
schema: 2.0.0
ms.openlocfilehash: f0f8f3ded2697e713215929f66ebd82b3af03ea0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939487"
---
# <span data-ttu-id="af484-101">Get-AzureRmPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="af484-101">Get-AzureRmPolicyAlias</span></span>

## <span data-ttu-id="af484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af484-102">SYNOPSIS</span></span>
<span data-ttu-id="af484-103">Tanımlı ve verilen parametre değerleriyle eşleşen Azure sağlayıcısı kaynak türlerini alır ve bu kaynakları alır Get-AzureRmPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="af484-103">Get-AzureRmPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="af484-104">Parametre sağlanmadıysa, diğer ad içeren tüm sağlayıcı kaynak türleri çıktı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="af484-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="af484-105">-ListAvailable anahtarı, diğer adlar olmadan eşleşen tüm kaynak türlerini listeleyerek bu davranışı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af484-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af484-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af484-106">SYNTAX</span></span>

```
Get-AzureRmPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af484-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af484-107">DESCRIPTION</span></span>
<span data-ttu-id="af484-108">**Get-AzureRmPolicyAlias** cmdlet 'i ilke diğer adlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="af484-108">The **Get-AzureRmPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="af484-109">İlke diğer adları, kaynak türü özelliklerine başvuruda bulunmak için Azure Ilkesi tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af484-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="af484-110">Kaynak türünün veya diğer adlarının çeşitli özelliklerini eşleştirerek listede öğeleri sınırlayan parametreler sağlanır.</span><span class="sxs-lookup"><span data-stu-id="af484-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="af484-111">Verilen eşleşme değeri, hedef dize büyük/küçük harf duyarsız karşılaştırmayı kullanarak içeriyorsa eşleşir.</span><span class="sxs-lookup"><span data-stu-id="af484-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="af484-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af484-112">EXAMPLES</span></span>

### <span data-ttu-id="af484-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af484-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="af484-114">Diğer adı olan tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af484-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="af484-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="af484-115">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="af484-116">Diğer ad içermeyen olanlar da içinde olmak üzere tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af484-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="af484-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="af484-117">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="af484-118">Ad alanı ' COMPUTE ' ile eşleşen ve diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af484-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="af484-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="af484-119">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="af484-120">Kaynak türü ' sanal ' ile eşleşen ve diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af484-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="af484-121">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="af484-121">Example 5</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="af484-122">Kaynak türü, diğer adları olmayan ' sanal ' ile eşleşen tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af484-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="af484-123">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="af484-123">Example 6</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="af484-124">Ad alanı ' COMPUTE ' ve kaynak türüyle eşleşen tüm sağlayıcı kaynak türlerini listeler ' sanal ' ile eşleşiyor ve bir diğer ad içeriyor.</span><span class="sxs-lookup"><span data-stu-id="af484-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="af484-125">Not:-NamespaceMatch ve-Resourcettypeınfo, diğerleri dahil olmak üzere özel eşleşmeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="af484-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="af484-126">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="af484-126">Example 7</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="af484-127">' Sanal ' ile eşleşen diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af484-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="af484-128">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="af484-128">Example 8</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="af484-129">Eşleşen bir diğer ad veya ' ağ ' ile eşleşen bir diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af484-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="af484-130">Örnek 9</span><span class="sxs-lookup"><span data-stu-id="af484-130">Example 9</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="af484-131">Alpha API sürümü ile tüm sağlayıcı kaynak türlerini listeler veya Alfa API sürümü olan diğer ad içerir.</span><span class="sxs-lookup"><span data-stu-id="af484-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="af484-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af484-132">PARAMETERS</span></span>

### <span data-ttu-id="af484-133">-Diğerad eşleştirme</span><span class="sxs-lookup"><span data-stu-id="af484-133">-AliasMatch</span></span>
<span data-ttu-id="af484-134">Adı bu değerle eşleşen diğer adlara sahip çıkış öğelerine dahildir.</span><span class="sxs-lookup"><span data-stu-id="af484-134">Includes in the output items with aliases whose name matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af484-135">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="af484-135">-ApiVersion</span></span>
<span data-ttu-id="af484-136">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="af484-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="af484-137">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="af484-137">If not specified, the API version is automatically determined as the latest available.</span></span>
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

### <span data-ttu-id="af484-138">-Apıversionmatch</span><span class="sxs-lookup"><span data-stu-id="af484-138">-ApiVersionMatch</span></span>
<span data-ttu-id="af484-139">Kaynak türlerinin veya diğer adlarının eşleşen API sürümüne sahip olduğu çıkış öğelerine dahildir.</span><span class="sxs-lookup"><span data-stu-id="af484-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>
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

### <span data-ttu-id="af484-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af484-140">-DefaultProfile</span></span>
<span data-ttu-id="af484-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af484-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af484-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="af484-142">-ListAvailable</span></span>
<span data-ttu-id="af484-143">Diğer ad içeren ve bulunmayan çıkış eşleştirmesi öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="af484-143">Includes in the output matching items with and without aliases.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af484-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="af484-144">-LocationMatch</span></span>
<span data-ttu-id="af484-145">Kaynak türlerinin eşleşen bir konumuna sahip olduğu çıkış öğelerine dahildir.</span><span class="sxs-lookup"><span data-stu-id="af484-145">Includes in the output items whose resource types have a matching location.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af484-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="af484-146">-NamespaceMatch</span></span>
<span data-ttu-id="af484-147">Çıktıyı, ad alanı bu değerle eşleşen öğelerle sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="af484-147">Limits the output to items whose namespace matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af484-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="af484-148">-PathMatch</span></span>
<span data-ttu-id="af484-149">Bu değerle eşleşen bir yol içeren diğer ad içeren çıkış öğelerine ekler.</span><span class="sxs-lookup"><span data-stu-id="af484-149">Includes in the output items with aliases containing a path that matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af484-150">-Pre-</span><span class="sxs-lookup"><span data-stu-id="af484-150">-Pre</span></span>
<span data-ttu-id="af484-151">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af484-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>
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

### <span data-ttu-id="af484-152">-Resourcettypeınfo</span><span class="sxs-lookup"><span data-stu-id="af484-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="af484-153">Çıktıyı, kaynak türü bu değerle eşleşen öğelerle sınırlar.</span><span class="sxs-lookup"><span data-stu-id="af484-153">Limits the output to items whose resource type matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af484-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af484-154">CommonParameters</span></span>
<span data-ttu-id="af484-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af484-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af484-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af484-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af484-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af484-157">INPUTS</span></span>

## <span data-ttu-id="af484-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af484-158">OUTPUTS</span></span>

### <span data-ttu-id="af484-159">Microsoft. Azure. Commands. ResourceManager. cmdlet. Implementation. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="af484-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="af484-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af484-160">NOTES</span></span>

* <span data-ttu-id="af484-161">Diğer adları veya diğer herhangi bir özelliği genişletmek için, çıktıyı boru yapın `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="af484-161">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="af484-162">Örneğin: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="af484-162">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="af484-163">Çıktıda ek özellikler kullanılabilir ve çıktının boru tarafından görüntülenebilir `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="af484-163">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="af484-164">Örneğin: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="af484-164">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="af484-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af484-165">RELATED LINKS</span></span>