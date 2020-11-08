---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275242"
---
# <span data-ttu-id="4b54e-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="4b54e-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="4b54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b54e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b54e-103">Uygulama ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="4b54e-103">Get an App and its properties.</span></span>

## <span data-ttu-id="4b54e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b54e-104">SYNTAX</span></span>

### <span data-ttu-id="4b54e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b54e-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b54e-106">Al</span><span class="sxs-lookup"><span data-stu-id="4b54e-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b54e-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4b54e-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b54e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b54e-108">DESCRIPTION</span></span>
<span data-ttu-id="4b54e-109">Uygulama ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="4b54e-109">Get an App and its properties.</span></span>

## <span data-ttu-id="4b54e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b54e-110">EXAMPLES</span></span>

### <span data-ttu-id="4b54e-111">Örnek 1: yay bulut uygulamasını ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="4b54e-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="4b54e-112">Yay bulut uygulamasını ada göre edinin.</span><span class="sxs-lookup"><span data-stu-id="4b54e-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="4b54e-113">Örnek 2: verilen yay bulut hizmeti altındaki tüm uygulamayı listeleyin.</span><span class="sxs-lookup"><span data-stu-id="4b54e-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="4b54e-114">Verilen yay bulutu hizmeti altındaki tüm uygulamaları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="4b54e-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="4b54e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b54e-115">PARAMETERS</span></span>

### <span data-ttu-id="4b54e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b54e-116">-DefaultProfile</span></span>
<span data-ttu-id="4b54e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b54e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b54e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b54e-118">-InputObject</span></span>
<span data-ttu-id="4b54e-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b54e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b54e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b54e-120">-Name</span></span>
<span data-ttu-id="4b54e-121">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b54e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b54e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b54e-123">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4b54e-124">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b54e-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4b54e-125">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="4b54e-125">-ServiceName</span></span>
<span data-ttu-id="4b54e-126">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="4b54e-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4b54e-127">-SubscriptionId</span></span>
<span data-ttu-id="4b54e-128">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="4b54e-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4b54e-129">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b54e-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4b54e-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="4b54e-130">-SyncStatus</span></span>
<span data-ttu-id="4b54e-131">Eşitleme durumunu gösterir</span><span class="sxs-lookup"><span data-stu-id="4b54e-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b54e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b54e-132">CommonParameters</span></span>
<span data-ttu-id="4b54e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b54e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b54e-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b54e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b54e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b54e-135">INPUTS</span></span>

### <span data-ttu-id="4b54e-136">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="4b54e-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="4b54e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b54e-137">OUTPUTS</span></span>

### <span data-ttu-id="4b54e-138">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20200701. ıappresource</span><span class="sxs-lookup"><span data-stu-id="4b54e-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="4b54e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b54e-139">NOTES</span></span>

<span data-ttu-id="4b54e-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4b54e-140">ALIASES</span></span>

<span data-ttu-id="4b54e-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4b54e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b54e-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b54e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b54e-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b54e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b54e-144">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4b54e-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b54e-145">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="4b54e-146">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="4b54e-147">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="4b54e-148">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="4b54e-149">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="4b54e-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4b54e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b54e-151">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="4b54e-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="4b54e-152">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4b54e-153">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b54e-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4b54e-154">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4b54e-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="4b54e-155">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="4b54e-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="4b54e-156">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b54e-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4b54e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b54e-157">RELATED LINKS</span></span>

