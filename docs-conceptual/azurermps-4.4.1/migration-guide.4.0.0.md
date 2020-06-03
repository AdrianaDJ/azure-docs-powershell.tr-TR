---
title: Microsoft Azure PowerShell 4.0.0 için bozucu değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell sürüm 4 yayınında yapılan ve hataya neden olan değişikliklerin listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 47d7ab67a6b1d092bb07405e7dc925d844cac5ab
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386723"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="bbeef-103">Microsoft Azure PowerShell 4.0.0 için bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-103">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="bbeef-104">Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="bbeef-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="bbeef-105">Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır.</span><span class="sxs-lookup"><span data-stu-id="bbeef-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="bbeef-106">Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="bbeef-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="bbeef-107">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="bbeef-107">Table of Contents</span></span>

- [<span data-ttu-id="bbeef-108">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="bbeef-109">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="bbeef-110">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="bbeef-111">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="bbeef-112">ServiceBus cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-112">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="bbeef-113">Sql cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-113">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="bbeef-114">Depolama cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-114">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="bbeef-115">Profil cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-115">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="bbeef-116">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-116">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="bbeef-117">Bu sürümden aşağıdaki çıktı türleri etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbeef-117">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="bbeef-118">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bbeef-118">PSVirtualMachine</span></span>
- <span data-ttu-id="bbeef-119">`PSVirtualMachine` nesnesinin `DataDiskNames` ve `NetworkInterfaceIDs` üst düzey özellikleri çıktı türünden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bbeef-119">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="bbeef-120">Bu özelliklere zaten `PSVirtualMachine` nesnesinin `StorageProfile` ve `NetworkProfile` özelliklerinden erişilebiliyordu ve bundan sonra bu şekilde erişilmesi gerekecek.</span><span class="sxs-lookup"><span data-stu-id="bbeef-120">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="bbeef-121">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="bbeef-121">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="bbeef-122">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-122">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="bbeef-123">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbeef-123">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="bbeef-124">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="bbeef-124">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="bbeef-125">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="bbeef-126">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="bbeef-126">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="bbeef-127">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-127">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="bbeef-128">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-128">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="bbeef-129">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbeef-129">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="bbeef-130">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="bbeef-130">Get-AzureRmUsage</span></span>
- <span data-ttu-id="bbeef-131">Bu cmdlet kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bbeef-131">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="bbeef-132">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbeef-132">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="bbeef-133">Bu cmdlet’in tek nesne içeren bir liste şeklindeki çıktısı, requestId’yi ve durum kodunu içeren tek bir nesne olarak değişitirildi.</span><span class="sxs-lookup"><span data-stu-id="bbeef-133">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
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
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="bbeef-134">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbeef-134">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="bbeef-135">Bu cmdlet kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bbeef-135">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="bbeef-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbeef-136">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="bbeef-137">Bu cmdlet’in çıktısının (nesne listesi) her bir öğesi, `{ Id, Location, Name, Tags, Properties }` yapısına sahip nesneler döndürmek yerine bir Azure Kaynağının tüm özniteliklerine ek olarak en üst düzeydeki bir AlertRuleResource’un tüm özniteliklerinden oluşan `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` yapısına sahip nesneler döndürecek şekilde düzleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bbeef-137">Each element of the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
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
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="bbeef-138">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bbeef-138">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="bbeef-139">`AutoscaleSettingResourceName` alanı her zaman `Name` alanıyla aynı değere sahip olduğundan kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bbeef-139">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

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
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="bbeef-140">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="bbeef-140">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="bbeef-141">Bu cmdlet'in `Boolean` olan çıktısı, `RequestId` ve `StatusCode` içeren bir nesne olarak değiştirilecek</span><span class="sxs-lookup"><span data-stu-id="bbeef-141">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

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
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="bbeef-142">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="bbeef-142">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="bbeef-143">Bu cmdlet’in requestId, durum kodu ve güncelleştirilmiş ya da yeni oluşturulmuş kaynağı içeren bir nesne şeklindeki çıktısı değiştirilecek</span><span class="sxs-lookup"><span data-stu-id="bbeef-143">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
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
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="bbeef-144">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="bbeef-144">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="bbeef-145">Komut `Update-AzureRmDiagnosticSettings` olarak yeniden adlandırılacak</span><span class="sxs-lookup"><span data-stu-id="bbeef-145">The command is going to be renamed to `Update-AzureRmDiagnosticSettings`</span></span>

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="bbeef-146">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-146">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="bbeef-147">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbeef-147">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="bbeef-148">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bbeef-148">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="bbeef-149">`EnableBgp`parametresi, `boolean` yerine `string` alacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bbeef-149">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="bbeef-150">ServiceBus cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-150">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="bbeef-151">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbeef-151">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="bbeef-152">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bbeef-152">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="bbeef-153">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="bbeef-154">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bbeef-154">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="bbeef-155">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-155">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="bbeef-156">Sql cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-156">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="bbeef-157">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbeef-157">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="bbeef-158">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbeef-158">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="bbeef-159">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-159">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="bbeef-160">`GracePeriodWithDataLossHour` parametresi `GracePeriodWithDataLossHours` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-160">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="bbeef-161">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbeef-161">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="bbeef-162">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-162">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="bbeef-163">`GracePeriodWithDataLossHour` parametresi `GracePeriodWithDataLossHours` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-163">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="bbeef-164">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbeef-164">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="bbeef-165">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-165">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="bbeef-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbeef-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="bbeef-167">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-167">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="bbeef-168">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbeef-168">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="bbeef-169">`PartnerResourceGroupName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-169">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="bbeef-170">`PartnerServerName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-170">`PartnerServerName` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="bbeef-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbeef-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="bbeef-172">`ExcludedDetectionType` parametresi için `Usage_Anomaly` değeri artık geçerli değil</span><span class="sxs-lookup"><span data-stu-id="bbeef-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="bbeef-173">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbeef-173">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="bbeef-174">`ExcludedDetectionType` parametresi için `Usage_Anomaly` değeri artık geçerli değil</span><span class="sxs-lookup"><span data-stu-id="bbeef-174">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="bbeef-175">Depolama cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-175">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="bbeef-176">Bu sürümden aşağıdaki çıktı türü özellikleri etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbeef-176">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="bbeef-177">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbeef-177">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="bbeef-178">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="bbeef-178">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="bbeef-179">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="bbeef-179">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="bbeef-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbeef-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="bbeef-181">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="bbeef-181">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="bbeef-182">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="bbeef-182">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="bbeef-183">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbeef-183">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="bbeef-184">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="bbeef-184">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="bbeef-185">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="bbeef-185">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="bbeef-186">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbeef-186">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="bbeef-187">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="bbeef-187">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="bbeef-188">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="bbeef-188">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="bbeef-189">Profil cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-189">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="bbeef-190">Bu sürümde aşağıdaki cmdlet’ler ve cmdlet çıktı türleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bbeef-190">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="bbeef-191">Add-AzureRmAccount bozucu değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="bbeef-191">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="bbeef-192">```EnvironmentName``` parametresi kaldırılıp ```Environment``` ile değiştirildi ve ```Environment``` artık bir ```AzureEnvironment``` nesnesi değil, bir dize alıyor</span><span class="sxs-lookup"><span data-stu-id="bbeef-192">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="bbeef-193">Select-AzureRmProfile, Import-AzureRmContext olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-193">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="bbeef-194">```Select-AzureRmProfile```, ```Import-AzureRmContext``` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-194">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="bbeef-195">Save-AzureRmProfile, Save-AzureRmContext olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-195">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="bbeef-196">```Save-AzureRmProfile```, ```Save-AzureRmContext``` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bbeef-196">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="bbeef-197">Çıktı PSAzureContext Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-197">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="bbeef-198">```TokenCache``` özelliği, bir ```byte[]``` yerine ```IAzureTokenCache``` uygulayan bir tür olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bbeef-198">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

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

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="bbeef-199">Çıktı PSAzureAccount Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-199">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="bbeef-200">```AccountType``` özelliği ```Type``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bbeef-200">The ```AccountType``` property was changed to ```Type```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="bbeef-201">Çıktı PSAzureSubscription Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-201">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="bbeef-202">```SubscriptionId``` özelliği ```Id``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bbeef-202">The ```SubscriptionId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="bbeef-203">```SubscriptionName``` özelliği ```Name``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bbeef-203">The ```SubscriptionName``` property was changed to ```Name```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="bbeef-204">Çıktı PSAzureTenant Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbeef-204">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="bbeef-205">```TenantId``` özelliği ```Id``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bbeef-205">The ```TenantId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="bbeef-206">```Domain``` özelliği ```Directory``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bbeef-206">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
