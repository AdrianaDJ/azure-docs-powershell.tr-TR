---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275219"
---
# <span data-ttu-id="d8e5e-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="d8e5e-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="d8e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e5e-103">Bir dağıtımdan çıkmak için işlem.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="d8e5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8e5e-104">SYNTAX</span></span>

### <span data-ttu-id="d8e5e-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8e5e-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e5e-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="d8e5e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8e5e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e5e-108">Bir dağıtımdan çıkmak için işlem.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="d8e5e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e5e-110">Örnek 1: yay bulut dağıtımını adıyla güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="d8e5e-111">Yay bulut dağıtımını adıyla güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="d8e5e-112">Örnek 2: yay bulut dağıtımını kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="d8e5e-113">Yay bulut dağıtımını kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="d8e5e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8e5e-114">PARAMETERS</span></span>

### <span data-ttu-id="d8e5e-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="d8e5e-115">-AppName</span></span>
<span data-ttu-id="d8e5e-116">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="d8e5e-117">-AsJob</span></span>
<span data-ttu-id="d8e5e-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="d8e5e-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="d8e5e-119">-Cpu</span></span>
<span data-ttu-id="d8e5e-120">Gerekli CPU</span><span class="sxs-lookup"><span data-stu-id="d8e5e-120">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e5e-121">-DefaultProfile</span></span>
<span data-ttu-id="d8e5e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="d8e5e-123">-EnvironmentVariable</span></span>
<span data-ttu-id="d8e5e-124">Ortam değişkenleri koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="d8e5e-124">Collection of environment variables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e5e-125">-InputObject</span></span>
<span data-ttu-id="d8e5e-126">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="d8e5e-127">-JvmOption</span></span>
<span data-ttu-id="d8e5e-128">JVM parametresi</span><span class="sxs-lookup"><span data-stu-id="d8e5e-128">JVM parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="d8e5e-129">-MemoryInGb</span></span>
<span data-ttu-id="d8e5e-130">GB cinsinden gerekli bellek boyutu</span><span class="sxs-lookup"><span data-stu-id="d8e5e-130">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8e5e-131">-Name</span></span>
<span data-ttu-id="d8e5e-132">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8e5e-133">-NoWait</span></span>
<span data-ttu-id="d8e5e-134">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="d8e5e-134">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e5e-135">-ResourceGroupName</span></span>
<span data-ttu-id="d8e5e-136">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d8e5e-137">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="d8e5e-138">-RuntimeVersion</span></span>
<span data-ttu-id="d8e5e-139">Çalışma zamanı sürümü</span><span class="sxs-lookup"><span data-stu-id="d8e5e-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-140">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d8e5e-140">-ServiceName</span></span>
<span data-ttu-id="d8e5e-141">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-141">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="d8e5e-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="d8e5e-143">Çoklu modül projelerinin dağıtımında kullanılacak yapının seçici.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="d8e5e-144">Bu, hedef modülün/projenin göreli yoludur.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-144">This should bethe relative path to the target module/project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="d8e5e-145">-SourceRelativePath</span></span>
<span data-ttu-id="d8e5e-146">Kaynağı depolayan depolamanın göreli yolu</span><span class="sxs-lookup"><span data-stu-id="d8e5e-146">Relative path of the storage which stores the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d8e5e-147">-SourceType</span></span>
<span data-ttu-id="d8e5e-148">Karşıya yüklenen kaynak türü</span><span class="sxs-lookup"><span data-stu-id="d8e5e-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="d8e5e-149">-SourceVersion</span></span>
<span data-ttu-id="d8e5e-150">Kaynak sürümü</span><span class="sxs-lookup"><span data-stu-id="d8e5e-150">Version of the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-151">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d8e5e-151">-SubscriptionId</span></span>
<span data-ttu-id="d8e5e-152">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8e5e-153">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-153">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e5e-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8e5e-154">-Confirm</span></span>
<span data-ttu-id="d8e5e-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e5e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e5e-156">-WhatIf</span></span>
<span data-ttu-id="d8e5e-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e5e-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e5e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e5e-159">CommonParameters</span></span>
<span data-ttu-id="d8e5e-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e5e-161">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e5e-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8e5e-162">INPUTS</span></span>

### <span data-ttu-id="d8e5e-163">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="d8e5e-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d8e5e-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8e5e-164">OUTPUTS</span></span>

### <span data-ttu-id="d8e5e-165">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20200701. ıdeploymentresource</span><span class="sxs-lookup"><span data-stu-id="d8e5e-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="d8e5e-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8e5e-166">NOTES</span></span>

<span data-ttu-id="d8e5e-167">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d8e5e-167">ALIASES</span></span>

<span data-ttu-id="d8e5e-168">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d8e5e-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8e5e-169">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8e5e-170">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8e5e-171">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d8e5e-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8e5e-172">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d8e5e-173">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d8e5e-174">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d8e5e-175">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d8e5e-176">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d8e5e-177">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d8e5e-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8e5e-178">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="d8e5e-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d8e5e-179">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d8e5e-180">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d8e5e-181">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d8e5e-182">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d8e5e-183">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d8e5e-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d8e5e-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8e5e-184">RELATED LINKS</span></span>

