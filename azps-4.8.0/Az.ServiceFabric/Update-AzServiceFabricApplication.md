---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: 779561ee3ff0a0b687104bd828890c314612f100
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268779"
---
# <span data-ttu-id="bf9a1-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bf9a1-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="bf9a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9a1-103">Hizmet dokusu uygulamasını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-103">Update a service fabric application.</span></span> <span data-ttu-id="bf9a1-104">Bu, uygulama parametrelerini güncellemesine ve/veya uygulama yükseltmesini tetikleyecek uygulama türü sürümünü yükseltmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="bf9a1-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf9a1-105">SYNTAX</span></span>

### <span data-ttu-id="bf9a1-106">ByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf9a1-106">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf9a1-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="bf9a1-107">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf9a1-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf9a1-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9a1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf9a1-109">DESCRIPTION</span></span>
<span data-ttu-id="bf9a1-110">Bu cmdlet, uygulama parametrelerini güncelleştirmek ve uygulama türü sürümünü güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="bf9a1-111">Parametre güncelleştirmesi yalnızca ARM tarafında yalnızca yeni bir tür sürümü kullanıldığında komut bir uygulama yükseltmesini tetikleyecektir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="bf9a1-112">Belirtilen tür sürümü kümede **Yeni-AzServiceFabricApplicationTypeVersion** kullanılarak oluşturulmuş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="bf9a1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf9a1-113">EXAMPLES</span></span>

### <span data-ttu-id="bf9a1-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf9a1-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="bf9a1-115">Bu örnek, tür sürümünü **New-AzServiceFabricApplicationTypeVersion** ile oluşturulan "v2" olarak güncelleştirmek için bir uygulama yükseltmesi başlatacak.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="bf9a1-116">Kullanılan uygulama parametreleri uygulama bildiriminde tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="bf9a1-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bf9a1-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="bf9a1-118">Bu örnek, uygulama için en az ve en fazla düğüm sınırlaması sayısını güncelleştirecek.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="bf9a1-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="bf9a1-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="bf9a1-120">Bu örnek, tür sürümünü "v2" olarak güncelleştirmek için bir uygulama yükseltmesi başlatacak ve aynı zamanda geçerli yükseltmeden geçerli olacak bazı yükseltme ilkesi parametrelerini de ayarlıyor.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="bf9a1-121">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="bf9a1-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="bf9a1-122">Bu örnek, uygulama parametrelerini güncelleştirir, ancak bu değişiklikler uygulamanın sonraki sürümü yükseltilinceye kadar geçerlilik kazanır.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="bf9a1-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf9a1-123">PARAMETERS</span></span>

### <span data-ttu-id="bf9a1-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="bf9a1-124">-ApplicationParameter</span></span>
<span data-ttu-id="bf9a1-125">Uygulama parametrelerini anahtar/değer çiftleri olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="bf9a1-126">Bu parametreler uygulama bildiriminde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-126">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bf9a1-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="bf9a1-128">Uygulama türü sürümünü belirtme</span><span class="sxs-lookup"><span data-stu-id="bf9a1-128">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-129">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bf9a1-129">-ClusterName</span></span>
<span data-ttu-id="bf9a1-130">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="bf9a1-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="bf9a1-132">Sağlık değerlendirmesi sırasında uyarı durumu olayının hata olayı olarak değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9a1-133">-DefaultProfile</span></span>
<span data-ttu-id="bf9a1-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-135">-Defaultservicetypemaxyüztunhealthypartitionsperservice</span><span class="sxs-lookup"><span data-stu-id="bf9a1-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="bf9a1-136">İzlenen yükseltme için kullanılacak varsayılan hizmet türü için sistem durumu ilkesinin izin verdiği hizmet başına en yüksek disk bölümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-137">-Defaultservicetypemaxyüztunhealthyreplicasperpartition</span><span class="sxs-lookup"><span data-stu-id="bf9a1-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="bf9a1-138">İzlenen yükseltme için kullanılacak varsayılan hizmet türü için sistem durumu ilkesinin izin verdiği hizmet başına en fazla çoğaltma sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="bf9a1-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="bf9a1-140">İzlenen yükseltme için kullanılacak varsayılan hizmet türü için sistem durumu ilkesinin izin verdiği en yüksek hizmet sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-141">-HataDurumunda eylemi</span><span class="sxs-lookup"><span data-stu-id="bf9a1-141">-FailureAction</span></span>
<span data-ttu-id="bf9a1-142">İzlenen yükseltme başarısız olursa gerçekleştirilecek eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="bf9a1-143">Bu parametre için kabul edilebilir değerler geri alma veya el Ile.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="bf9a1-144">-ForceRestart</span></span>
<span data-ttu-id="bf9a1-145">Yükseltme yalnızca yapılandırma değişikliği olsa bile hizmet ana bilgisayarının yeniden başlayacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="bf9a1-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="bf9a1-147">Önceki sistem durumu denetiminin başarısız olması durumunda, hizmet yapısı sistem durumunu yeniden denemeden önce saniye cinsinden süreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="bf9a1-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="bf9a1-149">Sonraki yükseltme etki alanına geçmeden veya yükseltmeyi tamamlamadan önce uygulamanın kararlı olduğunu doğrulamak için hizmet yapınızın süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="bf9a1-150">Bu bekleme süresi, sistem durumu denetimi gerçekleştirildikten sonra sistem durumu saptanmaz değişikliklerini engeller.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="bf9a1-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="bf9a1-152">Yükseltme etki alanındaki yükseltmeyi bitirdikten sonra, hizmet dokun ilk sistem durumu denetimini gerçekleştirmeden önce bekleyeceği süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf9a1-153">-InputObject</span></span>
<span data-ttu-id="bf9a1-154">Uygulama kaynağı.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-154">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="bf9a1-155">-MaximumNodeCount</span></span>
<span data-ttu-id="bf9a1-156">Uygulamanın yerleştirileceği en fazla düğüm sayısını belirtir</span><span class="sxs-lookup"><span data-stu-id="bf9a1-156">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="bf9a1-157">-MinimumNodeCount</span></span>
<span data-ttu-id="bf9a1-158">Bu uygulama için hizmet yapınızın kapasiteyi ayırabileceği en az düğüm sayısını belirtir</span><span class="sxs-lookup"><span data-stu-id="bf9a1-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf9a1-159">-Name</span></span>
<span data-ttu-id="bf9a1-160">Uygulamanın adını belirtme</span><span class="sxs-lookup"><span data-stu-id="bf9a1-160">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9a1-161">-ResourceGroupName</span></span>
<span data-ttu-id="bf9a1-162">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-162">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-163">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf9a1-163">-ResourceId</span></span>
<span data-ttu-id="bf9a1-164">Uygulamanın Kolonu.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-164">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="bf9a1-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="bf9a1-166">Aşağıdaki biçimde, karma tablo olarak farklı hizmet türleri için kullanılacak sistem durumu ilkesinin haritasını belirtir: @ {"ServiceTypeName": "Maxyüztunhealthypartitionsperservice, Maxyüztunhealthyreplicasperpartition, Maxyüztunhealthyservices"}.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="bf9a1-167">Örneğin: @ {"ServiceTypeName01" = "5, 10, 5"; "ServiceTypeName02" = "5, 5, 5"}</span><span class="sxs-lookup"><span data-stu-id="bf9a1-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="bf9a1-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="bf9a1-169">Kümedeki düğümlerde dağıtılmış olan uygulama örneklerinin en yüksek yüzdesini, kümenin uygulama durumu durumundan önce hata durumu olmadan önce hatalı olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="bf9a1-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="bf9a1-171">Hizmet yapınızın tek bir yükseltme etki alanını yükseltmeye yönelik en uzun süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="bf9a1-172">Bu süre sonunda yükseltme başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-172">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-173">-Yükseltme Derizerepsetchecktimeoutsec</span><span class="sxs-lookup"><span data-stu-id="bf9a1-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="bf9a1-174">Hizmet yapısı yükseltmeye devam etmeden önce, hizmet yapısı için hizmetin güvenli bir duruma yeniden yapılandırılacağını bekleyen en uzun süreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="bf9a1-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="bf9a1-176">Hizmet yapının tüm yükseltme için aldığı en uzun süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="bf9a1-177">Bu süre sonunda yükseltme başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-177">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-178">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf9a1-178">-Confirm</span></span>
<span data-ttu-id="bf9a1-179">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-179">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9a1-180">-WhatIf</span></span>
<span data-ttu-id="bf9a1-181">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9a1-182">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-182">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9a1-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9a1-183">CommonParameters</span></span>
<span data-ttu-id="bf9a1-184">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9a1-185">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9a1-186">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf9a1-186">INPUTS</span></span>

### <span data-ttu-id="bf9a1-187">System. String</span><span class="sxs-lookup"><span data-stu-id="bf9a1-187">System.String</span></span>

### <span data-ttu-id="bf9a1-188">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="bf9a1-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="bf9a1-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf9a1-189">OUTPUTS</span></span>

### <span data-ttu-id="bf9a1-190">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="bf9a1-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="bf9a1-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf9a1-191">NOTES</span></span>

## <span data-ttu-id="bf9a1-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf9a1-192">RELATED LINKS</span></span>
