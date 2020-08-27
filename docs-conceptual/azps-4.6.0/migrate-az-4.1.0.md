---
title: Az 4.1.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Az sürüm 4.1.0 yayınında Azure PowerShell’de yapılan ve hataya neden olan değişikliklerin bir listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.openlocfilehash: e3a4563acf4b0820b61a2ac5da244b26490c8174
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821926"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="cb890-103">Az 4.1.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="cb890-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="cb890-104">Bu belgede Az 3.0.0 ve 4.1.0 sürümleri arasındaki değişiklikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cb890-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="cb890-105">Az 4.1.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="cb890-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="cb890-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb890-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="cb890-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb890-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="cb890-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="cb890-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="cb890-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="cb890-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="cb890-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="cb890-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="cb890-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb890-111">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="cb890-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb890-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="cb890-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb890-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="cb890-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb890-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="cb890-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb890-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="cb890-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb890-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="cb890-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb890-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="cb890-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="cb890-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="cb890-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="cb890-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="cb890-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="cb890-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="cb890-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="cb890-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="cb890-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="cb890-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="cb890-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb890-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="cb890-124">`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` türündeki `Type` özelliğinin `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` olan türü `System.String` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="cb890-125">`New-AzApiManagement` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-126">`New-AzApiManagement` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="cb890-127">`Set-AzApiManagement` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-128">`Set-AzApiManagement` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="cb890-129">`Get-AzApiManagementProperty` cmdlet’i `Get-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzureApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="cb890-130">`New-AzApiManagementProperty` cmdlet’i `New-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzureApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="cb890-131">`Remove-AzApiManagementProperty` cmdlet’i `Remove-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzureApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="cb890-132">`Set-AzApiManagementProperty` cmdlet’i `Set-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzureApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="cb890-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb890-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="cb890-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="cb890-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="cb890-135">`Microsoft.Azure.Commands.Batch.Models.PSApplication` türündeki `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="cb890-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="cb890-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="cb890-137">`Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` türündeki `PublicIPs` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="cb890-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="cb890-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="cb890-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="cb890-139">`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` türündeki `StorageUrlExpiry` özelliğinin `System.DateTime` olan türü `System.DateTime?` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="cb890-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb890-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="cb890-141">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="cb890-142">`Get-AzVMImage` cmdlet’i artık `FilterExpression` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-143">`Get-AzVMImage` cmdlet’i için `ListVMImage` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="cb890-144">`New-AzVMConfig` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-145">`New-AzVMConfig` cmdlet’i için `AssignIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="cb890-146">`Update-AzVM` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-147">`Update-AzVM` cmdlet’i için `AssignIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="cb890-148">`VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="cb890-149">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-150">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-150">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="cb890-151">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-151">After</span></span>

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

- <span data-ttu-id="cb890-152">`VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="cb890-153">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-154">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-154">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="cb890-155">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-155">After</span></span>

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

- <span data-ttu-id="cb890-156">`VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="cb890-157">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-158">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-158">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="cb890-159">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-159">After</span></span>

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

<span data-ttu-id="cb890-160">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="cb890-161">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="cb890-162">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="cb890-163">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="cb890-164">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="cb890-165">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="cb890-166">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="cb890-167">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="cb890-168">Artık `AutomaticRepairMaxInstanceRepairsPercent` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-169">Artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-170">`__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="cb890-171">`ExplicitIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="cb890-172">`AssignIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="cb890-173">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="cb890-174">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="cb890-175">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="cb890-176">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="cb890-177">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="cb890-178">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="cb890-179">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="cb890-180">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="cb890-181">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="cb890-182">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="cb890-183">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="cb890-184">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="cb890-185">Artık `AutomaticRepairMaxInstanceRepairsPercent` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-186">`__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="cb890-187">`ExplicitIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="cb890-188">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="cb890-189">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="cb890-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb890-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="cb890-191">`New-AzKeyVaultCertificateOrganizationDetails` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="cb890-192">Lütfen `New-AzKeyVaultCertificateOrganizationDetail` kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb890-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-193">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="cb890-194">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="cb890-195">`New-AzKeyVaultCertificateAdministratorDetails` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="cb890-196">Lütfen `New-AzKeyVaultCertificateAdministratorDetail` kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb890-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-197">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="cb890-198">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="cb890-199">Geçici silme varsayılan olarak etkin olduğundan `-EnableSoftDelete` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="cb890-200">Bu davranışı istemiyorsanız lütfen `-DisableSoftDelete` kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb890-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-201">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="cb890-202">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="cb890-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb890-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="cb890-204">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` türündeki `RetentionPolicy` özelliğinin `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` olan türü `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="cb890-205">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` türündeki `RetentionPolicy` özelliğinin `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` olan türü `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="cb890-206">`New-AzMetricAlertRuleV2Criteria` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="cb890-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb890-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="cb890-208">`RoundTripTimeMs` özelliği için `System.Nullable1[System.Int32]` olan genel tür `System.Nullable1[System.Double]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="cb890-209">`SuccessThresholdRoundTripTimeMs` parametresi için `System.Nullable1[System.Int32]` olan genel tür `System.Nullable1[System.Double]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="cb890-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb890-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="cb890-211">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="cb890-212">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="cb890-213">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="cb890-214">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="cb890-215">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="cb890-216">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="cb890-217">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="cb890-218">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="cb890-219">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="cb890-220">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="cb890-221">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="cb890-222">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="cb890-223">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="cb890-224">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="cb890-225">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="cb890-226">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="cb890-227">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="cb890-228">`Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` türündeki `Metadata` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="cb890-229">Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsSavedSearchResult` cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="cb890-230">Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsSearchResult` cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="cb890-231">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="cb890-232">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="cb890-233">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="cb890-234">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="cb890-235">Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsLinkTarget` cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="cb890-236">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="cb890-237">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="cb890-238">`New-AzOperationalInsightsWorkspace` cmdlet’i artık `CustomerId` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="cb890-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="cb890-239">`New-AzOperationalInsightsWorkspace` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="cb890-240">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="cb890-241">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="cb890-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb890-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="cb890-243">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="cb890-244">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="cb890-245">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="cb890-246">`TenantLevel` parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb890-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="cb890-247">`Aliases` özelliği için `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="cb890-248">`New-AzPolicyAssignment` cmdlet’i artık `PolicyDefinition` parametresi için `System.Management.Automation.PSObject` türünü desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="cb890-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="cb890-249">`New-AzPolicyAssignment` cmdlet’i artık `PolicySetDefinition` parametresi için `System.Management.Automation.PSObject` türünü desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="cb890-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="cb890-250">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cb890-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="cb890-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb890-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="cb890-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="cb890-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="cb890-253">NetWorkRule DefaultAction değeri değiştirildi, eski değer: İzin Ver = 1, Reddet = 0, yeni değer: İzin Ver = 0, Reddet = 1.</span><span class="sxs-lookup"><span data-stu-id="cb890-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="cb890-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="cb890-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="cb890-255">AzureStorageTable.CloudTable.ServiceClient çıkış nesnesinden 2 özellik kaldırıldı: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="cb890-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="cb890-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="cb890-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="cb890-257">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFile" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="cb890-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-258">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="cb890-259">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="cb890-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="cb890-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="cb890-261">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFileDirectory" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="cb890-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-262">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="cb890-263">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="cb890-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="cb890-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="cb890-265">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFileShare" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="cb890-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-266">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="cb890-267">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="cb890-268">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın ""CloudFileShare.Properties"" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="cb890-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-269">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="cb890-270">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-270">After</span></span>

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

<span data-ttu-id="cb890-271">Üst Dizin nesnesi ve -Path ile alt Dosya Dizinleri kaldırılırken, artık işlem hattından tür (dize) eşleşmesiyle -Path girilemez.</span><span class="sxs-lookup"><span data-stu-id="cb890-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="cb890-272">Önce</span><span class="sxs-lookup"><span data-stu-id="cb890-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="cb890-273">Sonra</span><span class="sxs-lookup"><span data-stu-id="cb890-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```