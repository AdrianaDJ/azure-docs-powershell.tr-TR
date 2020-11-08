---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 75ee07a9ce74f5b2667d8197ca141883508faa1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098380"
---
# <span data-ttu-id="ab253-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-101">Set-AzWebApp</span></span>

## <span data-ttu-id="ab253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab253-102">SYNOPSIS</span></span>
<span data-ttu-id="ab253-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ab253-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="ab253-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab253-104">SYNTAX</span></span>

### <span data-ttu-id="ab253-105">S1</span><span class="sxs-lookup"><span data-stu-id="ab253-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab253-106">S2</span><span class="sxs-lookup"><span data-stu-id="ab253-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab253-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab253-107">DESCRIPTION</span></span>
<span data-ttu-id="ab253-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ab253-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="ab253-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab253-109">EXAMPLES</span></span>

### <span data-ttu-id="ab253-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ab253-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="ab253-111">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp ile ilişkili appservice planını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ab253-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="ab253-112">Bağlantıyı kullanarak appservice planının ve onunla ilişkilendirilmiş kısıtlamaların değiştirilmesiyle ilgili daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="ab253-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="ab253-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="ab253-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="ab253-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ab253-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="ab253-115">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="ab253-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ab253-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab253-116">PARAMETERS</span></span>

### <span data-ttu-id="ab253-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="ab253-117">-AlwaysOn</span></span>
<span data-ttu-id="ab253-118">Web uygulamasının, boşta kaldıktan sonra, her zaman yüklü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ab253-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab253-119">-AppServicePlan</span></span>
<span data-ttu-id="ab253-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="ab253-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ab253-121">-AppSettings</span></span>
<span data-ttu-id="ab253-122">Uygulama ayarları HashTable.</span><span class="sxs-lookup"><span data-stu-id="ab253-122">App Settings HashTable.</span></span> <span data-ttu-id="ab253-123">Mevcut uygulama ayarları değiştirilecek ve sağlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="ab253-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="ab253-124">-AsJob</span></span>
<span data-ttu-id="ab253-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ab253-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab253-126">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="ab253-126">-AssignIdentity</span></span>
<span data-ttu-id="ab253-127">Mevcut Azure WebApp veya functionapp 'te MSI 'yi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="ab253-127">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ab253-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="ab253-129">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="ab253-129">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ab253-130">-AzureStoragePath</span></span>
<span data-ttu-id="ab253-131">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="ab253-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="ab253-132">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="ab253-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ab253-133">-ConnectionStrings</span></span>
<span data-ttu-id="ab253-134">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="ab253-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-135">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="ab253-135">-ContainerImageName</span></span>
<span data-ttu-id="ab253-136">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="ab253-136">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ab253-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ab253-138">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="ab253-138">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ab253-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ab253-140">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="ab253-140">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ab253-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="ab253-142">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="ab253-142">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ab253-143">-DefaultDocuments</span></span>
<span data-ttu-id="ab253-144">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="ab253-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab253-145">-DefaultProfile</span></span>
<span data-ttu-id="ab253-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab253-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ab253-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ab253-148">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="ab253-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ab253-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ab253-150">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="ab253-150">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="ab253-151">-FtpsState</span></span>
<span data-ttu-id="ab253-152">Bir uygulamanın FTPS durum değerini ayarlama.</span><span class="sxs-lookup"><span data-stu-id="ab253-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="ab253-153">İzin verilen değerler [AllAllowed | Devre dışı | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="ab253-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ab253-154">-HandlerMappings</span></span>
<span data-ttu-id="ab253-155">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="ab253-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-156">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="ab253-156">-HostNames</span></span>
<span data-ttu-id="ab253-157">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="ab253-157">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-158">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ab253-158">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ab253-159">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="ab253-159">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-160">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ab253-160">-HttpsOnly</span></span>
<span data-ttu-id="ab253-161">Var olan Azure WebApp veya functionapp 'te tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="ab253-161">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-162">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ab253-162">-ManagedPipelineMode</span></span>
<span data-ttu-id="ab253-163">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="ab253-163">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-164">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ab253-164">-MinTlsVersion</span></span>
<span data-ttu-id="ab253-165">SSL istekleri için gereken en düşük TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab253-165">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="ab253-166">İzin verilen değerler [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="ab253-166">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-167">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab253-167">-Name</span></span>
<span data-ttu-id="ab253-168">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ab253-168">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-169">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ab253-169">-NetFrameworkVersion</span></span>
<span data-ttu-id="ab253-170">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="ab253-170">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-171">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="ab253-171">-NumberOfWorkers</span></span>
<span data-ttu-id="ab253-172">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="ab253-172">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-173">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ab253-173">-PhpVersion</span></span>
<span data-ttu-id="ab253-174">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="ab253-174">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-175">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ab253-175">-RequestTracingEnabled</span></span>
<span data-ttu-id="ab253-176">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="ab253-176">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab253-177">-ResourceGroupName</span></span>
<span data-ttu-id="ab253-178">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ab253-178">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ab253-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ab253-180">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="ab253-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-181">-WebApp</span></span>
<span data-ttu-id="ab253-182">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="ab253-182">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ab253-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="ab253-184">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="ab253-184">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab253-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab253-185">CommonParameters</span></span>
<span data-ttu-id="ab253-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab253-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab253-187">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ab253-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab253-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab253-188">INPUTS</span></span>

### <span data-ttu-id="ab253-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ab253-189">System.Int32</span></span>

### <span data-ttu-id="ab253-190">System. String</span><span class="sxs-lookup"><span data-stu-id="ab253-190">System.String</span></span>

### <span data-ttu-id="ab253-191">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="ab253-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ab253-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab253-192">OUTPUTS</span></span>

### <span data-ttu-id="ab253-193">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="ab253-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ab253-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab253-194">NOTES</span></span>

## <span data-ttu-id="ab253-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab253-195">RELATED LINKS</span></span>

[<span data-ttu-id="ab253-196">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-196">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ab253-197">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-197">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ab253-198">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-198">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ab253-199">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-199">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ab253-200">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-200">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ab253-201">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab253-201">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
