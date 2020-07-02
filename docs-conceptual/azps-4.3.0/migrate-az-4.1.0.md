---
title: Az 4.1.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Az sürüm 4.1.0 yayınında Azure PowerShell’de yapılan ve hataya neden olan değişikliklerin bir listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.openlocfilehash: e3a4563acf4b0820b61a2ac5da244b26490c8174
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268330"
---
# <a name="migration-guide-for-az-410"></a>Az 4.1.0 için Geçiş Kılavuzu

Bu belgede Az 3.0.0 ve 4.1.0 sürümleri arasındaki değişiklikler açıklanmaktadır.

- [Az 4.1.0 için Geçiş Kılavuzu](#migration-guide-for-az-410)
  - [Az.ApiManagement](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [Az.Batch](#azbatch)
    - [`Get-AzBatchApplication`, `New-AzBatchApplication`](#get-azbatchapplication-new-azbatchapplication)
    - [`Get-AzBatchComputeNode`, `New-AzBatchPool`](#get-azbatchcomputenode-new-azbatchpool)
    - [`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [Az.Compute](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [Az.KeyVault](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [Az.Monitor](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [Az.Network](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [Az.OperationalInsights](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [Az.Resources](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [Az.Storage](#azstorage)
    - [`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [`New-AzStorageTable`, `Get-AzStorageTable`](#new-azstoragetable-get-azstoragetable)
    - [`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a>Az.ApiManagement

### `Add-AzApiManagementRegion`

`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` türündeki `Type` özelliğinin `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` olan türü `System.String` olarak değiştirildi.

### `New-AzApiManagement`

- `New-AzApiManagement` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `New-AzApiManagement` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.

### `Set-AzApiManagement`

- `Set-AzApiManagement` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `Set-AzApiManagement` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.

### `Get-AzApiManagementProperty`

`Get-AzApiManagementProperty` cmdlet’i `Get-AzureApiManagementNamedValue` ile değiştirildi.

### `New-AzApiManagementProperty`

`New-AzApiManagementProperty` cmdlet’i `New-AzureApiManagementNamedValue` ile değiştirildi.

### `Remove-AzApiManagementProperty`

`Remove-AzApiManagementProperty` cmdlet’i `Remove-AzureApiManagementNamedValue` ile değiştirildi.

### `Set-AzApiManagementProperty`

`Set-AzApiManagementProperty` cmdlet’i `Set-AzureApiManagementNamedValue` ile değiştirildi.

## <a name="azbatch"></a>Az.Batch

### <a name="get-azbatchapplication-new-azbatchapplication"></a>`Get-AzBatchApplication`, `New-AzBatchApplication`

`Microsoft.Azure.Commands.Batch.Models.PSApplication` türündeki `ApplicationPackages` özelliği kaldırıldı.

### <a name="get-azbatchcomputenode-new-azbatchpool"></a>`Get-AzBatchComputeNode`, `New-AzBatchPool`

`Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` türündeki `PublicIPs` özelliği kaldırıldı

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a>`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`

`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` türündeki `StorageUrlExpiry` özelliğinin `System.DateTime` olan türü `System.DateTime?` olarak değiştirildi.

## <a name="azcompute"></a>Az.Compute

### `Remove-AzVmssDiagnosticsExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Get-AzVMImage`

- `Get-AzVMImage` cmdlet’i artık `FilterExpression` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `Get-AzVMImage` cmdlet’i için `ListVMImage` parametre kümesi kaldırıldı.

### `New-AzVMConfig`

- `New-AzVMConfig` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `New-AzVMConfig` cmdlet’i için `AssignIdentityParameterSet` parametre kümesi kaldırıldı.

### `Update-AzVM`

- `Update-AzVM` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `Update-AzVM` cmdlet’i için `AssignIdentityParameterSet` parametre kümesi kaldırıldı.

### `New-AzProximityPlacementGroup`

- `VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.
- `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.

#### <a name="before"></a>Önce

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- `VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.
- `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.

#### <a name="before"></a>Önce

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- `VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.
- `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.

#### <a name="before"></a>Önce

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Add-AzVmssDataDisk`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Add-AzVmssExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Add-AzVmssNetworkInterfaceConfiguration`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Add-AzVmssSecret`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Add-AzVmssSshPublicKey`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Add-AzVmssWinRMListener`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `New-AzVmssConfig`

- `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.
- Artık `AutomaticRepairMaxInstanceRepairsPercent` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- Artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `__AllParameterSets` parametre kümesi kaldırıldı.
- `ExplicitIdentityParameterSet` parametre kümesi kaldırıldı.
- `AssignIdentityParameterSet` parametre kümesi kaldırıldı.

### `Remove-AzVmssDataDisk`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Remove-AzVmssExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Remove-AzVmssNetworkInterfaceConfiguration`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Set-AzVmssBootDiagnostic`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Set-AzVmssOsProfile`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Set-AzVmssRollingUpgradePolicy`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Set-AzVmssStorageProfile`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `New-AzVmss`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Repair-AzVmssServiceFabricUpdateDomain`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Get-AzVmss`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Set-AzVmssOrchestrationServiceState`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Update-AzVmss`

- `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.
- Artık `AutomaticRepairMaxInstanceRepairsPercent` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `__AllParameterSets` parametre kümesi kaldırıldı.
- `ExplicitIdentityParameterSet` parametre kümesi kaldırıldı.

### `Add-AzVmssDiagnosticsExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

### `Disable-AzVmssDiskEncryption`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.

## <a name="azkeyvault"></a>Az.KeyVault

### `New-AzKeyVaultCertificateOrganizationDetail`

`New-AzKeyVaultCertificateOrganizationDetails` diğer adı kaldırıldı. Lütfen `New-AzKeyVaultCertificateOrganizationDetail` kullanın.

#### <a name="before"></a>Önce

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

`New-AzKeyVaultCertificateAdministratorDetails` diğer adı kaldırıldı. Lütfen `New-AzKeyVaultCertificateAdministratorDetail` kullanın.

#### <a name="before"></a>Önce

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

Geçici silme varsayılan olarak etkin olduğundan `-EnableSoftDelete` kaldırıldı. Bu davranışı istemiyorsanız lütfen `-DisableSoftDelete` kullanın.

#### <a name="before"></a>Önce

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a>Az.Monitor

### `Add-AzLogProfile`

`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` türündeki `RetentionPolicy` özelliğinin `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` olan türü `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` olarak değiştirildi.

### `Get-AzLogProfile`

`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` türündeki `RetentionPolicy` özelliğinin `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` olan türü `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` olarak değiştirildi.

### `New-AzMetricAlertRuleV2Criteria`

`New-AzMetricAlertRuleV2Criteria` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.

## <a name="aznetwork"></a>Az.Network

### `Get-AzNetworkWatcherConnectionMonitor`

`RoundTripTimeMs` özelliği için `System.Nullable1[System.Int32]` olan genel tür `System.Nullable1[System.Double]` olarak değiştirildi.

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

`SuccessThresholdRoundTripTimeMs` parametresi için `System.Nullable1[System.Int32]` olan genel tür `System.Nullable1[System.Double]` olarak değiştirildi.

## <a name="azoperationalinsights"></a>Az.OperationalInsights

### `Get-AzOperationalInsightsDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsApplicationInsightsDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsAzureActivityLogDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsCustomLogDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsLinuxSyslogDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsWindowsEventDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Remove-AzOperationalInsightsDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Disable-AzOperationalInsightsIISLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Enable-AzOperationalInsightsIISLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Get-AzOperationalInsightsSavedSearch`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` türündeki `Metadata` özelliği kaldırıldı.

### `Get-AzOperationalInsightsSavedSearchResult`

Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsSavedSearchResult` cmdlet’i kaldırıldı.

### `Get-AzOperationalInsightsSearchResult`

Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsSearchResult` cmdlet’i kaldırıldı.

### `Get-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Remove-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Set-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Get-AzOperationalInsightsLinkTarget`

Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsLinkTarget` cmdlet’i kaldırıldı.

### `Get-AzOperationalInsightsWorkspace`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `New-AzOperationalInsightsWorkspace`

- `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.
- `New-AzOperationalInsightsWorkspace` cmdlet’i artık `CustomerId` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.
- `New-AzOperationalInsightsWorkspace` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.

### `Set-AzOperationalInsightsWorkspace`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

### `Invoke-AzOperationalInsightsQuery`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.

## <a name="azresources"></a>Az.Resources

### `Get-AzDeploymentScript`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.

### `Get-AzDeploymentScriptLog`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.

### `Save-AzDeploymentScriptLog`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

`TenantLevel` parametresi kaldırıldı.

### `Get-AzPolicyAlias`

`Aliases` özelliği için `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]` olarak değiştirildi.

### `New-AzPolicyAssignment`

- `New-AzPolicyAssignment` cmdlet’i artık `PolicyDefinition` parametresi için `System.Management.Automation.PSObject` türünü desteklememektedir.
- `New-AzPolicyAssignment` cmdlet’i artık `PolicySetDefinition` parametresi için `System.Management.Automation.PSObject` türünü desteklememektedir.

### `Remove-AzDeploymentScript`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.

## <a name="azstorage"></a>Az.Storage

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a>`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`

NetWorkRule DefaultAction değeri değiştirildi, eski değer: İzin Ver = 1, Reddet = 0, yeni değer: İzin Ver = 0, Reddet = 1.

### <a name="new-azstoragetable-get-azstoragetable"></a>`New-AzStorageTable`, `Get-AzStorageTable`

AzureStorageTable.CloudTable.ServiceClient çıkış nesnesinden 2 özellik kaldırıldı: ConnectionPolicy, ConsistencyLevel.

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a>`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`

CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFile" alt özelliği olacak

#### <a name="before"></a>Önce

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a>`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`

CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFileDirectory" alt özelliği olacak

#### <a name="before"></a>Önce

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a>`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`

FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFileShare" alt özelliği olacak

#### <a name="before"></a>Önce

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın ""CloudFileShare.Properties"" alt özelliği olacak

#### <a name="before"></a>Önce

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

Üst Dizin nesnesi ve -Path ile alt Dosya Dizinleri kaldırılırken, artık işlem hattından tür (dize) eşleşmesiyle -Path girilemez.

#### <a name="before"></a>Önce

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Sonra

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
