---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275243"
---
# <span data-ttu-id="2e28f-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="2e28f-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="2e28f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e28f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e28f-103">Dağıtım ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="2e28f-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="2e28f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e28f-104">SYNTAX</span></span>

### <span data-ttu-id="2e28f-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e28f-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e28f-106">Al</span><span class="sxs-lookup"><span data-stu-id="2e28f-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e28f-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="2e28f-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e28f-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="2e28f-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2e28f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e28f-109">DESCRIPTION</span></span>
<span data-ttu-id="2e28f-110">Dağıtım ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="2e28f-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="2e28f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e28f-111">EXAMPLES</span></span>

### <span data-ttu-id="2e28f-112">Örnek 1: yay bulut uygulaması Deploymeng 'yi ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="2e28f-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
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

<span data-ttu-id="2e28f-113">Yay bulut uygulaması Deploymeng 'yi ada göre edinin.</span><span class="sxs-lookup"><span data-stu-id="2e28f-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="2e28f-114">Örnek 2: verilen yay bulutu uygulamasının altındaki tüm dağıtımı listeler.</span><span class="sxs-lookup"><span data-stu-id="2e28f-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="2e28f-115">Verilen yay bulutu uygulamasının altındaki tüm dağıtımı listeler.</span><span class="sxs-lookup"><span data-stu-id="2e28f-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="2e28f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e28f-116">PARAMETERS</span></span>

### <span data-ttu-id="2e28f-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="2e28f-117">-AppName</span></span>
<span data-ttu-id="2e28f-118">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e28f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e28f-119">-DefaultProfile</span></span>
<span data-ttu-id="2e28f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e28f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e28f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e28f-121">-InputObject</span></span>
<span data-ttu-id="2e28f-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e28f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e28f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e28f-123">-Name</span></span>
<span data-ttu-id="2e28f-124">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e28f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e28f-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e28f-126">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2e28f-127">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e28f-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e28f-128">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="2e28f-128">-ServiceName</span></span>
<span data-ttu-id="2e28f-129">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e28f-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2e28f-130">-SubscriptionId</span></span>
<span data-ttu-id="2e28f-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="2e28f-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e28f-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2e28f-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e28f-133">-Version</span><span class="sxs-lookup"><span data-stu-id="2e28f-133">-Version</span></span>
<span data-ttu-id="2e28f-134">Listelenen dağıtımlar sürümü</span><span class="sxs-lookup"><span data-stu-id="2e28f-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e28f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e28f-135">CommonParameters</span></span>
<span data-ttu-id="2e28f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e28f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e28f-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2e28f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e28f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e28f-138">INPUTS</span></span>

### <span data-ttu-id="2e28f-139">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="2e28f-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2e28f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e28f-140">OUTPUTS</span></span>

### <span data-ttu-id="2e28f-141">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20200701. ıdeploymentresource</span><span class="sxs-lookup"><span data-stu-id="2e28f-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="2e28f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e28f-142">NOTES</span></span>

<span data-ttu-id="2e28f-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="2e28f-143">ALIASES</span></span>

<span data-ttu-id="2e28f-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="2e28f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e28f-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2e28f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e28f-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e28f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e28f-147">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="2e28f-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e28f-148">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2e28f-149">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2e28f-150">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2e28f-151">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2e28f-152">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2e28f-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="2e28f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e28f-154">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="2e28f-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2e28f-155">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2e28f-156">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e28f-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2e28f-157">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="2e28f-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2e28f-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="2e28f-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2e28f-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2e28f-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2e28f-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e28f-160">RELATED LINKS</span></span>

