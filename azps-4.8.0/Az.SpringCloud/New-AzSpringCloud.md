---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: c84037fd402e5ecea51cc4f60dcddb1873878f5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273941"
---
# <span data-ttu-id="14f8a-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="14f8a-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="14f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="14f8a-103">Yeni hizmet oluşturun veya çıkışta hizmeti güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="14f8a-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="14f8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14f8a-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14f8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="14f8a-106">Yeni hizmet oluşturun veya çıkışta hizmeti güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="14f8a-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="14f8a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14f8a-107">EXAMPLES</span></span>

### <span data-ttu-id="14f8a-108">Örnek 1: yay bulut hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="14f8a-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="14f8a-109">Yay bulut hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="14f8a-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="14f8a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14f8a-110">PARAMETERS</span></span>

### <span data-ttu-id="14f8a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="14f8a-111">-AsJob</span></span>
<span data-ttu-id="14f8a-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="14f8a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="14f8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f8a-113">-DefaultProfile</span></span>
<span data-ttu-id="14f8a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14f8a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f8a-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="14f8a-115">-GitPropertyUri</span></span>
<span data-ttu-id="14f8a-116">Deponun URI 'SI</span><span class="sxs-lookup"><span data-stu-id="14f8a-116">URI of the repository</span></span>

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

### <span data-ttu-id="14f8a-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="14f8a-117">-Location</span></span>
<span data-ttu-id="14f8a-118">Kaynağın COĞRAFI konumu.</span><span class="sxs-lookup"><span data-stu-id="14f8a-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="14f8a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="14f8a-119">-Name</span></span>
<span data-ttu-id="14f8a-120">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="14f8a-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f8a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="14f8a-121">-NoWait</span></span>
<span data-ttu-id="14f8a-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="14f8a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14f8a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f8a-123">-ResourceGroupName</span></span>
<span data-ttu-id="14f8a-124">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="14f8a-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="14f8a-125">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14f8a-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="14f8a-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="14f8a-126">-SkuName</span></span>
<span data-ttu-id="14f8a-127">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="14f8a-127">Name of the Sku</span></span>

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

### <span data-ttu-id="14f8a-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="14f8a-128">-SkuTier</span></span>
<span data-ttu-id="14f8a-129">SKU 'nun katmanı</span><span class="sxs-lookup"><span data-stu-id="14f8a-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="14f8a-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="14f8a-130">-SubscriptionId</span></span>
<span data-ttu-id="14f8a-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="14f8a-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="14f8a-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="14f8a-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="14f8a-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="14f8a-133">-Tag</span></span>
<span data-ttu-id="14f8a-134">Hizmetin, kaynağı tanımlayan anahtar değer çiftleri listesi olan etiketleri.</span><span class="sxs-lookup"><span data-stu-id="14f8a-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="14f8a-135">-Traceappınsider.</span><span class="sxs-lookup"><span data-stu-id="14f8a-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="14f8a-136">Hedef uygulama Insight alet anahtarı</span><span class="sxs-lookup"><span data-stu-id="14f8a-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="14f8a-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="14f8a-137">-TraceEnabled</span></span>
<span data-ttu-id="14f8a-138">İzleme işlevinin etkinleştirilip etkinleştirilmeyeceğini gösterir</span><span class="sxs-lookup"><span data-stu-id="14f8a-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="14f8a-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="14f8a-139">-Confirm</span></span>
<span data-ttu-id="14f8a-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14f8a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f8a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f8a-141">-WhatIf</span></span>
<span data-ttu-id="14f8a-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14f8a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14f8a-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14f8a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f8a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f8a-144">CommonParameters</span></span>
<span data-ttu-id="14f8a-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14f8a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f8a-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="14f8a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f8a-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14f8a-147">INPUTS</span></span>

## <span data-ttu-id="14f8a-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14f8a-148">OUTPUTS</span></span>

### <span data-ttu-id="14f8a-149">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="14f8a-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="14f8a-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14f8a-150">NOTES</span></span>

<span data-ttu-id="14f8a-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="14f8a-151">ALIASES</span></span>

## <span data-ttu-id="14f8a-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14f8a-152">RELATED LINKS</span></span>

