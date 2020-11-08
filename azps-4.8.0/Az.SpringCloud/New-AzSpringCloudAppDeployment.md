---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0669371f589722e3da18e554df98dbf7d193ccc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273930"
---
# <span data-ttu-id="077f5-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="077f5-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="077f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="077f5-102">SYNOPSIS</span></span>
<span data-ttu-id="077f5-103">Yeni bir dağıtım oluşturun veya çıkış dağıtımını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="077f5-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="077f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="077f5-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="077f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="077f5-105">DESCRIPTION</span></span>
<span data-ttu-id="077f5-106">Yeni bir dağıtım oluşturun veya çıkış dağıtımını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="077f5-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="077f5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="077f5-107">EXAMPLES</span></span>

### <span data-ttu-id="077f5-108">Örnek 1: örnek 1: yay bulut dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="077f5-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="077f5-109">Yay bulut dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="077f5-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="077f5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="077f5-110">PARAMETERS</span></span>

### <span data-ttu-id="077f5-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="077f5-111">-AppName</span></span>
<span data-ttu-id="077f5-112">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="077f5-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077f5-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="077f5-113">-AsJob</span></span>
<span data-ttu-id="077f5-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="077f5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="077f5-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="077f5-115">-Cpu</span></span>
<span data-ttu-id="077f5-116">Gerekli CPU</span><span class="sxs-lookup"><span data-stu-id="077f5-116">Required CPU</span></span>

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

### <span data-ttu-id="077f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077f5-117">-DefaultProfile</span></span>
<span data-ttu-id="077f5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="077f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="077f5-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="077f5-119">-EnvironmentVariable</span></span>
<span data-ttu-id="077f5-120">Ortam değişkenleri koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="077f5-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="077f5-121">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="077f5-121">-InstanceCount</span></span>
<span data-ttu-id="077f5-122">Örnek sayısı</span><span class="sxs-lookup"><span data-stu-id="077f5-122">Instance count</span></span>

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

### <span data-ttu-id="077f5-123">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="077f5-123">-JvmOption</span></span>
<span data-ttu-id="077f5-124">JVM parametresi</span><span class="sxs-lookup"><span data-stu-id="077f5-124">JVM parameter</span></span>

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

### <span data-ttu-id="077f5-125">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="077f5-125">-MemoryInGb</span></span>
<span data-ttu-id="077f5-126">GB cinsinden gerekli bellek boyutu</span><span class="sxs-lookup"><span data-stu-id="077f5-126">Required Memory size in GB</span></span>

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

### <span data-ttu-id="077f5-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="077f5-127">-Name</span></span>
<span data-ttu-id="077f5-128">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="077f5-128">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077f5-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="077f5-129">-NoWait</span></span>
<span data-ttu-id="077f5-130">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="077f5-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="077f5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077f5-131">-ResourceGroupName</span></span>
<span data-ttu-id="077f5-132">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="077f5-132">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="077f5-133">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="077f5-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077f5-134">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="077f5-134">-RuntimeVersion</span></span>
<span data-ttu-id="077f5-135">Çalışma zamanı sürümü</span><span class="sxs-lookup"><span data-stu-id="077f5-135">Runtime version</span></span>

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

### <span data-ttu-id="077f5-136">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="077f5-136">-ServiceName</span></span>
<span data-ttu-id="077f5-137">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="077f5-137">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077f5-138">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="077f5-138">-SourceArtifactSelector</span></span>
<span data-ttu-id="077f5-139">Çoklu modül projelerinin dağıtımında kullanılacak yapının seçici.</span><span class="sxs-lookup"><span data-stu-id="077f5-139">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="077f5-140">Bu, hedef modülün/projenin göreli yoludur.</span><span class="sxs-lookup"><span data-stu-id="077f5-140">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="077f5-141">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="077f5-141">-SourceRelativePath</span></span>
<span data-ttu-id="077f5-142">Kaynağı depolayan depolamanın göreli yolu</span><span class="sxs-lookup"><span data-stu-id="077f5-142">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="077f5-143">-SourceType</span><span class="sxs-lookup"><span data-stu-id="077f5-143">-SourceType</span></span>
<span data-ttu-id="077f5-144">Karşıya yüklenen kaynak türü</span><span class="sxs-lookup"><span data-stu-id="077f5-144">Type of the source uploaded</span></span>

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

### <span data-ttu-id="077f5-145">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="077f5-145">-SourceVersion</span></span>
<span data-ttu-id="077f5-146">Kaynak sürümü</span><span class="sxs-lookup"><span data-stu-id="077f5-146">Version of the source</span></span>

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

### <span data-ttu-id="077f5-147">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="077f5-147">-SubscriptionId</span></span>
<span data-ttu-id="077f5-148">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="077f5-148">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="077f5-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="077f5-149">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077f5-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="077f5-150">-Confirm</span></span>
<span data-ttu-id="077f5-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="077f5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077f5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077f5-152">-WhatIf</span></span>
<span data-ttu-id="077f5-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="077f5-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077f5-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="077f5-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077f5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077f5-155">CommonParameters</span></span>
<span data-ttu-id="077f5-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="077f5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077f5-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="077f5-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077f5-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="077f5-158">INPUTS</span></span>

## <span data-ttu-id="077f5-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="077f5-159">OUTPUTS</span></span>

### <span data-ttu-id="077f5-160">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20190501Preview. ıdeploymentresource</span><span class="sxs-lookup"><span data-stu-id="077f5-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="077f5-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="077f5-161">NOTES</span></span>

<span data-ttu-id="077f5-162">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="077f5-162">ALIASES</span></span>

## <span data-ttu-id="077f5-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="077f5-163">RELATED LINKS</span></span>

