---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275233"
---
# <span data-ttu-id="5bd13-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="5bd13-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="5bd13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd13-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd13-103">Yeni bir dağıtım oluşturun veya çıkış dağıtımını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5bd13-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="5bd13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bd13-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5bd13-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bd13-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd13-106">Yeni bir dağıtım oluşturun veya çıkış dağıtımını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5bd13-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="5bd13-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bd13-107">EXAMPLES</span></span>

### <span data-ttu-id="5bd13-108">Örnek 1: örnek 1: yay bulut dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5bd13-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="5bd13-109">Yay bulut dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5bd13-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="5bd13-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bd13-110">PARAMETERS</span></span>

### <span data-ttu-id="5bd13-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="5bd13-111">-AppName</span></span>
<span data-ttu-id="5bd13-112">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5bd13-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="5bd13-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5bd13-113">-AsJob</span></span>
<span data-ttu-id="5bd13-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="5bd13-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5bd13-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="5bd13-115">-Cpu</span></span>
<span data-ttu-id="5bd13-116">Gerekli CPU</span><span class="sxs-lookup"><span data-stu-id="5bd13-116">Required CPU</span></span>

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

### <span data-ttu-id="5bd13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd13-117">-DefaultProfile</span></span>
<span data-ttu-id="5bd13-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bd13-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd13-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="5bd13-119">-EnvironmentVariable</span></span>
<span data-ttu-id="5bd13-120">Ortam değişkenleri koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="5bd13-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="5bd13-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="5bd13-121">-JvmOption</span></span>
<span data-ttu-id="5bd13-122">JVM parametresi</span><span class="sxs-lookup"><span data-stu-id="5bd13-122">JVM parameter</span></span>

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

### <span data-ttu-id="5bd13-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="5bd13-123">-MemoryInGb</span></span>
<span data-ttu-id="5bd13-124">GB cinsinden gerekli bellek boyutu</span><span class="sxs-lookup"><span data-stu-id="5bd13-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="5bd13-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="5bd13-125">-Name</span></span>
<span data-ttu-id="5bd13-126">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5bd13-126">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="5bd13-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5bd13-127">-NoWait</span></span>
<span data-ttu-id="5bd13-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="5bd13-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5bd13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd13-129">-ResourceGroupName</span></span>
<span data-ttu-id="5bd13-130">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5bd13-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5bd13-131">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5bd13-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5bd13-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="5bd13-132">-RuntimeVersion</span></span>
<span data-ttu-id="5bd13-133">Çalışma zamanı sürümü</span><span class="sxs-lookup"><span data-stu-id="5bd13-133">Runtime version</span></span>

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

### <span data-ttu-id="5bd13-134">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="5bd13-134">-ServiceName</span></span>
<span data-ttu-id="5bd13-135">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5bd13-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="5bd13-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="5bd13-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="5bd13-137">Çoklu modül projelerinin dağıtımında kullanılacak yapının seçici.</span><span class="sxs-lookup"><span data-stu-id="5bd13-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="5bd13-138">Bu, hedef modülün/projenin göreli yoludur.</span><span class="sxs-lookup"><span data-stu-id="5bd13-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="5bd13-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="5bd13-139">-SourceRelativePath</span></span>
<span data-ttu-id="5bd13-140">Kaynağı depolayan depolamanın göreli yolu</span><span class="sxs-lookup"><span data-stu-id="5bd13-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="5bd13-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="5bd13-141">-SourceType</span></span>
<span data-ttu-id="5bd13-142">Karşıya yüklenen kaynak türü</span><span class="sxs-lookup"><span data-stu-id="5bd13-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="5bd13-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="5bd13-143">-SourceVersion</span></span>
<span data-ttu-id="5bd13-144">Kaynak sürümü</span><span class="sxs-lookup"><span data-stu-id="5bd13-144">Version of the source</span></span>

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

### <span data-ttu-id="5bd13-145">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5bd13-145">-SubscriptionId</span></span>
<span data-ttu-id="5bd13-146">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="5bd13-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5bd13-147">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5bd13-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5bd13-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="5bd13-148">-Confirm</span></span>
<span data-ttu-id="5bd13-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5bd13-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd13-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd13-150">-WhatIf</span></span>
<span data-ttu-id="5bd13-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5bd13-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd13-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5bd13-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd13-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd13-153">CommonParameters</span></span>
<span data-ttu-id="5bd13-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bd13-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd13-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5bd13-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd13-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bd13-156">INPUTS</span></span>

## <span data-ttu-id="5bd13-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bd13-157">OUTPUTS</span></span>

### <span data-ttu-id="5bd13-158">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20200701. ıdeploymentresource</span><span class="sxs-lookup"><span data-stu-id="5bd13-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="5bd13-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bd13-159">NOTES</span></span>

<span data-ttu-id="5bd13-160">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5bd13-160">ALIASES</span></span>

## <span data-ttu-id="5bd13-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bd13-161">RELATED LINKS</span></span>

