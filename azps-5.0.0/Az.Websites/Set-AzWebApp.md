---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279137"
---
# <span data-ttu-id="9e4a9-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-101">Set-AzWebApp</span></span>

## <span data-ttu-id="9e4a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4a9-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="9e4a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e4a9-104">SYNTAX</span></span>

### <span data-ttu-id="9e4a9-105">S1</span><span class="sxs-lookup"><span data-stu-id="9e4a9-105">S1</span></span>
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

### <span data-ttu-id="9e4a9-106">S2</span><span class="sxs-lookup"><span data-stu-id="9e4a9-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e4a9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e4a9-107">DESCRIPTION</span></span>
<span data-ttu-id="9e4a9-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="9e4a9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e4a9-109">EXAMPLES</span></span>

### <span data-ttu-id="9e4a9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e4a9-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="9e4a9-111">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp ile ilişkili appservice planını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="9e4a9-112">Bağlantıyı kullanarak appservice planının ve onunla ilişkilendirilmiş kısıtlamaların değiştirilmesiyle ilgili daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="9e4a9-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="9e4a9-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="9e4a9-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9e4a9-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="9e4a9-115">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="9e4a9-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="9e4a9-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9e4a9-116">Example 3</span></span>

<span data-ttu-id="9e4a9-117">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="9e4a9-118">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="9e4a9-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="9e4a9-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="9e4a9-119">Example 4</span></span>

<span data-ttu-id="9e4a9-120">Aşağıdaki örnek, Web App ContosoWebApp için myConnectionString adlı bir bağlantı dizesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="9e4a9-121">Bu, Web App ContosoWebApp için varolan tüm bağlantı dizelerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="9e4a9-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e4a9-122">PARAMETERS</span></span>

### <span data-ttu-id="9e4a9-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="9e4a9-123">-AlwaysOn</span></span>
<span data-ttu-id="9e4a9-124">Web uygulamasının, boşta kaldıktan sonra, her zaman yüklü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="9e4a9-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9e4a9-125">-AppServicePlan</span></span>
<span data-ttu-id="9e4a9-126">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="9e4a9-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9e4a9-127">-AppSettings</span></span>
<span data-ttu-id="9e4a9-128">Uygulama ayarları HashTable.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-128">App Settings HashTable.</span></span> <span data-ttu-id="9e4a9-129">Mevcut uygulama ayarları değiştirilecek ve sağlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="9e4a9-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="9e4a9-130">-AsJob</span></span>
<span data-ttu-id="9e4a9-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9e4a9-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e4a9-132">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="9e4a9-132">-AssignIdentity</span></span>
<span data-ttu-id="9e4a9-133">Mevcut Azure WebApp veya functionapp 'te MSI 'yi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9e4a9-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="9e4a9-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9e4a9-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="9e4a9-135">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="9e4a9-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="9e4a9-136">-AzureStoragePath</span></span>
<span data-ttu-id="9e4a9-137">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="9e4a9-138">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="9e4a9-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="9e4a9-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="9e4a9-139">-ConnectionStrings</span></span>
<span data-ttu-id="9e4a9-140">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="9e4a9-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="9e4a9-141">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-141">-ContainerImageName</span></span>
<span data-ttu-id="9e4a9-142">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-142">Container Image Name</span></span>

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

### <span data-ttu-id="9e4a9-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9e4a9-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9e4a9-144">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="9e4a9-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9e4a9-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9e4a9-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9e4a9-146">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="9e4a9-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9e4a9-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9e4a9-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="9e4a9-148">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9e4a9-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="9e4a9-149">-DefaultDocuments</span></span>
<span data-ttu-id="9e4a9-150">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="9e4a9-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="9e4a9-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4a9-151">-DefaultProfile</span></span>
<span data-ttu-id="9e4a9-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e4a9-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9e4a9-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9e4a9-154">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="9e4a9-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="9e4a9-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9e4a9-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9e4a9-156">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="9e4a9-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9e4a9-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="9e4a9-157">-FtpsState</span></span>
<span data-ttu-id="9e4a9-158">Bir uygulamanın FTPS durum değerini ayarlama.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="9e4a9-159">İzin verilen değerler [AllAllowed | Devre dışı | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="9e4a9-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="9e4a9-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9e4a9-160">-HandlerMappings</span></span>
<span data-ttu-id="9e4a9-161">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="9e4a9-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="9e4a9-162">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="9e4a9-162">-HostNames</span></span>
<span data-ttu-id="9e4a9-163">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="9e4a9-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="9e4a9-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9e4a9-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9e4a9-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="9e4a9-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="9e4a9-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9e4a9-166">-HttpsOnly</span></span>
<span data-ttu-id="9e4a9-167">Var olan Azure WebApp veya functionapp 'te tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9e4a9-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="9e4a9-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9e4a9-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="9e4a9-169">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="9e4a9-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9e4a9-170">-MinTlsVersion</span></span>
<span data-ttu-id="9e4a9-171">SSL istekleri için gereken en düşük TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="9e4a9-172">İzin verilen değerler [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="9e4a9-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="9e4a9-173">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e4a9-173">-Name</span></span>
<span data-ttu-id="9e4a9-174">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-174">WebApp Name</span></span>

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

### <span data-ttu-id="9e4a9-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9e4a9-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="9e4a9-176">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="9e4a9-176">Net Framework Version</span></span>

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

### <span data-ttu-id="9e4a9-177">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="9e4a9-177">-NumberOfWorkers</span></span>
<span data-ttu-id="9e4a9-178">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="9e4a9-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9e4a9-179">-PhpVersion</span></span>
<span data-ttu-id="9e4a9-180">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="9e4a9-180">Php Version</span></span>

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

### <span data-ttu-id="9e4a9-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9e4a9-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="9e4a9-182">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="9e4a9-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="9e4a9-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4a9-183">-ResourceGroupName</span></span>
<span data-ttu-id="9e4a9-184">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-184">Resource Group Name</span></span>

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

### <span data-ttu-id="9e4a9-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9e4a9-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9e4a9-186">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="9e4a9-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="9e4a9-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-187">-WebApp</span></span>
<span data-ttu-id="9e4a9-188">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="9e4a9-188">WebApp Object</span></span>

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

### <span data-ttu-id="9e4a9-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e4a9-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="9e4a9-190">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="9e4a9-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="9e4a9-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4a9-191">CommonParameters</span></span>
<span data-ttu-id="9e4a9-192">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4a9-193">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4a9-194">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e4a9-194">INPUTS</span></span>

### <span data-ttu-id="9e4a9-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9e4a9-195">System.Int32</span></span>

### <span data-ttu-id="9e4a9-196">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4a9-196">System.String</span></span>

### <span data-ttu-id="9e4a9-197">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="9e4a9-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9e4a9-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e4a9-198">OUTPUTS</span></span>

### <span data-ttu-id="9e4a9-199">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="9e4a9-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9e4a9-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e4a9-200">NOTES</span></span>
<span data-ttu-id="9e4a9-201">Sağlanan cmdlet 'in altında, Azure Web App 'i **Dotnetcore** 'a güncelleştirmenize yardımcı olur</span><span class="sxs-lookup"><span data-stu-id="9e4a9-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="9e4a9-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-Web-WestUS"-ResourceType Microsoft. Web/Sites/config-ResourceName "ContosoWebApp/Metadata"-Apıversion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="9e4a9-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="9e4a9-203">Default-Web-WestUS değerlerini WebApp ve ContosoWebApp kaynak grubu adınızla WebApp adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9e4a9-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="9e4a9-204">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e4a9-204">RELATED LINKS</span></span>

[<span data-ttu-id="9e4a9-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="9e4a9-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="9e4a9-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="9e4a9-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="9e4a9-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="9e4a9-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9e4a9-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="9e4a9-211">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="9e4a9-211">New-AzResource</span></span>](./New-AzResource.md)
