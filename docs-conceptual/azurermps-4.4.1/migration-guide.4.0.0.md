# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="69bed-101">Microsoft Azure PowerShell 4.0.0 için bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-101">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

<span data-ttu-id="69bed-102">Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="69bed-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="69bed-103">Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır.</span><span class="sxs-lookup"><span data-stu-id="69bed-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="69bed-104">Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="69bed-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="69bed-105">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="69bed-105">Table of Contents</span></span>

- [<span data-ttu-id="69bed-106">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-106">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="69bed-107">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-107">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="69bed-108">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-108">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="69bed-109">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-109">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="69bed-110">ServiceBus cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-110">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="69bed-111">Sql cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-111">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="69bed-112">Depolama cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-112">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="69bed-113">Profil cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-113">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="69bed-114">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-114">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="69bed-115">Bu sürümden aşağıdaki çıktı türleri etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="69bed-115">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="69bed-116">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="69bed-116">PSVirtualMachine</span></span>
- <span data-ttu-id="69bed-117">`PSVirtualMachine` nesnesinin `DataDiskNames` ve `NetworkInterfaceIDs` üst düzey özellikleri çıktı türünden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="69bed-117">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="69bed-118">Bu özelliklere zaten `PSVirtualMachine` nesnesinin `StorageProfile` ve `NetworkProfile` özelliklerinden erişilebiliyordu ve bundan sonra bu şekilde erişilmesi gerekecek.</span><span class="sxs-lookup"><span data-stu-id="69bed-118">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="69bed-119">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="69bed-119">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="69bed-120">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-120">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="69bed-121">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="69bed-121">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="69bed-122">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="69bed-122">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="69bed-123">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-123">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="69bed-124">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="69bed-124">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="69bed-125">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="69bed-126">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-126">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="69bed-127">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="69bed-127">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="69bed-128">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="69bed-128">Get-AzureRmUsage</span></span>
- <span data-ttu-id="69bed-129">Bu cmdlet kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="69bed-129">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="69bed-130">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="69bed-130">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="69bed-131">Bu cmdlet’in tek nesne içeren bir liste şeklindeki çıktısı, requestId’yi ve durum kodunu içeren tek bir nesne olarak değişitirildi.</span><span class="sxs-lookup"><span data-stu-id="69bed-131">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell
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
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="69bed-132">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="69bed-132">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="69bed-133">Bu cmdlet kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="69bed-133">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="69bed-134">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="69bed-134">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="69bed-135">Bu cmdlet’in çıktısının (nesne listesi) her bir öğesi, `{ Id, Location, Name, Tags, Properties }` yapısına sahip nesneler döndürmek yerine bir Azure Kaynağının tüm özniteliklerine ek olarak en üst düzeydeki bir AlertRuleResource’un tüm özniteliklerinden oluşan `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` yapısına sahip nesneler döndürecek şekilde düzleştirildi.</span><span class="sxs-lookup"><span data-stu-id="69bed-135">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell
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
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="69bed-136">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="69bed-136">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="69bed-137">`AutoscaleSettingResourceName` alanı her zaman `Name` alanıyla aynı değere sahip olduğundan kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="69bed-137">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell
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
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="69bed-138">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="69bed-138">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="69bed-139">Bu cmdlet'in `Boolean` olan çıktısı, `RequestId` ve `StatusCode` içeren bir nesne olarak değiştirilecek</span><span class="sxs-lookup"><span data-stu-id="69bed-139">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell
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
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="69bed-140">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="69bed-140">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="69bed-141">Bu cmdlet’in requestId, durum kodu ve güncelleştirilmiş ya da yeni oluşturulmuş kaynağı içeren bir nesne şeklindeki çıktısı değiştirilecek</span><span class="sxs-lookup"><span data-stu-id="69bed-141">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="69bed-142">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="69bed-142">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="69bed-143">Komut `Update-AzureRmDiagnsoticSettings` olarak yeniden adlandırılacak</span><span class="sxs-lookup"><span data-stu-id="69bed-143">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="69bed-144">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-144">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="69bed-145">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="69bed-145">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="69bed-146">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="69bed-146">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="69bed-147">`EnableBgp`parametresi, `boolean` yerine `string` alacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="69bed-147">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="69bed-148">ServiceBus cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-148">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="69bed-149">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="69bed-149">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="69bed-150">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="69bed-150">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="69bed-151">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-151">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="69bed-152">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="69bed-152">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="69bed-153">`ResourceGroupName` özelliği `NamespaceAttributes` çıktı türünden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="69bed-154">Sql cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-154">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="69bed-155">Bu sürümden aşağıdaki cmdlet’ler etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="69bed-155">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="69bed-156">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="69bed-156">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="69bed-157">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-157">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="69bed-158">`GracePeriodWithDataLossHour` parametresi `GracePeriodWithDataLossHours` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-158">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="69bed-159">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="69bed-159">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="69bed-160">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-160">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="69bed-161">`GracePeriodWithDataLossHour` parametresi `GracePeriodWithDataLossHours` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-161">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="69bed-162">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="69bed-162">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="69bed-163">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-163">`Tag` parameter has been removed</span></span>

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="69bed-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="69bed-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="69bed-165">`Tag` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-165">`Tag` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="69bed-166">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="69bed-166">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="69bed-167">`PartnerResourceGroupName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-167">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="69bed-168">`PartnerServerName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-168">`PartnerServerName` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="69bed-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69bed-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="69bed-170">`ExcludedDetectionType` parametresi için `Usage_Anomaly` değeri artık geçerli değil</span><span class="sxs-lookup"><span data-stu-id="69bed-170">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="69bed-171">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69bed-171">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="69bed-172">`ExcludedDetectionType` parametresi için `Usage_Anomaly` değeri artık geçerli değil</span><span class="sxs-lookup"><span data-stu-id="69bed-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="69bed-173">Depolama cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-173">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="69bed-174">Bu sürümden aşağıdaki çıktı türü özellikleri etkilenmiştir:</span><span class="sxs-lookup"><span data-stu-id="69bed-174">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="69bed-175">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="69bed-175">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="69bed-176">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="69bed-176">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="69bed-177">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="69bed-177">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="69bed-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="69bed-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="69bed-179">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="69bed-179">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="69bed-180">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="69bed-180">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="69bed-181">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="69bed-181">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="69bed-182">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="69bed-182">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="69bed-183">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="69bed-183">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="69bed-184">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="69bed-184">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="69bed-185">Aşağıdaki özellikler bu türden kaldırıldı (_not_: Bunlar hala `DefaultRequestOptions` özelliğinde bulunabilir):</span><span class="sxs-lookup"><span data-stu-id="69bed-185">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="69bed-186">Bu değişiklik, aşağıdaki cmdlet etkiler:</span><span class="sxs-lookup"><span data-stu-id="69bed-186">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell
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

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="69bed-187">Profil cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-187">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="69bed-188">Bu sürümde aşağıdaki cmdlet’ler ve cmdlet çıktı türleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="69bed-188">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="69bed-189">Add-AzureRmAccount bozucu değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="69bed-189">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="69bed-190">```EnvironmentName``` parametresi kaldırılıp ```Environment``` ile değiştirildi ve ```Environment``` artık bir ```AzureEnvironment``` nesnesi değil, bir dize alıyor</span><span class="sxs-lookup"><span data-stu-id="69bed-190">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="69bed-191">Select-AzureRmProfile, Import-AzureRmContext olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-191">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="69bed-192">```Select-AzureRmProfile```, ```Import-AzureRmContext``` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-192">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="69bed-193">Save-AzureRmProfile, Save-AzureRmContext olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-193">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="69bed-194">```Save-AzureRmProfile```, ```Save-AzureRmContext``` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="69bed-194">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="69bed-195">Çıktı PSAzureContext Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-195">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="69bed-196">```TokenCache``` özelliği, bir ```byte[]``` yerine ```IAzureTokenCache``` uygulayan bir tür olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="69bed-196">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="69bed-197">Çıktı PSAzureAccount Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-197">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="69bed-198">```AccountType``` özelliği ```Type``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="69bed-198">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="69bed-199">Çıktı PSAzureSubscription Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-199">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="69bed-200">```SubscriptionId``` özelliği ```Id``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="69bed-200">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell
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

- <span data-ttu-id="69bed-201">```SubscriptionName``` özelliği ```Name``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="69bed-201">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell
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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="69bed-202">Çıktı PSAzureTenant Türünde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="69bed-202">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="69bed-203">```TenantId``` özelliği ```Id``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="69bed-203">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell
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

- <span data-ttu-id="69bed-204">```Domain``` özelliği ```Directory``` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="69bed-204">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
