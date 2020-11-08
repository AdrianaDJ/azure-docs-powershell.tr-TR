---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109295"
---
# <span data-ttu-id="44ae0-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-101">Set-AzWebApp</span></span>

## <span data-ttu-id="44ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="44ae0-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="44ae0-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="44ae0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44ae0-104">SYNTAX</span></span>

### <span data-ttu-id="44ae0-105">S1</span><span class="sxs-lookup"><span data-stu-id="44ae0-105">S1</span></span>
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

### <span data-ttu-id="44ae0-106">S2</span><span class="sxs-lookup"><span data-stu-id="44ae0-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ae0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="44ae0-107">DESCRIPTION</span></span>
<span data-ttu-id="44ae0-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="44ae0-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="44ae0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44ae0-109">EXAMPLES</span></span>

### <span data-ttu-id="44ae0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44ae0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="44ae0-111">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp ile ilişkili appservice planını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="44ae0-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="44ae0-112">Bağlantıyı kullanarak appservice planının ve onunla ilişkilendirilmiş kısıtlamaların değiştirilmesiyle ilgili daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="44ae0-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="44ae0-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="44ae0-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="44ae0-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="44ae0-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="44ae0-115">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="44ae0-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="44ae0-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="44ae0-116">Example 3</span></span>

<span data-ttu-id="44ae0-117">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="44ae0-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="44ae0-118">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="44ae0-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="44ae0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44ae0-119">PARAMETERS</span></span>

### <span data-ttu-id="44ae0-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="44ae0-120">-AlwaysOn</span></span>
<span data-ttu-id="44ae0-121">Web uygulamasının, boşta kaldıktan sonra, her zaman yüklü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="44ae0-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="44ae0-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="44ae0-122">-AppServicePlan</span></span>
<span data-ttu-id="44ae0-123">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="44ae0-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="44ae0-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="44ae0-124">-AppSettings</span></span>
<span data-ttu-id="44ae0-125">Uygulama ayarları HashTable.</span><span class="sxs-lookup"><span data-stu-id="44ae0-125">App Settings HashTable.</span></span> <span data-ttu-id="44ae0-126">Mevcut uygulama ayarları değiştirilecek ve sağlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="44ae0-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="44ae0-127">-Iş</span><span class="sxs-lookup"><span data-stu-id="44ae0-127">-AsJob</span></span>
<span data-ttu-id="44ae0-128">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="44ae0-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44ae0-129">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="44ae0-129">-AssignIdentity</span></span>
<span data-ttu-id="44ae0-130">Mevcut Azure WebApp veya functionapp 'te MSI 'yi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="44ae0-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="44ae0-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="44ae0-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="44ae0-132">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="44ae0-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="44ae0-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="44ae0-133">-AzureStoragePath</span></span>
<span data-ttu-id="44ae0-134">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="44ae0-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="44ae0-135">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="44ae0-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="44ae0-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="44ae0-136">-ConnectionStrings</span></span>
<span data-ttu-id="44ae0-137">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="44ae0-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="44ae0-138">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="44ae0-138">-ContainerImageName</span></span>
<span data-ttu-id="44ae0-139">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="44ae0-139">Container Image Name</span></span>

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

### <span data-ttu-id="44ae0-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="44ae0-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="44ae0-141">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="44ae0-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="44ae0-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="44ae0-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="44ae0-143">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="44ae0-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="44ae0-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="44ae0-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="44ae0-145">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="44ae0-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="44ae0-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="44ae0-146">-DefaultDocuments</span></span>
<span data-ttu-id="44ae0-147">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="44ae0-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="44ae0-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ae0-148">-DefaultProfile</span></span>
<span data-ttu-id="44ae0-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44ae0-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44ae0-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="44ae0-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="44ae0-151">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="44ae0-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="44ae0-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="44ae0-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="44ae0-153">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="44ae0-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="44ae0-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="44ae0-154">-FtpsState</span></span>
<span data-ttu-id="44ae0-155">Bir uygulamanın FTPS durum değerini ayarlama.</span><span class="sxs-lookup"><span data-stu-id="44ae0-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="44ae0-156">İzin verilen değerler [AllAllowed | Devre dışı | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="44ae0-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="44ae0-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="44ae0-157">-HandlerMappings</span></span>
<span data-ttu-id="44ae0-158">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="44ae0-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="44ae0-159">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="44ae0-159">-HostNames</span></span>
<span data-ttu-id="44ae0-160">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="44ae0-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="44ae0-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="44ae0-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="44ae0-162">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="44ae0-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="44ae0-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="44ae0-163">-HttpsOnly</span></span>
<span data-ttu-id="44ae0-164">Var olan Azure WebApp veya functionapp 'te tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="44ae0-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="44ae0-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="44ae0-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="44ae0-166">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="44ae0-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="44ae0-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="44ae0-167">-MinTlsVersion</span></span>
<span data-ttu-id="44ae0-168">SSL istekleri için gereken en düşük TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="44ae0-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="44ae0-169">İzin verilen değerler [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="44ae0-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="44ae0-170">-Ad</span><span class="sxs-lookup"><span data-stu-id="44ae0-170">-Name</span></span>
<span data-ttu-id="44ae0-171">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="44ae0-171">WebApp Name</span></span>

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

### <span data-ttu-id="44ae0-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="44ae0-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="44ae0-173">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="44ae0-173">Net Framework Version</span></span>

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

### <span data-ttu-id="44ae0-174">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="44ae0-174">-NumberOfWorkers</span></span>
<span data-ttu-id="44ae0-175">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="44ae0-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="44ae0-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="44ae0-176">-PhpVersion</span></span>
<span data-ttu-id="44ae0-177">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="44ae0-177">Php Version</span></span>

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

### <span data-ttu-id="44ae0-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="44ae0-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="44ae0-179">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="44ae0-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="44ae0-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ae0-180">-ResourceGroupName</span></span>
<span data-ttu-id="44ae0-181">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="44ae0-181">Resource Group Name</span></span>

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

### <span data-ttu-id="44ae0-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="44ae0-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="44ae0-183">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="44ae0-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="44ae0-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-184">-WebApp</span></span>
<span data-ttu-id="44ae0-185">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="44ae0-185">WebApp Object</span></span>

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

### <span data-ttu-id="44ae0-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="44ae0-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="44ae0-187">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="44ae0-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="44ae0-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ae0-188">CommonParameters</span></span>
<span data-ttu-id="44ae0-189">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44ae0-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ae0-190">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="44ae0-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ae0-191">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44ae0-191">INPUTS</span></span>

### <span data-ttu-id="44ae0-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="44ae0-192">System.Int32</span></span>

### <span data-ttu-id="44ae0-193">System. String</span><span class="sxs-lookup"><span data-stu-id="44ae0-193">System.String</span></span>

### <span data-ttu-id="44ae0-194">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="44ae0-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="44ae0-195">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44ae0-195">OUTPUTS</span></span>

### <span data-ttu-id="44ae0-196">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="44ae0-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="44ae0-197">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44ae0-197">NOTES</span></span>
<span data-ttu-id="44ae0-198">Sağlanan cmdlet 'in altında, Azure Web App 'i **Dotnetcore** 'a güncelleştirmenize yardımcı olur</span><span class="sxs-lookup"><span data-stu-id="44ae0-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="44ae0-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-Web-WestUS"-ResourceType Microsoft. Web/Sites/config-ResourceName "ContosoWebApp/Metadata"-Apıversion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="44ae0-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="44ae0-200">Default-Web-WestUS değerlerini WebApp ve ContosoWebApp kaynak grubu adınızla WebApp adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="44ae0-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="44ae0-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44ae0-201">RELATED LINKS</span></span>

[<span data-ttu-id="44ae0-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="44ae0-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="44ae0-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="44ae0-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="44ae0-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="44ae0-207">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44ae0-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="44ae0-208">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="44ae0-208">New-AzResource</span></span>](./New-AzResource.md)
