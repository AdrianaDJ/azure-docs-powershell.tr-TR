---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934178"
---
# <span data-ttu-id="34a5e-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-101">Set-AzWebApp</span></span>

## <span data-ttu-id="34a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="34a5e-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="34a5e-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="34a5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34a5e-104">SYNTAX</span></span>

### <span data-ttu-id="34a5e-105">S1</span><span class="sxs-lookup"><span data-stu-id="34a5e-105">S1</span></span>
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
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34a5e-106">S2</span><span class="sxs-lookup"><span data-stu-id="34a5e-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34a5e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34a5e-107">DESCRIPTION</span></span>
<span data-ttu-id="34a5e-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34a5e-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="34a5e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34a5e-109">EXAMPLES</span></span>

### <span data-ttu-id="34a5e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34a5e-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="34a5e-111">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp ile ilişkili appservice planını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="34a5e-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="34a5e-112">Bağlantıyı kullanarak appservice planının ve onunla ilişkilendirilmiş kısıtlamaların değiştirilmesiyle ilgili daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="34a5e-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="34a5e-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="34a5e-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="34a5e-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="34a5e-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="34a5e-115">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="34a5e-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="34a5e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34a5e-116">PARAMETERS</span></span>

### <span data-ttu-id="34a5e-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="34a5e-117">-AppServicePlan</span></span>
<span data-ttu-id="34a5e-118">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="34a5e-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="34a5e-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="34a5e-119">-AppSettings</span></span>
<span data-ttu-id="34a5e-120">Uygulama ayarları HashTable.</span><span class="sxs-lookup"><span data-stu-id="34a5e-120">App Settings HashTable.</span></span> <span data-ttu-id="34a5e-121">Mevcut uygulama ayarları değiştirilecek ve sağlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="34a5e-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="34a5e-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="34a5e-122">-AsJob</span></span>
<span data-ttu-id="34a5e-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="34a5e-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34a5e-124">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="34a5e-124">-AssignIdentity</span></span>
<span data-ttu-id="34a5e-125">Mevcut Azure WebApp veya functionapp 'te MSI 'yi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="34a5e-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="34a5e-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="34a5e-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="34a5e-127">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="34a5e-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="34a5e-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="34a5e-128">-AzureStoragePath</span></span>
<span data-ttu-id="34a5e-129">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="34a5e-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="34a5e-130">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="34a5e-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="34a5e-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="34a5e-131">-ConnectionStrings</span></span>
<span data-ttu-id="34a5e-132">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="34a5e-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="34a5e-133">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="34a5e-133">-ContainerImageName</span></span>
<span data-ttu-id="34a5e-134">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="34a5e-134">Container Image Name</span></span>

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

### <span data-ttu-id="34a5e-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="34a5e-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="34a5e-136">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="34a5e-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="34a5e-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="34a5e-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="34a5e-138">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="34a5e-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="34a5e-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="34a5e-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="34a5e-140">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="34a5e-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="34a5e-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="34a5e-141">-DefaultDocuments</span></span>
<span data-ttu-id="34a5e-142">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="34a5e-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="34a5e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a5e-143">-DefaultProfile</span></span>
<span data-ttu-id="34a5e-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34a5e-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34a5e-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="34a5e-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="34a5e-146">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="34a5e-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="34a5e-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="34a5e-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="34a5e-148">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="34a5e-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="34a5e-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="34a5e-149">-HandlerMappings</span></span>
<span data-ttu-id="34a5e-150">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="34a5e-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="34a5e-151">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="34a5e-151">-HostNames</span></span>
<span data-ttu-id="34a5e-152">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="34a5e-152">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="34a5e-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="34a5e-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="34a5e-154">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="34a5e-154">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="34a5e-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="34a5e-155">-HttpsOnly</span></span>
<span data-ttu-id="34a5e-156">Var olan Azure WebApp veya functionapp 'te tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="34a5e-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="34a5e-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="34a5e-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="34a5e-158">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="34a5e-158">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="34a5e-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="34a5e-159">-Name</span></span>
<span data-ttu-id="34a5e-160">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="34a5e-160">WebApp Name</span></span>

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

### <span data-ttu-id="34a5e-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="34a5e-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="34a5e-162">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="34a5e-162">Net Framework Version</span></span>

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

### <span data-ttu-id="34a5e-163">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="34a5e-163">-NumberOfWorkers</span></span>
<span data-ttu-id="34a5e-164">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="34a5e-164">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="34a5e-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="34a5e-165">-PhpVersion</span></span>
<span data-ttu-id="34a5e-166">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="34a5e-166">Php Version</span></span>

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

### <span data-ttu-id="34a5e-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="34a5e-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="34a5e-168">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="34a5e-168">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="34a5e-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a5e-169">-ResourceGroupName</span></span>
<span data-ttu-id="34a5e-170">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="34a5e-170">Resource Group Name</span></span>

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

### <span data-ttu-id="34a5e-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="34a5e-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="34a5e-172">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="34a5e-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="34a5e-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-173">-WebApp</span></span>
<span data-ttu-id="34a5e-174">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="34a5e-174">WebApp Object</span></span>

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

### <span data-ttu-id="34a5e-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="34a5e-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="34a5e-176">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="34a5e-176">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="34a5e-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a5e-177">CommonParameters</span></span>
<span data-ttu-id="34a5e-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34a5e-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a5e-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34a5e-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a5e-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34a5e-180">INPUTS</span></span>

### <span data-ttu-id="34a5e-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="34a5e-181">System.Int32</span></span>

### <span data-ttu-id="34a5e-182">System. String</span><span class="sxs-lookup"><span data-stu-id="34a5e-182">System.String</span></span>

### <span data-ttu-id="34a5e-183">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="34a5e-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="34a5e-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34a5e-184">OUTPUTS</span></span>

### <span data-ttu-id="34a5e-185">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="34a5e-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="34a5e-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34a5e-186">NOTES</span></span>

## <span data-ttu-id="34a5e-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34a5e-187">RELATED LINKS</span></span>

[<span data-ttu-id="34a5e-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="34a5e-189">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="34a5e-190">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="34a5e-191">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="34a5e-192">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="34a5e-193">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34a5e-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)