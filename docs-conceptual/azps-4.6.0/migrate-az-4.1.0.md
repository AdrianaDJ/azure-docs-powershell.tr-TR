---
title: Az 4.1.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Az sürüm 4.1.0 yayınında Azure PowerShell’de yapılan ve hataya neden olan değişikliklerin bir listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5f42bbb65313d1caa839443d463b61cc743ca0a5
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242673"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="50fcf-103">Az 4.1.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="50fcf-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="50fcf-104">Bu belgede Az 3.0.0 ve 4.1.0 sürümleri arasındaki değişiklikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="50fcf-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="50fcf-105">Az 4.1.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="50fcf-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="50fcf-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50fcf-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="50fcf-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50fcf-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="50fcf-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="50fcf-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="50fcf-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="50fcf-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="50fcf-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="50fcf-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="50fcf-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50fcf-111">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="50fcf-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50fcf-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="50fcf-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50fcf-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="50fcf-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50fcf-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="50fcf-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50fcf-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="50fcf-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50fcf-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="50fcf-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50fcf-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="50fcf-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="50fcf-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="50fcf-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="50fcf-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="50fcf-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="50fcf-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="50fcf-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="50fcf-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="50fcf-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="50fcf-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="50fcf-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50fcf-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="50fcf-124">`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` türündeki `Type` özelliğinin `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` olan türü `System.String` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="50fcf-125">`New-AzApiManagement` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-126">`New-AzApiManagement` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="50fcf-127">`Set-AzApiManagement` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-128">`Set-AzApiManagement` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="50fcf-129">`Get-AzApiManagementProperty` cmdlet’i `Get-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzureApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="50fcf-130">`New-AzApiManagementProperty` cmdlet’i `New-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzureApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="50fcf-131">`Remove-AzApiManagementProperty` cmdlet’i `Remove-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzureApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="50fcf-132">`Set-AzApiManagementProperty` cmdlet’i `Set-AzureApiManagementNamedValue` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzureApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="50fcf-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50fcf-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="50fcf-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="50fcf-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="50fcf-135">`Microsoft.Azure.Commands.Batch.Models.PSApplication` türündeki `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="50fcf-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="50fcf-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="50fcf-137">`Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` türündeki `PublicIPs` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50fcf-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="50fcf-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="50fcf-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="50fcf-139">`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` türündeki `StorageUrlExpiry` özelliğinin `System.DateTime` olan türü `System.DateTime?` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="50fcf-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50fcf-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="50fcf-141">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="50fcf-142">`Get-AzVMImage` cmdlet’i artık `FilterExpression` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-143">`Get-AzVMImage` cmdlet’i için `ListVMImage` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="50fcf-144">`New-AzVMConfig` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-145">`New-AzVMConfig` cmdlet’i için `AssignIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="50fcf-146">`Update-AzVM` cmdlet’i artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-147">`Update-AzVM` cmdlet’i için `AssignIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="50fcf-148">`VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="50fcf-149">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-150">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-150">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="50fcf-151">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-151">After</span></span>

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

- <span data-ttu-id="50fcf-152">`VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="50fcf-153">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-154">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-154">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="50fcf-155">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-155">After</span></span>

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

- <span data-ttu-id="50fcf-156">`VirtualMachines`, `VirtualMachineScaleSets` ve `AvailabilitySets` için `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="50fcf-157">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` türündeki `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` ve `AvailabilitySetsColocationStatus` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-158">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-158">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="50fcf-159">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-159">After</span></span>

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

<span data-ttu-id="50fcf-160">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="50fcf-161">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="50fcf-162">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="50fcf-163">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="50fcf-164">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="50fcf-165">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="50fcf-166">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="50fcf-167">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="50fcf-168">Artık `AutomaticRepairMaxInstanceRepairsPercent` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-169">Artık `AssignIdentity` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-170">`__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="50fcf-171">`ExplicitIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="50fcf-172">`AssignIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="50fcf-173">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="50fcf-174">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="50fcf-175">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="50fcf-176">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="50fcf-177">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="50fcf-178">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="50fcf-179">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="50fcf-180">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="50fcf-181">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="50fcf-182">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="50fcf-183">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="50fcf-184">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="50fcf-185">Artık `AutomaticRepairMaxInstanceRepairsPercent` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-186">`__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="50fcf-187">`ExplicitIdentityParameterSet` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="50fcf-188">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="50fcf-189">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` türündeki `AutomaticRepairsPolicy` özelliğinin `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` olan türü `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="50fcf-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50fcf-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="50fcf-191">`New-AzKeyVaultCertificateOrganizationDetails` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="50fcf-192">Lütfen `New-AzKeyVaultCertificateOrganizationDetail` kullanın.</span><span class="sxs-lookup"><span data-stu-id="50fcf-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-193">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="50fcf-194">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="50fcf-195">`New-AzKeyVaultCertificateAdministratorDetails` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="50fcf-196">Lütfen `New-AzKeyVaultCertificateAdministratorDetail` kullanın.</span><span class="sxs-lookup"><span data-stu-id="50fcf-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-197">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="50fcf-198">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="50fcf-199">Geçici silme varsayılan olarak etkin olduğundan `-EnableSoftDelete` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="50fcf-200">Bu davranışı istemiyorsanız lütfen `-DisableSoftDelete` kullanın.</span><span class="sxs-lookup"><span data-stu-id="50fcf-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-201">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="50fcf-202">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="50fcf-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50fcf-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="50fcf-204">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` türündeki `RetentionPolicy` özelliğinin `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` olan türü `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="50fcf-205">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` türündeki `RetentionPolicy` özelliğinin `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` olan türü `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="50fcf-206">`New-AzMetricAlertRuleV2Criteria` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="50fcf-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50fcf-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="50fcf-208">`RoundTripTimeMs` özelliği için `System.Nullable1[System.Int32]` olan genel tür `System.Nullable1[System.Double]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="50fcf-209">`SuccessThresholdRoundTripTimeMs` parametresi için `System.Nullable1[System.Int32]` olan genel tür `System.Nullable1[System.Double]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="50fcf-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50fcf-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="50fcf-211">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="50fcf-212">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="50fcf-213">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="50fcf-214">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="50fcf-215">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="50fcf-216">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="50fcf-217">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="50fcf-218">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="50fcf-219">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="50fcf-220">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="50fcf-221">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="50fcf-222">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="50fcf-223">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="50fcf-224">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="50fcf-225">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="50fcf-226">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="50fcf-227">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="50fcf-228">`Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` türündeki `Metadata` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="50fcf-229">Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsSavedSearchResult` cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="50fcf-230">Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsSearchResult` cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="50fcf-231">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="50fcf-232">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="50fcf-233">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="50fcf-234">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="50fcf-235">Artık SDK tarafından desteklenmeyen `Get-AzOperationalInsightsLinkTarget` cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="50fcf-236">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="50fcf-237">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="50fcf-238">`New-AzOperationalInsightsWorkspace` cmdlet’i artık `CustomerId` parametresini desteklememektedir ve özgün parametre adı için diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="50fcf-239">`New-AzOperationalInsightsWorkspace` cmdlet’i için `__AllParameterSets` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="50fcf-240">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="50fcf-241">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` türündeki `PortalUrl` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="50fcf-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50fcf-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="50fcf-243">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="50fcf-244">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="50fcf-245">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="50fcf-246">`TenantLevel` parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50fcf-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="50fcf-247">`Aliases` özelliği için `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` olan genel tür `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="50fcf-248">`New-AzPolicyAssignment` cmdlet’i artık `PolicyDefinition` parametresi için `System.Management.Automation.PSObject` türünü desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="50fcf-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="50fcf-249">`New-AzPolicyAssignment` cmdlet’i artık `PolicySetDefinition` parametresi için `System.Management.Automation.PSObject` türünü desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="50fcf-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="50fcf-250">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` türündeki `Status` özelliğinin `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` olan türü `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50fcf-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="50fcf-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50fcf-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="50fcf-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="50fcf-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="50fcf-253">NetWorkRule DefaultAction değeri değiştirildi, eski değer: İzin Ver = 1, Reddet = 0, yeni değer: İzin Ver = 0, Reddet = 1.</span><span class="sxs-lookup"><span data-stu-id="50fcf-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="50fcf-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="50fcf-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="50fcf-255">AzureStorageTable.CloudTable.ServiceClient çıkış nesnesinden 2 özellik kaldırıldı: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="50fcf-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="50fcf-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="50fcf-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="50fcf-257">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFile" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50fcf-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-258">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="50fcf-259">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="50fcf-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="50fcf-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="50fcf-261">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFileDirectory" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50fcf-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-262">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="50fcf-263">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="50fcf-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="50fcf-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="50fcf-265">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın "CloudFileShare" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50fcf-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-266">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="50fcf-267">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="50fcf-268">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın ""CloudFileShare.Properties"" alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50fcf-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-269">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="50fcf-270">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-270">After</span></span>

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

<span data-ttu-id="50fcf-271">Üst Dizin nesnesi ve -Path ile alt Dosya Dizinleri kaldırılırken, artık işlem hattından tür (dize) eşleşmesiyle -Path girilemez.</span><span class="sxs-lookup"><span data-stu-id="50fcf-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="50fcf-272">Önce</span><span class="sxs-lookup"><span data-stu-id="50fcf-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="50fcf-273">Sonra</span><span class="sxs-lookup"><span data-stu-id="50fcf-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
