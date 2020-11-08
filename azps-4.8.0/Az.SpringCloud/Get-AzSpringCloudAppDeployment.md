---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273942"
---
# <span data-ttu-id="6130d-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="6130d-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="6130d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6130d-102">SYNOPSIS</span></span>
<span data-ttu-id="6130d-103">Dağıtım ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="6130d-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="6130d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6130d-104">SYNTAX</span></span>

### <span data-ttu-id="6130d-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6130d-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6130d-106">Al</span><span class="sxs-lookup"><span data-stu-id="6130d-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6130d-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6130d-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6130d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6130d-108">DESCRIPTION</span></span>
<span data-ttu-id="6130d-109">Dağıtım ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="6130d-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="6130d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6130d-110">EXAMPLES</span></span>

### <span data-ttu-id="6130d-111">Örnek 1: yay bulut uygulaması Deploymeng 'yi ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="6130d-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="6130d-112">Yay bulut uygulaması Deploymeng 'yi ada göre edinin.</span><span class="sxs-lookup"><span data-stu-id="6130d-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="6130d-113">Örnek 2: verilen yay bulutu uygulamasının altındaki tüm dağıtımı listeler.</span><span class="sxs-lookup"><span data-stu-id="6130d-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="6130d-114">Verilen yay bulutu uygulamasının altındaki tüm dağıtımı listeler.</span><span class="sxs-lookup"><span data-stu-id="6130d-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="6130d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6130d-115">PARAMETERS</span></span>

### <span data-ttu-id="6130d-116">-AppName</span><span class="sxs-lookup"><span data-stu-id="6130d-116">-AppName</span></span>
<span data-ttu-id="6130d-117">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="6130d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6130d-118">-DefaultProfile</span></span>
<span data-ttu-id="6130d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6130d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6130d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6130d-120">-InputObject</span></span>
<span data-ttu-id="6130d-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6130d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6130d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6130d-122">-Name</span></span>
<span data-ttu-id="6130d-123">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="6130d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6130d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6130d-125">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6130d-126">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6130d-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6130d-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="6130d-127">-ServiceName</span></span>
<span data-ttu-id="6130d-128">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="6130d-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6130d-129">-SubscriptionId</span></span>
<span data-ttu-id="6130d-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="6130d-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6130d-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6130d-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6130d-132">-Version</span><span class="sxs-lookup"><span data-stu-id="6130d-132">-Version</span></span>
<span data-ttu-id="6130d-133">Listelenen dağıtımlar sürümü</span><span class="sxs-lookup"><span data-stu-id="6130d-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6130d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6130d-134">CommonParameters</span></span>
<span data-ttu-id="6130d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6130d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6130d-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6130d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6130d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6130d-137">INPUTS</span></span>

### <span data-ttu-id="6130d-138">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="6130d-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="6130d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6130d-139">OUTPUTS</span></span>

### <span data-ttu-id="6130d-140">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20190501Preview. ıdeploymentresource</span><span class="sxs-lookup"><span data-stu-id="6130d-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="6130d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6130d-141">NOTES</span></span>

<span data-ttu-id="6130d-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6130d-142">ALIASES</span></span>

<span data-ttu-id="6130d-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6130d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6130d-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6130d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6130d-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6130d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6130d-146">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6130d-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6130d-147">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="6130d-148">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="6130d-149">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="6130d-150">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="6130d-151">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="6130d-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6130d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6130d-153">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="6130d-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="6130d-154">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6130d-155">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6130d-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6130d-156">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6130d-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="6130d-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="6130d-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6130d-158">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6130d-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6130d-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6130d-159">RELATED LINKS</span></span>

