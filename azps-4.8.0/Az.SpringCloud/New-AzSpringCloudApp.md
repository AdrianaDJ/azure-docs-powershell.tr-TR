---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: 966a0c0243d8ca8cd982420a9a3018f9d41ab52e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273932"
---
# <span data-ttu-id="d85bc-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d85bc-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="d85bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d85bc-103">Yeni bir uygulama oluşturun veya çıkışta uygulamayı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="d85bc-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="d85bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d85bc-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d85bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d85bc-105">DESCRIPTION</span></span>
<span data-ttu-id="d85bc-106">Yeni bir uygulama oluşturun veya çıkışta uygulamayı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="d85bc-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="d85bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d85bc-107">EXAMPLES</span></span>

### <span data-ttu-id="d85bc-108">Örnek 1: yay bulut uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d85bc-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
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

<span data-ttu-id="d85bc-109">Yay bulut uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d85bc-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="d85bc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d85bc-110">PARAMETERS</span></span>

### <span data-ttu-id="d85bc-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="d85bc-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="d85bc-112">Uygulamanın etkin dağıtımının adı</span><span class="sxs-lookup"><span data-stu-id="d85bc-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="d85bc-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d85bc-113">-AsJob</span></span>
<span data-ttu-id="d85bc-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="d85bc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d85bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85bc-115">-DefaultProfile</span></span>
<span data-ttu-id="d85bc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d85bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85bc-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="d85bc-117">-Fqdn</span></span>
<span data-ttu-id="d85bc-118">Tam nitelikli DNS adı.</span><span class="sxs-lookup"><span data-stu-id="d85bc-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="d85bc-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d85bc-119">-HttpsOnly</span></span>
<span data-ttu-id="d85bc-120">Yalnızca https olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d85bc-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="d85bc-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="d85bc-121">-Location</span></span>
<span data-ttu-id="d85bc-122">Uygulamanın COĞRAFI konumu, her zaman üst kaynağıyla aynı olan</span><span class="sxs-lookup"><span data-stu-id="d85bc-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="d85bc-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d85bc-123">-Name</span></span>
<span data-ttu-id="d85bc-124">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d85bc-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85bc-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d85bc-125">-NoWait</span></span>
<span data-ttu-id="d85bc-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="d85bc-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d85bc-127">-Persistentdiskbağlamayolu</span><span class="sxs-lookup"><span data-stu-id="d85bc-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="d85bc-128">Kalıcı diskin bağlama yolu</span><span class="sxs-lookup"><span data-stu-id="d85bc-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="d85bc-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="d85bc-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="d85bc-130">GB cinsinden kalıcı diskin boyutu</span><span class="sxs-lookup"><span data-stu-id="d85bc-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="d85bc-131">-Genel</span><span class="sxs-lookup"><span data-stu-id="d85bc-131">-Public</span></span>
<span data-ttu-id="d85bc-132">Uygulamanın genel uç noktayı gösterir</span><span class="sxs-lookup"><span data-stu-id="d85bc-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="d85bc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d85bc-133">-ResourceGroupName</span></span>
<span data-ttu-id="d85bc-134">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d85bc-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d85bc-135">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d85bc-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d85bc-136">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d85bc-136">-ServiceName</span></span>
<span data-ttu-id="d85bc-137">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d85bc-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d85bc-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d85bc-138">-SubscriptionId</span></span>
<span data-ttu-id="d85bc-139">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="d85bc-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d85bc-140">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d85bc-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d85bc-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="d85bc-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="d85bc-142">Geçici diskin bağlama yolu</span><span class="sxs-lookup"><span data-stu-id="d85bc-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="d85bc-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="d85bc-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="d85bc-144">GB cinsinden geçici diskin boyutu</span><span class="sxs-lookup"><span data-stu-id="d85bc-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="d85bc-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="d85bc-145">-Confirm</span></span>
<span data-ttu-id="d85bc-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d85bc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d85bc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d85bc-147">-WhatIf</span></span>
<span data-ttu-id="d85bc-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d85bc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d85bc-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d85bc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d85bc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85bc-150">CommonParameters</span></span>
<span data-ttu-id="d85bc-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d85bc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85bc-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d85bc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85bc-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d85bc-153">INPUTS</span></span>

## <span data-ttu-id="d85bc-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d85bc-154">OUTPUTS</span></span>

### <span data-ttu-id="d85bc-155">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20190501Preview. ıappresource</span><span class="sxs-lookup"><span data-stu-id="d85bc-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="d85bc-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d85bc-156">NOTES</span></span>

<span data-ttu-id="d85bc-157">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d85bc-157">ALIASES</span></span>

## <span data-ttu-id="d85bc-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d85bc-158">RELATED LINKS</span></span>

