---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275241"
---
# <span data-ttu-id="02c66-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="02c66-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="02c66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c66-102">SYNOPSIS</span></span>
<span data-ttu-id="02c66-103">Bir hizmet ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="02c66-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="02c66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02c66-104">SYNTAX</span></span>

### <span data-ttu-id="02c66-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02c66-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02c66-106">Al</span><span class="sxs-lookup"><span data-stu-id="02c66-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02c66-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="02c66-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02c66-108">List1</span><span class="sxs-lookup"><span data-stu-id="02c66-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="02c66-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="02c66-109">DESCRIPTION</span></span>
<span data-ttu-id="02c66-110">Bir hizmet ve özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="02c66-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="02c66-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02c66-111">EXAMPLES</span></span>

### <span data-ttu-id="02c66-112">Örnek 1: yay bulut hizmetini adıyla edinin</span><span class="sxs-lookup"><span data-stu-id="02c66-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="02c66-113">Yay bulut hizmetini adıyla edinin</span><span class="sxs-lookup"><span data-stu-id="02c66-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="02c66-114">Örnek 2: kaynak grubunun altındaki tüm yay bulut hizmetini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="02c66-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="02c66-115">Kaynak grubunun altındaki tüm yay bulut hizmetini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="02c66-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="02c66-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02c66-116">PARAMETERS</span></span>

### <span data-ttu-id="02c66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c66-117">-DefaultProfile</span></span>
<span data-ttu-id="02c66-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02c66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c66-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c66-119">-InputObject</span></span>
<span data-ttu-id="02c66-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="02c66-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="02c66-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="02c66-121">-Name</span></span>
<span data-ttu-id="02c66-122">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c66-123">-ResourceGroupName</span></span>
<span data-ttu-id="02c66-124">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="02c66-125">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02c66-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c66-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="02c66-126">-SubscriptionId</span></span>
<span data-ttu-id="02c66-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="02c66-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="02c66-128">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="02c66-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="02c66-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c66-129">CommonParameters</span></span>
<span data-ttu-id="02c66-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02c66-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c66-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02c66-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c66-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02c66-132">INPUTS</span></span>

### <span data-ttu-id="02c66-133">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="02c66-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="02c66-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02c66-134">OUTPUTS</span></span>

### <span data-ttu-id="02c66-135">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="02c66-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="02c66-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02c66-136">NOTES</span></span>

<span data-ttu-id="02c66-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="02c66-137">ALIASES</span></span>

<span data-ttu-id="02c66-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="02c66-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02c66-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="02c66-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02c66-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02c66-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02c66-141">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="02c66-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02c66-142">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="02c66-143">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="02c66-144">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="02c66-145">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="02c66-146">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="02c66-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="02c66-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02c66-148">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="02c66-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="02c66-149">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="02c66-150">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02c66-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="02c66-151">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="02c66-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="02c66-152">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="02c66-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="02c66-153">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="02c66-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="02c66-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02c66-154">RELATED LINKS</span></span>

