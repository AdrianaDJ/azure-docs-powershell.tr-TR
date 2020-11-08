---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275224"
---
# <span data-ttu-id="0f545-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="0f545-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="0f545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f545-102">SYNOPSIS</span></span>
<span data-ttu-id="0f545-103">Bir uygulamayı güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="0f545-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="0f545-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f545-104">SYNTAX</span></span>

### <span data-ttu-id="0f545-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f545-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0f545-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="0f545-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f545-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f545-107">DESCRIPTION</span></span>
<span data-ttu-id="0f545-108">Bir uygulamayı güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="0f545-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="0f545-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f545-109">EXAMPLES</span></span>

### <span data-ttu-id="0f545-110">Örnek 1: yay bulut uygulamasını ada göre güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="0f545-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
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

<span data-ttu-id="0f545-111">Yay bulut uygulamasını ada göre güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="0f545-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="0f545-112">Örnek 2: yay bulut uygulamasını kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="0f545-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
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

<span data-ttu-id="0f545-113">Yay bulut uygulamasını kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="0f545-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="0f545-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f545-114">PARAMETERS</span></span>

### <span data-ttu-id="0f545-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="0f545-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="0f545-116">Uygulamanın etkin dağıtımının adı</span><span class="sxs-lookup"><span data-stu-id="0f545-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="0f545-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="0f545-117">-AsJob</span></span>
<span data-ttu-id="0f545-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="0f545-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0f545-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f545-119">-DefaultProfile</span></span>
<span data-ttu-id="0f545-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f545-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f545-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="0f545-121">-Fqdn</span></span>
<span data-ttu-id="0f545-122">Tam nitelikli DNS adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="0f545-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0f545-123">-HttpsOnly</span></span>
<span data-ttu-id="0f545-124">Yalnızca https olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f545-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="0f545-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f545-125">-InputObject</span></span>
<span data-ttu-id="0f545-126">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f545-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f545-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="0f545-127">-Location</span></span>
<span data-ttu-id="0f545-128">Uygulamanın COĞRAFI konumu, her zaman üst kaynağıyla aynı olan</span><span class="sxs-lookup"><span data-stu-id="0f545-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="0f545-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f545-129">-Name</span></span>
<span data-ttu-id="0f545-130">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f545-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0f545-131">-NoWait</span></span>
<span data-ttu-id="0f545-132">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="0f545-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0f545-133">-Persistentdiskbağlamayolu</span><span class="sxs-lookup"><span data-stu-id="0f545-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="0f545-134">Kalıcı diskin bağlama yolu</span><span class="sxs-lookup"><span data-stu-id="0f545-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="0f545-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="0f545-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="0f545-136">GB cinsinden kalıcı diskin boyutu</span><span class="sxs-lookup"><span data-stu-id="0f545-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="0f545-137">-Genel</span><span class="sxs-lookup"><span data-stu-id="0f545-137">-Public</span></span>
<span data-ttu-id="0f545-138">Uygulamanın genel uç noktayı gösterir</span><span class="sxs-lookup"><span data-stu-id="0f545-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="0f545-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f545-139">-ResourceGroupName</span></span>
<span data-ttu-id="0f545-140">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0f545-141">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f545-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0f545-142">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="0f545-142">-ServiceName</span></span>
<span data-ttu-id="0f545-143">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="0f545-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0f545-144">-SubscriptionId</span></span>
<span data-ttu-id="0f545-145">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="0f545-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0f545-146">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0f545-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0f545-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="0f545-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="0f545-148">Geçici diskin bağlama yolu</span><span class="sxs-lookup"><span data-stu-id="0f545-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="0f545-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="0f545-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="0f545-150">GB cinsinden geçici diskin boyutu</span><span class="sxs-lookup"><span data-stu-id="0f545-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="0f545-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f545-151">-Confirm</span></span>
<span data-ttu-id="0f545-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f545-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f545-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f545-153">-WhatIf</span></span>
<span data-ttu-id="0f545-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f545-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f545-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f545-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f545-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f545-156">CommonParameters</span></span>
<span data-ttu-id="0f545-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f545-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f545-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0f545-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f545-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f545-159">INPUTS</span></span>

### <span data-ttu-id="0f545-160">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="0f545-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="0f545-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f545-161">OUTPUTS</span></span>

### <span data-ttu-id="0f545-162">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20200701. ıappresource</span><span class="sxs-lookup"><span data-stu-id="0f545-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="0f545-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f545-163">NOTES</span></span>

<span data-ttu-id="0f545-164">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0f545-164">ALIASES</span></span>

<span data-ttu-id="0f545-165">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="0f545-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f545-166">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f545-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f545-167">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f545-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f545-168">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0f545-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f545-169">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="0f545-170">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="0f545-171">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="0f545-172">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="0f545-173">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="0f545-174">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0f545-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f545-175">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="0f545-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="0f545-176">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0f545-177">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f545-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0f545-178">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0f545-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="0f545-179">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="0f545-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="0f545-180">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0f545-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0f545-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f545-181">RELATED LINKS</span></span>

