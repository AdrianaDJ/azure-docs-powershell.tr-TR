---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274225"
---
# <span data-ttu-id="0732b-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="0732b-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="0732b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0732b-102">SYNOPSIS</span></span>
<span data-ttu-id="0732b-103">Tanımlı ve verilen parametre değerleriyle eşleşen Azure sağlayıcısı kaynak türlerini alır ve bu kaynakları alır Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="0732b-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="0732b-104">Parametre sağlanmadıysa, diğer ad içeren tüm sağlayıcı kaynak türleri çıktı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="0732b-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="0732b-105">-ListAvailable anahtarı, diğer adlar olmadan eşleşen tüm kaynak türlerini listeleyerek bu davranışı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0732b-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="0732b-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0732b-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0732b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0732b-107">DESCRIPTION</span></span>
<span data-ttu-id="0732b-108">**Get-Azpolicyalıas** cmdlet 'i, ilke diğer adlarının bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0732b-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="0732b-109">İlke diğer adları, kaynak türü özelliklerine başvuruda bulunmak için Azure Ilkesi tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0732b-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="0732b-110">Kaynak türünün veya diğer adlarının çeşitli özelliklerini eşleştirerek listede öğeleri sınırlayan parametreler sağlanır.</span><span class="sxs-lookup"><span data-stu-id="0732b-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="0732b-111">Verilen eşleşme değeri, hedef dize büyük/küçük harf duyarsız karşılaştırmayı kullanarak içeriyorsa eşleşir.</span><span class="sxs-lookup"><span data-stu-id="0732b-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="0732b-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0732b-112">EXAMPLES</span></span>

### <span data-ttu-id="0732b-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0732b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

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

<span data-ttu-id="0732b-114">Diğer adı olan tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0732b-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="0732b-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0732b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="0732b-116">Diğer ad içermeyen olanlar da içinde olmak üzere tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0732b-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="0732b-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0732b-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="0732b-118">Ad alanı ' COMPUTE ' ile eşleşen ve diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0732b-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="0732b-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="0732b-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

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

<span data-ttu-id="0732b-120">Kaynak türü ' sanal ' ile eşleşen ve diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0732b-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="0732b-121">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="0732b-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

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

<span data-ttu-id="0732b-122">Kaynak türü, diğer adları olmayan ' sanal ' ile eşleşen tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0732b-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="0732b-123">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="0732b-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="0732b-124">Ad alanı ' COMPUTE ' ve kaynak türüyle eşleşen tüm sağlayıcı kaynak türlerini listeler ' sanal ' ile eşleşiyor ve bir diğer ad içeriyor.</span><span class="sxs-lookup"><span data-stu-id="0732b-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="0732b-125">Not:-NamespaceMatch ve-Resourcettypeınfo, diğerleri dahil olmak üzere özel eşleşmeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="0732b-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="0732b-126">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="0732b-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

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

<span data-ttu-id="0732b-127">' Sanal ' ile eşleşen diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0732b-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="0732b-128">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="0732b-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

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

<span data-ttu-id="0732b-129">Eşleşen bir diğer ad veya ' ağ ' ile eşleşen bir diğer ad içeren tüm sağlayıcı kaynak türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0732b-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="0732b-130">Örnek 9</span><span class="sxs-lookup"><span data-stu-id="0732b-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="0732b-131">Alpha API sürümü ile tüm sağlayıcı kaynak türlerini listeler veya Alfa API sürümü olan diğer ad içerir.</span><span class="sxs-lookup"><span data-stu-id="0732b-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="0732b-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0732b-132">PARAMETERS</span></span>

### <span data-ttu-id="0732b-133">-Diğerad eşleştirme</span><span class="sxs-lookup"><span data-stu-id="0732b-133">-AliasMatch</span></span>
<span data-ttu-id="0732b-134">Adı bu değerle eşleşen diğer adlara sahip çıkış öğelerine dahildir.</span><span class="sxs-lookup"><span data-stu-id="0732b-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-135">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0732b-135">-ApiVersion</span></span>
<span data-ttu-id="0732b-136">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="0732b-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="0732b-137">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0732b-137">If not specified, the API version is automatically determined as the latest available.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-138">-Apıversionmatch</span><span class="sxs-lookup"><span data-stu-id="0732b-138">-ApiVersionMatch</span></span>
<span data-ttu-id="0732b-139">Kaynak türlerinin veya diğer adlarının eşleşen API sürümüne sahip olduğu çıkış öğelerine dahildir.</span><span class="sxs-lookup"><span data-stu-id="0732b-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0732b-140">-DefaultProfile</span></span>
<span data-ttu-id="0732b-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0732b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0732b-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="0732b-142">-ListAvailable</span></span>
<span data-ttu-id="0732b-143">Diğer ad içeren ve bulunmayan çıkış eşleştirmesi öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="0732b-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="0732b-144">-LocationMatch</span></span>
<span data-ttu-id="0732b-145">Kaynak türlerinin eşleşen bir konumuna sahip olduğu çıkış öğelerine dahildir.</span><span class="sxs-lookup"><span data-stu-id="0732b-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="0732b-146">-NamespaceMatch</span></span>
<span data-ttu-id="0732b-147">Çıktıyı, ad alanı bu değerle eşleşen öğelerle sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="0732b-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="0732b-148">-PathMatch</span></span>
<span data-ttu-id="0732b-149">Bu değerle eşleşen bir yol içeren diğer ad içeren çıkış öğelerine ekler.</span><span class="sxs-lookup"><span data-stu-id="0732b-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-150">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0732b-150">-Pre</span></span>
<span data-ttu-id="0732b-151">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0732b-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-152">-Resourcettypeınfo</span><span class="sxs-lookup"><span data-stu-id="0732b-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="0732b-153">Çıktıyı, kaynak türü bu değerle eşleşen öğelerle sınırlar.</span><span class="sxs-lookup"><span data-stu-id="0732b-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0732b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0732b-154">CommonParameters</span></span>
<span data-ttu-id="0732b-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0732b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0732b-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0732b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0732b-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0732b-157">INPUTS</span></span>

### <span data-ttu-id="0732b-158">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0732b-158">None</span></span>

## <span data-ttu-id="0732b-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0732b-159">OUTPUTS</span></span>

### <span data-ttu-id="0732b-160">Microsoft. Azure. Commands. ResourceManager. cmdlet. Implementation. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="0732b-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="0732b-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0732b-161">NOTES</span></span>

* <span data-ttu-id="0732b-162">Diğer adları veya diğer herhangi bir özelliği genişletmek için, çıktıyı boru yapın `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="0732b-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="0732b-163">Örneğin: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="0732b-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="0732b-164">Çıktıda ek özellikler kullanılabilir ve çıktının boru tarafından görüntülenebilir `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="0732b-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="0732b-165">Örneğin: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="0732b-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="0732b-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0732b-166">RELATED LINKS</span></span>
