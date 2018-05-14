# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Microsoft Azure PowerShell 3.0.0 için bozucu değişiklikler.

Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır.  Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır.  Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.

## <a name="table-of-contents"></a>İçindekiler
1. [Data Lake Store cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-data-lake-store-cmdlets)
2. [ApiManagement cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-apimanagement-cmdlets)
3. [Ağ cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Data Lake Store cmdlet’lerinde bozucu değişiklikler

Bu sürümden ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) aşağıdaki cmdlet’ler etkilenmiştir:

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- Bu cmdlet kaldırılıp ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` ile değiştirilmiştir.
- Eski cmdlet, erişim denetim listesini (ACL) temsil eden karmaşık bir nesne döndürüyordu. Yeni cmdlet, seçilen yolun ACL'sindeki girdilerin basit bir listesini döndürür.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- Bu cmdlet, eski ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` cmdletinin yerini alır.
- Bu yeni cmdlet, ``DataLakeStoreItemAce[]`` türü ile seçilen yolun ACL'sindeki girdilerin basit bir listesini döndürür.
- Bu cmdlet'in çıktısı, aşağıdaki cmdlet’lerin ``-Acl`` parametresine geçirilebilir:
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- Bu cmdlet’ler artık ``-Acl`` parametresi için ``DataLakeStoreItemAce[]`` kabul eder.
- ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)`` tarafından ``DataLakeStoreItemAce[]`` döndürülür.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>ApiManagement cmdlet’lerinde bozucu değişiklikler

Bu sürümden ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) aşağıdaki cmdlet’ler etkilenmiştir:

**New-AzureRmApiManagementVirtualNetwork**
- Bir sanal ağa başvurmak için gerekli olan SubnetName ve VnetId parametrelerinin yerini ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}`` biçimindeki SubnetResourceId almıştır

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Set-AzureRmApiManagementVirtualNetworks Cmdlet’i Kullanım Dışı Bırakılıyor**
- ApiManagement dağıtımıyla ilişkili Sanal Ağ Ayarlamanın birden çok yolu olduğundan bu Cmdlet kullanım dışı bırakılıyor.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Ağ cmdlet’lerinde bozucu değişiklikler

Bu sürümden ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) aşağıdaki cmdlet’ler etkilenmiştir:

**New-AzureRmVirtualNetworkGateway**
- Değişikliklerin açıklaması ``:- Bool parameter:-ActiveActive`` kaldırıldı ve yeni oluşturulan sanal ağ geçidinde Etkin-Etkin özelliğinin etkinleştirilmesi için ``SwitchParameter:-EnableActiveActiveFeature`` eklendi.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- Değişikliklerin açıklaması ``:- Bool parameter:-ActiveActive`` kaldırıldı ve sanal ağ geçidinde Etkin-Etkin özelliğinin etkinleştirilip devre dışı bırakılması için 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` eklendi.

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