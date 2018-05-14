# <a name="table-of-contents"></a>İçindekiler
1. [Force parametrelerinin kaldırılması](#removal-of-force-parameters)
2. [Tag parametrelerinin değiştirilmesi](#change-of-tag-parameters)
3. [Depolama cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-storage-cmdlets)
4. [AD cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a>Force parametrelerinin kaldırılması

Bu sürümde, cmdlet’lerden tüm Eski `Force` parametrelerini ve parametrelerin gelecekteki bir sürümde kaldırılacağına ilişkin uyarıları kaldırdık.

Bu değişiklikten aşağıdaki cmdlet’ler etkilenir:

**ApiManagement**
- Remove-AzureRmApiManagement
- Remove-AzureRmApiManagementApi
- Remove-AzureRmApiManagementGroup
- Remove-AzureRmApiManagementLogger
- Remove-AzureRmApiManagementOpenIdConnectProvider
- Remove-AzureRmApiManagementOperation
- Remove-AzureRmApiManagementPolicy
- Remove-AzureRmApiManagementProduct
- Remove-AzureRmApiManagementProperty
- Remove-AzureRmApiManagementSubscription
- Remove-AzureRmApiManagementUser

**Otomasyon**
- Remove-AzureRmAutomationCertificate
- Remove-AzureRmAutomationCredential
- Remove-AzureRmAutomationVariable
- Remove-AzureRmAutomationWebhook

**Batch**
- Remove-AzureBatchCertificate
- Remove-AzureBatchComputeNode
- Remove-AzureBatchComputeNodeUser

**DataFactories**
- Resume-AzureRmDataFactoryPipeline
- Set-AzureRmDataFactoryPipelineActivePeriod
- Suspend-AzureRmDataFactoryPipeline

**DataLakeStore**
- Remove-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemAcl
- Set-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemOwner

**OperationalInsights**
- Remove-AzureRmOperationalInsightsSavedSearch

**Profil**
- Remove-AzureRmEnvironment

**RedisCache**
- Remove-AzureRmRedisCacheDiagnostics

**Kaynaklar**
- Register-AzureRmProviderFeature
- Register-AzureRmResourceProvider
- Remove-AzureRmADServicePrincipal
- Remove-AzureRmPolicyAssignment
- Remove-AzureRmResourceGroupDeployment
- Remove-AzureRmRoleAssignment
- Stop-AzureRmResourceGroupDeployment
- Unregister-AzureRmResourceProvider

**Depolama**
- Remove-AzureStorageContainerStoredAccessPolicy
- Remove-AzureStorageQueueStoredAccessPolicy
- Remove-AzureStorageShareStoredAccessPolicy
- Remove-AzureStorageTableStoredAccessPolicy

**StreamAnalytics**
- Remove-AzureRmStreamAnalyticsFunction
- Remove-AzureRmStreamAnalyticsInput
- Remove-AzureRmStreamAnalyticsJob
- Remove-AzureRmStreamAnalyticsOutput

**Tag**
- Remove-AzureRmTag

<br>

Yukarıdaki cmdlet'lerinden herhangi birini kullanan bir betiğiniz varsa `Force` parametresinin kaldırılması, bozucu değişikliğin düzeltilmesi için yeterlidir.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a>Tag parametrelerinin değiştirilmesi

Bu sürümde `Tags` parametresinin adı `Tag` olarak, `Hashtable[]` olan tür ise `Hashtable` olarak değiştirildiğinden, anahtar-değer eşleştirmelerinin biçimi değişmiştir.

Önceden her bir `Hashtable[]` girdisi tek bir anahtar-değer eşleştirmesini temsil ediyordu:

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

Şimdiyse `Name` ve `Value` artık gerekli olmadığından, `Hashtable`’da `Key = "Value"` atanarak anahtar-değer eşleştirmeleri oluşturulabilir:

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

Bu değişiklikten aşağıdaki cmdlet’ler etkilenir:

**Batch**
- Get-AzureRmBatchAccount
- New-AzureRmBatchAccount
- Set-AzureRmBatchAccount

**İşlem**
- New-AzureRmVM
- Update-AzureRmVM

**DataLakeAnalytics**
- New-AzureRmDataLakeAnalyticsAccount
- Set-AzureRmDataLakeAnalyticsAccount

**DataLakeStore**
- New-AzureRmDataLakeStoreAccount
- Set-AzureRmDataLakeStoreAccount

**Dns**
- New-AzureRmDnsZone
- Set-AzureRmDnsZone

**KeyVault**
- Get-AzureRmKeyVault
- New-AzureRmKeyVault

**Ağ**
- New-AzureRmApplicationGateway
- New-AzureRmExpressRouteCircuit
- New-AzureRmLoadBalancer
- New-AzureRmLocalNetworkGateway
- New-AzureRmNetworkInterface
- New-AzureRmNetworkSecurityGroup
- New-AzureRmPublicIpAddress
- New-AzureRmRouteTable
- New-AzureRmVirtualNetwork
- New-AzureRmVirtualNetworkGateway
- New-AzureRmVirtualNetworkGatewayConnection
- New-AzureRmVirtualNetworkPeering

**Kaynaklar**
- Find-AzureRmResource
- Find-AzureRmResourceGroup
- New-AzureRmResource
- New-AzureRmResourceGroup
- Set-AzureRmResource
- Set-AzureRmResourceGroup

**SQL**
- New-AzureRmSqlDatabase
- New-AzureRmSqlDatabaseCopy
- New-AzureRmSqlDatabaseSecondary
- New-AzureRmSqlElasticPool
- New-AzureRmSqlServer
- Set-AzureRmSqlDatabase
- Set-AzureRmSqlElasticPool
- Set-AzureRmSqlServer

**Depolama**
- New-AzureRmStorageAccount
- Set-AzureRmStorageAccount

**TrafficManager**
- New-AzureRmTrafficManagerProfile

<br>

Yukarıdaki cmdlet'lerinden herhangi birini kullanan bir betiğiniz varsa, bozucu değişiklik `Tags` parametresinin `Tag` olarak değiştirilmesinin yanı sıra `Tag` öğesinin yeni biçime değiştirilmesi ile düzeltilebilir.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a>Depolama cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki cmdlet’ler etkilenir:

**Get-AzureRmStorageAccountKey**
- Bu cmdlet artık her anahtarın özelliklerini içeren bir nesne yerine anahtarların listesini döndürür

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

**New-AzureRmStorageAccountKey**
- Bu cmdlet’in çıktısındaki `StorageAccountRegenerateKeyResponse` alanı, artık her anahtarın özelliklerini içeren bir nesne yerine anahtarların listesi olan `StorageAccountListKeysResults` olarak yeniden adlandırıldı

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

**New/Get/Set-AzureRmStorageAccount**
- Bu cmdlet’in çıktısındaki `AccountType` alanı, `Sku.Name` olarak yeniden adlandırıldı
- Birincil uç noktalar/İkincil uç noktalar blob/tablo/kuyruk/dosya için `Uri` olan çıktı türü `String` olarak değiştirildi

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a>AD cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:

**Get-AzureRMADServicePrincipal**
- Bu cmdlet’in çıktısındaki `ServicePrincipalName` alanı, `ServicePrincipalNames` olarak yeniden adlandırıldı ve bir koleksiyona dönüştürüldü. Artık identifierUri’nin yanı sıra bir SPN olarak `ApplicationId`’yi de görüntülüyor.

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

**Get-AzureRmADApplication**
- `ApplicationObjectId` parametresi `ObjectId` olarak yeniden adlandırıldı.
- Bu cmdlet’in çıktısındaki `ApplicationObjectId`, `ObjectId` olarak yeniden adlandırıldı.

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

**Remove-AzureRmADApplication**
- `ApplicationObjectId` parametresi `ObjectId` olarak yeniden adlandırıldı.

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

**New-AzureRmADApplication**
- Bu cmdlet’in çıktısındaki `ApplicationObjectId`, `ObjectId` olarak yeniden adlandırıldı.
- `KeyValue`, `KeyUsage`, `KeyType` parametreleri kaldırıldı.

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

**Get-AzureRmADGroup**
- `Mail` alanı çıktıdan kaldırıldı.

**Get-AzureRmADUser**
- `Mail` alanı çıktıdan kaldırıldı.

**New-AzureRmADServicePrincipal**
- `DisableAccount` parametresi kaldırıldı.

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```