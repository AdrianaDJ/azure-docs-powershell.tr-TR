---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268764"
---
# <span data-ttu-id="daa97-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="daa97-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="daa97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa97-102">SYNOPSIS</span></span>
<span data-ttu-id="daa97-103">Bir dağıtımdan çıkmak için işlem.</span><span class="sxs-lookup"><span data-stu-id="daa97-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="daa97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="daa97-104">SYNTAX</span></span>

### <span data-ttu-id="daa97-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="daa97-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="daa97-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="daa97-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="daa97-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="daa97-107">DESCRIPTION</span></span>
<span data-ttu-id="daa97-108">Bir dağıtımdan çıkmak için işlem.</span><span class="sxs-lookup"><span data-stu-id="daa97-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="daa97-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="daa97-109">EXAMPLES</span></span>

### <span data-ttu-id="daa97-110">Örnek 1: yay bulut dağıtımını adıyla güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="daa97-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="daa97-111">Yay bulut dağıtımını adıyla güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="daa97-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="daa97-112">Örnek 2: yay bulut dağıtımını kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="daa97-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="daa97-113">Yay bulut dağıtımını kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="daa97-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="daa97-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="daa97-114">PARAMETERS</span></span>

### <span data-ttu-id="daa97-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="daa97-115">-AppName</span></span>
<span data-ttu-id="daa97-116">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="daa97-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="daa97-117">-AsJob</span></span>
<span data-ttu-id="daa97-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="daa97-118">Run the command as a job</span></span>

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

### <span data-ttu-id="daa97-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="daa97-119">-Cpu</span></span>
<span data-ttu-id="daa97-120">Gerekli CPU</span><span class="sxs-lookup"><span data-stu-id="daa97-120">Required CPU</span></span>

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

### <span data-ttu-id="daa97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa97-121">-DefaultProfile</span></span>
<span data-ttu-id="daa97-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="daa97-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa97-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="daa97-123">-EnvironmentVariable</span></span>
<span data-ttu-id="daa97-124">Ortam değişkenleri koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="daa97-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="daa97-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daa97-125">-InputObject</span></span>
<span data-ttu-id="daa97-126">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="daa97-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="daa97-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="daa97-127">-InstanceCount</span></span>
<span data-ttu-id="daa97-128">Örnek sayısı</span><span class="sxs-lookup"><span data-stu-id="daa97-128">Instance count</span></span>

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

### <span data-ttu-id="daa97-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="daa97-129">-JvmOption</span></span>
<span data-ttu-id="daa97-130">JVM parametresi</span><span class="sxs-lookup"><span data-stu-id="daa97-130">JVM parameter</span></span>

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

### <span data-ttu-id="daa97-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="daa97-131">-MemoryInGb</span></span>
<span data-ttu-id="daa97-132">GB cinsinden gerekli bellek boyutu</span><span class="sxs-lookup"><span data-stu-id="daa97-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="daa97-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="daa97-133">-Name</span></span>
<span data-ttu-id="daa97-134">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="daa97-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="daa97-135">-NoWait</span></span>
<span data-ttu-id="daa97-136">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="daa97-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="daa97-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa97-137">-ResourceGroupName</span></span>
<span data-ttu-id="daa97-138">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="daa97-139">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="daa97-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="daa97-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="daa97-140">-RuntimeVersion</span></span>
<span data-ttu-id="daa97-141">Çalışma zamanı sürümü</span><span class="sxs-lookup"><span data-stu-id="daa97-141">Runtime version</span></span>

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

### <span data-ttu-id="daa97-142">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="daa97-142">-ServiceName</span></span>
<span data-ttu-id="daa97-143">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="daa97-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="daa97-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="daa97-145">Çoklu modül projelerinin dağıtımında kullanılacak yapının seçici.</span><span class="sxs-lookup"><span data-stu-id="daa97-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="daa97-146">Bu, hedef modülün/projenin göreli yoludur.</span><span class="sxs-lookup"><span data-stu-id="daa97-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="daa97-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="daa97-147">-SourceRelativePath</span></span>
<span data-ttu-id="daa97-148">Kaynağı depolayan depolamanın göreli yolu</span><span class="sxs-lookup"><span data-stu-id="daa97-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="daa97-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="daa97-149">-SourceType</span></span>
<span data-ttu-id="daa97-150">Karşıya yüklenen kaynak türü</span><span class="sxs-lookup"><span data-stu-id="daa97-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="daa97-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="daa97-151">-SourceVersion</span></span>
<span data-ttu-id="daa97-152">Kaynak sürümü</span><span class="sxs-lookup"><span data-stu-id="daa97-152">Version of the source</span></span>

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

### <span data-ttu-id="daa97-153">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="daa97-153">-SubscriptionId</span></span>
<span data-ttu-id="daa97-154">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="daa97-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="daa97-155">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="daa97-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="daa97-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="daa97-156">-Confirm</span></span>
<span data-ttu-id="daa97-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="daa97-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa97-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa97-158">-WhatIf</span></span>
<span data-ttu-id="daa97-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="daa97-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daa97-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="daa97-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa97-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa97-161">CommonParameters</span></span>
<span data-ttu-id="daa97-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="daa97-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa97-163">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="daa97-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa97-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="daa97-164">INPUTS</span></span>

### <span data-ttu-id="daa97-165">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="daa97-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="daa97-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="daa97-166">OUTPUTS</span></span>

### <span data-ttu-id="daa97-167">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20190501Preview. ıdeploymentresource</span><span class="sxs-lookup"><span data-stu-id="daa97-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="daa97-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="daa97-168">NOTES</span></span>

<span data-ttu-id="daa97-169">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="daa97-169">ALIASES</span></span>

<span data-ttu-id="daa97-170">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="daa97-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="daa97-171">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="daa97-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="daa97-172">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="daa97-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="daa97-173">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="daa97-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="daa97-174">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="daa97-175">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="daa97-176">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="daa97-177">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="daa97-178">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="daa97-179">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="daa97-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="daa97-180">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="daa97-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="daa97-181">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="daa97-182">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="daa97-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="daa97-183">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="daa97-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="daa97-184">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="daa97-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="daa97-185">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="daa97-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="daa97-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="daa97-186">RELATED LINKS</span></span>

