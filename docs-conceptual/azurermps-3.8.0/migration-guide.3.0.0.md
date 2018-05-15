# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="40314-101">Microsoft Azure PowerShell 3.0.0 için bozucu değişiklikler.</span><span class="sxs-lookup"><span data-stu-id="40314-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="40314-102">Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="40314-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="40314-103">Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır.</span><span class="sxs-lookup"><span data-stu-id="40314-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="40314-104">Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="40314-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="40314-105">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="40314-105">Table of Contents</span></span>
1. [<span data-ttu-id="40314-106">Data Lake Store cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="40314-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="40314-107">ApiManagement cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="40314-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="40314-108">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="40314-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="40314-109">Data Lake Store cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="40314-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="40314-110">Bu sürümden ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="40314-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="40314-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="40314-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="40314-112">Bu cmdlet kaldırılıp ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="40314-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="40314-113">Eski cmdlet, erişim denetim listesini (ACL) temsil eden karmaşık bir nesne döndürüyordu.</span><span class="sxs-lookup"><span data-stu-id="40314-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="40314-114">Yeni cmdlet, seçilen yolun ACL'sindeki girdilerin basit bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="40314-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="40314-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="40314-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="40314-116">Bu cmdlet, eski ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` cmdletinin yerini alır.</span><span class="sxs-lookup"><span data-stu-id="40314-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="40314-117">Bu yeni cmdlet, ``DataLakeStoreItemAce[]`` türü ile seçilen yolun ACL'sindeki girdilerin basit bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="40314-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="40314-118">Bu cmdlet'in çıktısı, aşağıdaki cmdlet’lerin ``-Acl`` parametresine geçirilebilir:</span><span class="sxs-lookup"><span data-stu-id="40314-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="40314-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="40314-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="40314-120">Bu cmdlet’ler artık ``-Acl`` parametresi için ``DataLakeStoreItemAce[]`` kabul eder.</span><span class="sxs-lookup"><span data-stu-id="40314-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="40314-121">``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` tarafından ``DataLakeStoreItemAce[]`` döndürülür.</span><span class="sxs-lookup"><span data-stu-id="40314-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="40314-122">ApiManagement cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="40314-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="40314-123">Bu sürümden ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="40314-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="40314-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="40314-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="40314-125">Bir sanal ağa başvurmak için gerekli olan SubnetName ve VnetId parametrelerinin yerini ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}`` biçimindeki SubnetResourceId almıştır</span><span class="sxs-lookup"><span data-stu-id="40314-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="40314-126">**Set-AzureRmApiManagementVirtualNetworks Cmdlet’i Kullanım Dışı Bırakılıyor**</span><span class="sxs-lookup"><span data-stu-id="40314-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="40314-127">ApiManagement dağıtımıyla ilişkili Sanal Ağ Ayarlamanın birden çok yolu olduğundan bu Cmdlet kullanım dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="40314-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="40314-128">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="40314-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="40314-129">Bu sürümden ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="40314-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="40314-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="40314-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="40314-131">Değişikliklerin açıklaması ``:- Bool parameter:-ActiveActive`` kaldırıldı ve yeni oluşturulan sanal ağ geçidinde Etkin-Etkin özelliğinin etkinleştirilmesi için ``SwitchParameter:-EnableActiveActiveFeature`` eklendi.</span><span class="sxs-lookup"><span data-stu-id="40314-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="40314-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40314-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="40314-133">Değişikliklerin açıklaması ``:- Bool parameter:-ActiveActive`` kaldırıldı ve sanal ağ geçidinde Etkin-Etkin özelliğinin etkinleştirilip devre dışı bırakılması için 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` eklendi.</span><span class="sxs-lookup"><span data-stu-id="40314-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```