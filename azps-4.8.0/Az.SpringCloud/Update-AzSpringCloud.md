---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 02a880d669e3e93693dc39823587fe1d676ac279
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108720"
---
# <span data-ttu-id="df8f3-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="df8f3-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="df8f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="df8f3-103">Bir hizmeti güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="df8f3-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="df8f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df8f3-104">SYNTAX</span></span>

### <span data-ttu-id="df8f3-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df8f3-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df8f3-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="df8f3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df8f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="df8f3-107">DESCRIPTION</span></span>
<span data-ttu-id="df8f3-108">Bir hizmeti güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="df8f3-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="df8f3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df8f3-109">EXAMPLES</span></span>

### <span data-ttu-id="df8f3-110">Örnek 1: yay bulut hizmetini adıyla güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="df8f3-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="df8f3-111">Spring bulut hizmetini adıyla güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="df8f3-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="df8f3-112">Örnek 2: yay bulut hizmetini kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="df8f3-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="df8f3-113">Yay bulut hizmetini kanaldan güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="df8f3-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="df8f3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df8f3-114">PARAMETERS</span></span>

### <span data-ttu-id="df8f3-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="df8f3-115">-AsJob</span></span>
<span data-ttu-id="df8f3-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="df8f3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="df8f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8f3-117">-DefaultProfile</span></span>
<span data-ttu-id="df8f3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df8f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df8f3-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="df8f3-119">-GitPropertyUri</span></span>
<span data-ttu-id="df8f3-120">Deponun URI 'SI</span><span class="sxs-lookup"><span data-stu-id="df8f3-120">URI of the repository</span></span>

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

### <span data-ttu-id="df8f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df8f3-121">-InputObject</span></span>
<span data-ttu-id="df8f3-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df8f3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df8f3-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="df8f3-123">-Location</span></span>
<span data-ttu-id="df8f3-124">Kaynağın COĞRAFI konumu.</span><span class="sxs-lookup"><span data-stu-id="df8f3-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="df8f3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="df8f3-125">-Name</span></span>
<span data-ttu-id="df8f3-126">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8f3-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="df8f3-127">-NoWait</span></span>
<span data-ttu-id="df8f3-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="df8f3-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df8f3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df8f3-129">-ResourceGroupName</span></span>
<span data-ttu-id="df8f3-130">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="df8f3-131">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="df8f3-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="df8f3-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="df8f3-132">-SkuName</span></span>
<span data-ttu-id="df8f3-133">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="df8f3-133">Name of the Sku</span></span>

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

### <span data-ttu-id="df8f3-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="df8f3-134">-SkuTier</span></span>
<span data-ttu-id="df8f3-135">SKU 'nun katmanı</span><span class="sxs-lookup"><span data-stu-id="df8f3-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="df8f3-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="df8f3-136">-SubscriptionId</span></span>
<span data-ttu-id="df8f3-137">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="df8f3-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="df8f3-138">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="df8f3-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="df8f3-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="df8f3-139">-Tag</span></span>
<span data-ttu-id="df8f3-140">Hizmetin, kaynağı tanımlayan anahtar değer çiftleri listesi olan etiketleri.</span><span class="sxs-lookup"><span data-stu-id="df8f3-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="df8f3-141">-Traceappınsider.</span><span class="sxs-lookup"><span data-stu-id="df8f3-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="df8f3-142">Hedef uygulama Insight alet anahtarı</span><span class="sxs-lookup"><span data-stu-id="df8f3-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="df8f3-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="df8f3-143">-TraceEnabled</span></span>
<span data-ttu-id="df8f3-144">İzleme işlevinin etkinleştirilip etkinleştirilmeyeceğini gösterir</span><span class="sxs-lookup"><span data-stu-id="df8f3-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="df8f3-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="df8f3-145">-Confirm</span></span>
<span data-ttu-id="df8f3-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df8f3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df8f3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df8f3-147">-WhatIf</span></span>
<span data-ttu-id="df8f3-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df8f3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df8f3-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df8f3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df8f3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8f3-150">CommonParameters</span></span>
<span data-ttu-id="df8f3-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df8f3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8f3-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="df8f3-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8f3-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df8f3-153">INPUTS</span></span>

### <span data-ttu-id="df8f3-154">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="df8f3-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="df8f3-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df8f3-155">OUTPUTS</span></span>

### <span data-ttu-id="df8f3-156">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="df8f3-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="df8f3-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df8f3-157">NOTES</span></span>

<span data-ttu-id="df8f3-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="df8f3-158">ALIASES</span></span>

<span data-ttu-id="df8f3-159">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="df8f3-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df8f3-160">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="df8f3-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df8f3-161">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df8f3-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df8f3-162">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="df8f3-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df8f3-163">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="df8f3-164">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="df8f3-165">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="df8f3-166">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="df8f3-167">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="df8f3-168">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="df8f3-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df8f3-169">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="df8f3-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="df8f3-170">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="df8f3-171">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="df8f3-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="df8f3-172">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="df8f3-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="df8f3-173">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="df8f3-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="df8f3-174">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="df8f3-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="df8f3-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df8f3-175">RELATED LINKS</span></span>

