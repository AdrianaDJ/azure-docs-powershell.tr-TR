---
title: Az 5.0.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Az sürüm 5.0.0 yayınında Azure PowerShell’de yapılan yeni değişikliklerin bir listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715639"
---
# <a name="migration-guide-for-az-500"></a>Az 5.0.0 için Geçiş Kılavuzu

Bu belgede Az 4.0.0 ve 5.0.0 sürümleri arasındaki değişiklikler açıklanmaktadır.

- [Az 5.0.0 için Geçiş Kılavuzu](#migration-guide-for-az-500)
  - [Az.Aks](#azaks)
    - [New-AzAksCluster](#new-azakscluster)
    - [Set-AzAksCluster](#set-azakscluster)
  - [Az.ContainerRegistry](#azcontainerregistry)
    - [New-AzContainerRegistry](#new-azcontainerregistry)
  - [Az.Functions](#azfunctions)
    - [Get-AzFunctionApp](#get-azfunctionapp)
    - [New-AzFunctionApp](#new-azfunctionapp)
  - [Az.KeyVault](#azkeyvault)
    - [New-AzKeyVault](#new-azkeyvault)
    - [Update-AzKeyVault](#update-azkeyvault)
    - [Get-AzKeyVaultSecret](#get-azkeyvaultsecret)
  - [Az.ManagedServices](#azmanagedservices)
    - [Get-AzManagedServicesDefinition](#get-azmanagedservicesdefinition)
    - [New-AzManagedServicesAssignment](#new-azmanagedservicesassignment)
    - [Remove-AzManagedServicesAssignment](#remove-azmanagedservicesassignment)
    - [Remove-AzManagedServicesDefinition](#remove-azmanagedservicesdefinition)
  - [Az.ResourceManager](#azresourcemanager)
    - [Get-AzManagementGroupDeployment](#get-azmanagementgroupdeployment)
    - [Get-AzManagementGroupDeploymentOperation](#get-azmanagementgroupdeploymentoperation)
    - [Get-AzDeployment](#get-azdeployment)
    - [Get-AzDeploymentOperation](#get-azdeploymentoperation)
    - [Get-AzDeploymentWhatIfResult](#get-azdeploymentwhatifresult)
    - [Get-AzTenantDeployment](#get-aztenantdeployment)
    - [Get-AzTenantDeploymentOperation](#get-aztenantdeploymentoperation)
    - [New-AzManagementGroupDeployment](#new-azmanagementgroupdeployment)
    - [New-AzDeployment](#new-azdeployment)
    - [New-AzTenantDeployment](#new-aztenantdeployment)
    - [Remove-AzManagementGroupDeployment](#remove-azmanagementgroupdeployment)
    - [Remove-AzDeployment](#remove-azdeployment)
    - [Remove-AzTenantDeployment](#remove-aztenantdeployment)
    - [Save-AzManagementGroupDeploymentTemplate](#save-azmanagementgroupdeploymenttemplate)
    - [Save-AzDeploymentTemplate](#save-azdeploymenttemplate)
    - [Save-AzTenantDeploymentTemplate](#save-aztenantdeploymenttemplate)
    - [Stop-AzManagementGroupDeployment](#stop-azmanagementgroupdeployment)
    - [Stop-AzDeployment](#stop-azdeployment)
    - [Stop-AzTenantDeployment](#stop-aztenantdeployment)
    - [Test-AzManagementGroupDeployment](#test-azmanagementgroupdeployment)
    - [Test-AzDeployment](#test-azdeployment)
    - [Test-AzTenantDeployment](#test-aztenantdeployment)
    - [Get-AzResourceGroupDeployment](#get-azresourcegroupdeployment)
    - [Get-AzResourceGroupDeploymentOperation](#get-azresourcegroupdeploymentoperation)
    - [Get-AzResourceGroupDeploymentWhatIfResult](#get-azresourcegroupdeploymentwhatifresult)
    - [New-AzResourceGroupDeployment](#new-azresourcegroupdeployment)
    - [Remove-AzResourceGroupDeployment](#remove-azresourcegroupdeployment)
    - [Save-AzResourceGroupDeploymentTemplate](#save-azresourcegroupdeploymenttemplate)
    - [Stop-AzResourceGroupDeployment](#stop-azresourcegroupdeployment)
    - [Test-AzResourceGroupDeployment](#test-azresourcegroupdeployment)
    - [Get-AzManagementGroupDeploymentWhatIfResult](#get-azmanagementgroupdeploymentwhatifresult)
    - [Get-AzTenantDeploymentWhatIfResult](#get-aztenantdeploymentwhatifresult)
  - [Az.Sql](#azsql)
    - [Set-AzSqlServerActiveDirectoryAdministrator](#set-azsqlserveractivedirectoryadministrator)
  - [Az.Synapse](#azsynapse)
    - [New-AzSynapseSqlPool](#new-azsynapsesqlpool)
    - [Update-AzSynapseSqlPool](#update-azsynapsesqlpool)
  - [Az.Network](#aznetwork)
    - [Approve-AzPrivateEndpointConnection](#approve-azprivateendpointconnection)
    - [Deny-AzPrivateEndpointConnection](#deny-azprivateendpointconnection)
    - [Get-AzPrivateEndpointConnection](#get-azprivateendpointconnection)
    - [Remove-AzPrivateEndpointConnection](#remove-azprivateendpointconnection)
    - [Set-AzPrivateEndpointConnection](#set-azprivateendpointconnection)
    - [New-AzNetworkWatcherConnectionMonitorEndpointObject](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a>Az.Aks

### <a name="new-azakscluster"></a>New-AzAksCluster

- Artık `NodeOsType` parametresini desteklemiyor ve özgün parametre adı için diğer ad bulunamadı, bu ad her zaman `Linux` olacak.
- Artık `ServicePrincipalIdAndSecret` parametresi için `ClientIdAndSecret` diğer adını desteklemiyor.
- `NodeVmSetType` varsayılan değeri `AvailabilitySet` yerine `VirtualMachineScaleSets` olarak değiştirildi.
- `NetworkPlugin` varsayılan değeri `none` yerine `azure` olarak değiştirildi.

#### <a name="before"></a>Önce

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a>Sonra

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a>Set-AzAksCluster

Artık `ServicePrincipalIdAndSecret` parametresi için `ClientIdAndSecret` diğer adını desteklemiyor.

#### <a name="before"></a>Önce

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a>Sonra

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a>Az.ContainerRegistry

### <a name="new-azcontainerregistry"></a>New-AzContainerRegistry

Artık `StorageAccountName` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a>Sonra

`Classic` kullanım dışı bırakıldı ve `StorageAccountName` yalnızca Klasik Container Registry ile çalıştığından kaldırıldı.

## <a name="azfunctions"></a>Az.Functions

### <a name="get-azfunctionapp"></a>Get-AzFunctionApp

`IncludeSlot` anahtar parametresi, `Get-AzFunctionApp` cmdlet’inin biri dışındaki tüm parametre kümelerinden kaldırıldı. Cmdlet, şimdi `-IncludeSlot` belirtildiğinde sonuçlarda dağıtım yuvalarının alınmasını destekliyor.
Bu işlev, önceki cmdlet sürümünde çalışmıyordu. Ancak bu sorun şimdi düzeltildi.

### <a name="new-azfunctionapp"></a>New-AzFunctionApp

- `New-AzFunctionApp` cmdlet’indeki `-DisableApplicationInsights`, bu seçenek belirtildiğinde hiçbir Application Insights projesi oluşturulmayacak şekilde düzeltildi.
- PowerShell 6.2 EOL olduğundan, PowerShell 6.2 işlev uygulamaları oluşturma desteği kaldırıldı. Müşterilerin, şu anda bunun yerine PowerShell 7.0 işlev uygulamaları oluşturmaları gerekir.
- `RuntimeVersion` parametresi belirtilmediğinde, PowerShell işlev uygulamaları için Windows üzerinde İşlevler sürüm 3’teki varsayılan çalışma zamanı 6.2 sürümünden 7.0 sürümüne yükseltildi.
- `RuntimeVersion` parametresi belirtilmediğinde, Node işlev uygulamaları için Windows ve Linux üzerinde İşlevler sürüm 3’teki varsayılan çalışma zamanı 10 sürümünden 12 sürümüne yükseltildi. Ancak kullanıcılar, `-Runtime Node` ve `-RuntimeVersion 10` parametrelerini belirterek Node 10 işlev uygulamalarını oluşturmaya devam edebilir. `RuntimeVersion` parametresi belirtilmediğinde, Python işlev uygulamaları için Linux üzerinde İşlevler sürüm 3’teki varsayılan çalışma zamanı 3.7 sürümünden 3.8 sürümüne yükseltildi. Ancak kullanıcılar, `-Runtime Python` ve `-RuntimeVersion 3.7` parametrelerini belirterek Python 3.7 işlev uygulamalarını oluşturmaya devam edebilir.

#### <a name="before"></a>Önce

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a>Sonra

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a>Az.KeyVault

### <a name="new-azkeyvault"></a>New-AzKeyVault

Artık `DisableSoftDelete` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a>Sonra

Geçici silme ayarını güncelleştirme özelliği Az.KeyVault 3.0.0 sürümünde kullanımdan kaldırıldı. Devamını okuyun: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="update-azkeyvault"></a>Update-AzKeyVault

Artık `EnableSoftDelete` ve `SoftDeleteRetentionInDays` parametrelerini desteklemiyor. Özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a>Sonra

Geçici silme ayarını güncelleştirme özelliği Az.KeyVault 3.0.0 sürümünde kullanımdan kaldırıldı. Devamını okuyun: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="get-azkeyvaultsecret"></a>Get-AzKeyVaultSecret

`Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` türündeki `SecretValueText` özelliği kaldırıldı. `SecretValueText` özelliği `SecretValue` ile değiştirildi.

#### <a name="before"></a>Önce

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a>Sonra

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a>Az.ManagedServices

### <a name="get-azmanagedservicesdefinition"></a>Get-AzManagedServicesDefinition

Artık `ResourceId` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Sonra

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a>New-AzManagedServicesAssignment

Artık `RegistrationDefinitionName` ve `RegistrationDefinitionResourceId` parametrelerini desteklemiyor. Özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a>Sonra

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a>Remove-AzManagedServicesAssignment

Artık `Id` ve `ResourceId` parametrelerini desteklemiyor. Özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a>Sonra

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a>Remove-AzManagedServicesDefinition

Artık `Id` ve `ResourceId` parametrelerini desteklemiyor. Özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Sonra

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a>Az.ResourceManager

### <a name="get-azmanagementgroupdeployment"></a>Get-AzManagementGroupDeployment

Artık `ApiVersion` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a>Sonra

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a>Get-AzManagementGroupDeploymentOperation

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-azdeployment"></a>Get-AzDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-azdeploymentoperation"></a>Get-AzDeploymentOperation

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-azdeploymentwhatifresult"></a>Get-AzDeploymentWhatIfResult

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-aztenantdeployment"></a>Get-AzTenantDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-aztenantdeploymentoperation"></a>Get-AzTenantDeploymentOperation

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="new-azmanagementgroupdeployment"></a>New-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="new-azdeployment"></a>New-AzDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="new-aztenantdeployment"></a>New-AzTenantDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="remove-azmanagementgroupdeployment"></a>Remove-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="remove-azdeployment"></a>Remove-AzDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="remove-aztenantdeployment"></a>Remove-AzTenantDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="save-azmanagementgroupdeploymenttemplate"></a>Save-AzManagementGroupDeploymentTemplate

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="save-azdeploymenttemplate"></a>Save-AzDeploymentTemplate

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="save-aztenantdeploymenttemplate"></a>Save-AzTenantDeploymentTemplate

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="stop-azmanagementgroupdeployment"></a>Stop-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="stop-azdeployment"></a>Stop-AzDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="stop-aztenantdeployment"></a>Stop-AzTenantDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="test-azmanagementgroupdeployment"></a>Test-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="test-azdeployment"></a>Test-AzDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="test-aztenantdeployment"></a>Test-AzTenantDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-azresourcegroupdeployment"></a>Get-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-azresourcegroupdeploymentoperation"></a>Get-AzResourceGroupDeploymentOperation

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-azresourcegroupdeploymentwhatifresult"></a>Get-AzResourceGroupDeploymentWhatIfResult

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="new-azresourcegroupdeployment"></a>New-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="remove-azresourcegroupdeployment"></a>Remove-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="save-azresourcegroupdeploymenttemplate"></a>Save-AzResourceGroupDeploymentTemplate

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="stop-azresourcegroupdeployment"></a>Stop-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="test-azresourcegroupdeployment"></a>Test-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a>Get-AzManagementGroupDeploymentWhatIfResult

`Get-AzManagementGroupDeployment` ile aynı.

### <a name="get-aztenantdeploymentwhatifresult"></a>Get-AzTenantDeploymentWhatIfResult

`Get-AzManagementGroupDeployment` ile aynı.

## <a name="azsql"></a>Az.Sql

### <a name="set-azsqlserveractivedirectoryadministrator"></a>Set-AzSqlServerActiveDirectoryAdministrator

Artık `IsAzureADOnlyAuthentication` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a>Sonra

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a>Az.Synapse

### <a name="new-azsynapsesqlpool"></a>New-AzSynapseSqlPool

Artık `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` ve `RestorePoint` parametrelerini desteklemiyor. Özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a>Update-AzSynapseSqlPool

Artık `Suspend` ve `Resume` parametrelerini desteklemiyor. Özgün parametre adı için diğer ad bulunamadı.

## <a name="aznetwork"></a>Az.Network

### <a name="approve-azprivateendpointconnection"></a>Approve-AzPrivateEndpointConnection

Artık `PrivateLinkResourceType` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a>Sonra

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a>Deny-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection` ile aynı.

### <a name="get-azprivateendpointconnection"></a>Get-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection` ile aynı.

### <a name="remove-azprivateendpointconnection"></a>Remove-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection` ile aynı.

### <a name="set-azprivateendpointconnection"></a>Set-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection` ile aynı.

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a>New-AzNetworkWatcherConnectionMonitorEndpointObject

Artık `FilterType` ve `FilterItem` parametrelerini desteklemiyor. Özgün parametre adı için diğer ad bulunamadı.

#### <a name="before"></a>Önce

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a>Sonra

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
