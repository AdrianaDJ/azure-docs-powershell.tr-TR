---
title: Microsoft Azure PowerShell 4.0.0 için bozucu değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell sürüm 4 yayınında yapılan ve hataya neden olan değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 2f61e41b701dfc263df18064f6ac2cc4c6e4021e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863549"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Microsoft Azure PowerShell 4.0.0 için bozucu değişiklikler

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır. Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır. Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.

## <a name="table-of-contents"></a>İçindekiler

- [İşlem cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-compute-cmdlets)
- [EventHub cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-eventhub-cmdlets)
- [Insights cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-insights-cmdlets)
- [Ağ cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-network-cmdlets)
- [ServiceBus cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-servicebus-cmdlets)
- [Sql cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-sql-cmdlets)
- [Depolama cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-storage-cmdlets)
- [Profil cmdlet’lerinde bozucu değişiklikler](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a>İşlem cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki çıktı türleri etkilenmiştir:

### <a name="psvirtualmachine"></a>PSVirtualMachine
- `PSVirtualMachine` nesnesinin `DataDiskNames` ve `NetworkInterfaceIDs` üst düzey özellikleri çıktı türünden kaldırıldı. Bu özelliklere zaten `PSVirtualMachine` nesnesinin `StorageProfile` ve `NetworkProfile` özelliklerinden erişilebiliyordu ve bundan sonra bu şekilde erişilmesi gerekecek.
- Bu değişiklik, aşağıdaki cmdlet etkiler:
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>EventHub cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki cmdlet’ler etkilenir:

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- `ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- `ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı

## <a name="breaking-changes-to-insights-cmdlets"></a>Insights cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki cmdlet’ler etkilenir:
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- Bu cmdlet kullanım dışı bırakıldı.

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- Bu cmdlet’in tek nesne içeren bir liste şeklindeki çıktısı, requestId’yi ve durum kodunu içeren tek bir nesne olarak değişitirildi.
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- Bu cmdlet kullanım dışı bırakıldı.
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- Bu cmdlet’in çıktısının (nesne listesi) her bir öğesi, `{ Id, Location, Name, Tags, Properties }` yapısına sahip nesneler döndürmek yerine bir Azure Kaynağının tüm özniteliklerine ek olarak en üst düzeydeki bir AlertRuleResource’un tüm özniteliklerinden oluşan `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` yapısına sahip nesneler döndürecek şekilde düzleştirildi.
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- `AutoscaleSettingResourceName` alanı her zaman `Name` alanıyla aynı değere sahip olduğundan kullanım dışı bırakıldı.

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- Bu cmdlet'in `Boolean` olan çıktısı, `RequestId` ve `StatusCode` içeren bir nesne olarak değiştirilecek

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- Bu cmdlet’in requestId, durum kodu ve güncelleştirilmiş ya da yeni oluşturulmuş kaynağı içeren bir nesne şeklindeki çıktısı değiştirilecek
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- Komut `Update-AzureRmDiagnosticSettings` olarak yeniden adlandırılacak

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>Ağ cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki cmdlet’ler etkilenir:

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- `EnableBgp`parametresi, `boolean` yerine `string` alacak şekilde değiştirildi

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>ServiceBus cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki cmdlet’ler etkilenir:

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- `ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- `ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı

## <a name="breaking-changes-to-sql-cmdlets"></a>Sql cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki cmdlet’ler etkilenir:

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- `Tag` parametresi kaldırıldı
- `GracePeriodWithDataLossHour` parametresi `GracePeriodWithDataLossHours` olarak yeniden adlandırıldı

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- `Tag` parametresi kaldırıldı
- `GracePeriodWithDataLossHour` parametresi `GracePeriodWithDataLossHours` olarak yeniden adlandırıldı

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- `Tag` parametresi kaldırıldı

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- `Tag` parametresi kaldırıldı

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- `PartnerResourceGroupName` parametresi kaldırıldı
- `PartnerServerName` parametresi kaldırıldı

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- `ExcludedDetectionType` parametresi için `Usage_Anomaly` değeri artık geçerli değil

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- `ExcludedDetectionType` parametresi için `Usage_Anomaly` değeri artık geçerli değil

## <a name="breaking-changes-to-storage-cmdlets"></a>Depolama cmdlet’lerinde bozucu değişiklikler

Bu sürümden aşağıdaki çıktı türü özellikleri etkilenmiştir:

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Bu değişiklik, aşağıdaki cmdlet etkiler:
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Bu değişiklik, aşağıdaki cmdlet etkiler:
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- Bu değişiklik, aşağıdaki cmdlet etkiler:
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- Bu değişiklik, aşağıdaki cmdlet etkiler:
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a>Profil cmdlet’lerinde bozucu değişiklikler

Bu sürümde aşağıdaki cmdlet’ler ve cmdlet çıktı türleri değiştirildi.

### <a name="add-azurermaccount-breaking-changes"></a>Add-AzureRmAccount bozucu değişiklikleri

- ```EnvironmentName``` parametresi kaldırılıp ```Environment``` ile değiştirildi ve ```Environment``` artık bir ```AzureEnvironment``` nesnesi değil, bir dize alıyor

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>Select-AzureRmProfile, Import-AzureRmContext olarak yeniden adlandırıldı

```Select-AzureRmProfile```, ```Import-AzureRmContext``` olarak yeniden adlandırıldı

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>Save-AzureRmProfile, Save-AzureRmContext olarak yeniden adlandırıldı

```Save-AzureRmProfile```, ```Save-AzureRmContext``` olarak yeniden adlandırıldı

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>Çıktı PSAzureContext Türünde Bozucu Değişiklikler

- ```TokenCache``` özelliği, bir ```byte[]``` yerine ```IAzureTokenCache``` uygulayan bir tür olarak değiştirildi

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>Çıktı PSAzureAccount Türünde Bozucu Değişiklikler

- ```AccountType``` özelliği ```Type``` olarak değiştirildi

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>Çıktı PSAzureSubscription Türünde Bozucu Değişiklikler
- ```SubscriptionId``` özelliği ```Id``` olarak değiştirildi

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- ```SubscriptionName``` özelliği ```Name``` olarak değiştirildi

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>Çıktı PSAzureTenant Türünde Bozucu Değişiklikler

- ```TenantId``` özelliği ```Id``` olarak değiştirildi

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- ```Domain``` özelliği ```Directory``` olarak değiştirildi

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
