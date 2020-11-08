---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275422"
---
# <span data-ttu-id="d1873-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d1873-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="d1873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1873-102">SYNOPSIS</span></span>
<span data-ttu-id="d1873-103">İşlev uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1873-103">Creates a function app.</span></span>

## <span data-ttu-id="d1873-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1873-104">SYNTAX</span></span>

### <span data-ttu-id="d1873-105">Tüketim (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1873-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1873-106">Byapılacak Pserviceplan</span><span class="sxs-lookup"><span data-stu-id="d1873-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1873-107">Customdockerımage</span><span class="sxs-lookup"><span data-stu-id="d1873-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1873-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1873-108">DESCRIPTION</span></span>
<span data-ttu-id="d1873-109">İşlev uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1873-109">Creates a function app.</span></span>

## <span data-ttu-id="d1873-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1873-110">EXAMPLES</span></span>

### <span data-ttu-id="d1873-111">Örnek 1: Merkezi ABD 'de bir tüketim PowerShell işlev uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d1873-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="d1873-112">Bu komut, Merkezi ABD 'de bir tüketim PowerShell işlev uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1873-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="d1873-113">Örnek 2: hizmet planında barındırılan bir PowerShell işlev uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d1873-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="d1873-114">Bu komut, hizmet planında barındırılan bir PowerShell işlevi uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1873-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="d1873-115">Örnek 3: özel bir ACR görüntüsü kullanarak işlev uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d1873-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="d1873-116">Bu komut özel bir ACR görüntüsü kullanarak işlev uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1873-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="d1873-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1873-117">PARAMETERS</span></span>

### <span data-ttu-id="d1873-118">-Applicationınsightskey</span><span class="sxs-lookup"><span data-stu-id="d1873-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="d1873-119">Application Insights 'ın alt yapısı</span><span class="sxs-lookup"><span data-stu-id="d1873-119">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-120">-Applicationınsightsname</span><span class="sxs-lookup"><span data-stu-id="d1873-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="d1873-121">İşlev uygulamasına eklenecek mevcut App Insights projesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d1873-121">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="d1873-122">-AppSetting</span></span>
<span data-ttu-id="d1873-123">İşlev uygulaması ayarları.</span><span class="sxs-lookup"><span data-stu-id="d1873-123">Function app settings.</span></span>

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

### <span data-ttu-id="d1873-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="d1873-124">-AsJob</span></span>
<span data-ttu-id="d1873-125">Cmdlet 'i arka plan işi olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d1873-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="d1873-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1873-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="d1873-127">-Disableapplicationınsights</span><span class="sxs-lookup"><span data-stu-id="d1873-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="d1873-128">Uygulama oluşturma işlevi sırasında Application Insights kaynağı oluşturmayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="d1873-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="d1873-129">Hiçbir günlük kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="d1873-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-130">-Dockerımagename</span><span class="sxs-lookup"><span data-stu-id="d1873-130">-DockerImageName</span></span>
<span data-ttu-id="d1873-131">Yalnızca Linux.</span><span class="sxs-lookup"><span data-stu-id="d1873-131">Linux only.</span></span>
<span data-ttu-id="d1873-132">Docker kayıt defterinden kapsayıcı görüntü adı; örneğin, Publisher/image-Name: Tag.</span><span class="sxs-lookup"><span data-stu-id="d1873-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="d1873-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="d1873-134">Kapsayıcı kayıt defteri Kullanıcı adı ve parolası.</span><span class="sxs-lookup"><span data-stu-id="d1873-134">The container registry user name and password.</span></span>
<span data-ttu-id="d1873-135">Özel kayıt defterleri için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d1873-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="d1873-136">-FunctionsVersion</span></span>
<span data-ttu-id="d1873-137">Işlevler sürümü.</span><span class="sxs-lookup"><span data-stu-id="d1873-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="d1873-138">-IdentityID</span></span>
<span data-ttu-id="d1873-139">İşlev uygulamasıyla ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1873-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="d1873-140">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="d1873-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d1873-141">-IdentityType</span></span>
<span data-ttu-id="d1873-142">İşlev uygulaması için kullanılan kimliğin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1873-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="d1873-143">Bu parametre için kabul edilebilir değerler şunlardır:-SystemAssigned-Useratandı</span><span class="sxs-lookup"><span data-stu-id="d1873-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-144">-Konum</span><span class="sxs-lookup"><span data-stu-id="d1873-144">-Location</span></span>
<span data-ttu-id="d1873-145">Tüketim planının konumu.</span><span class="sxs-lookup"><span data-stu-id="d1873-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1873-146">-Name</span></span>
<span data-ttu-id="d1873-147">İşlev uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="d1873-147">The name of the function app.</span></span>

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

### <span data-ttu-id="d1873-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d1873-148">-NoWait</span></span>
<span data-ttu-id="d1873-149">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="d1873-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="d1873-150">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="d1873-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d1873-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="d1873-151">-OSType</span></span>
<span data-ttu-id="d1873-152">İşlev uygulamasını barındıracak işletim sistemi.</span><span class="sxs-lookup"><span data-stu-id="d1873-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-153">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d1873-153">-PassThru</span></span>
<span data-ttu-id="d1873-154">Komut başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="d1873-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="d1873-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d1873-155">-PlanName</span></span>
<span data-ttu-id="d1873-156">Hizmet planının adı.</span><span class="sxs-lookup"><span data-stu-id="d1873-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1873-157">-ResourceGroupName</span></span>
<span data-ttu-id="d1873-158">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d1873-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1873-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="d1873-159">-Runtime</span></span>
<span data-ttu-id="d1873-160">İşlev çalışma zamanı.</span><span class="sxs-lookup"><span data-stu-id="d1873-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="d1873-161">-RuntimeVersion</span></span>
<span data-ttu-id="d1873-162">İşlev çalışma zamanı.</span><span class="sxs-lookup"><span data-stu-id="d1873-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1873-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d1873-163">-StorageAccountName</span></span>
<span data-ttu-id="d1873-164">Depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="d1873-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="d1873-165">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d1873-165">-SubscriptionId</span></span>
<span data-ttu-id="d1873-166">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d1873-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d1873-167">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d1873-167">-Tag</span></span>
<span data-ttu-id="d1873-168">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="d1873-168">Resource tags.</span></span>

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

### <span data-ttu-id="d1873-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1873-169">-Confirm</span></span>
<span data-ttu-id="d1873-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1873-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1873-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1873-171">-WhatIf</span></span>
<span data-ttu-id="d1873-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1873-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1873-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1873-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1873-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1873-174">CommonParameters</span></span>
<span data-ttu-id="d1873-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1873-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1873-176">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d1873-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1873-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1873-177">INPUTS</span></span>

## <span data-ttu-id="d1873-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1873-178">OUTPUTS</span></span>

### <span data-ttu-id="d1873-179">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="d1873-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="d1873-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1873-180">NOTES</span></span>

<span data-ttu-id="d1873-181">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d1873-181">ALIASES</span></span>

## <span data-ttu-id="d1873-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1873-182">RELATED LINKS</span></span>

