---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098079"
---
# <span data-ttu-id="4ee70-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ee70-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="4ee70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee70-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee70-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4ee70-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="4ee70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ee70-104">SYNTAX</span></span>

### <span data-ttu-id="4ee70-105">S1</span><span class="sxs-lookup"><span data-stu-id="4ee70-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ee70-106">S2</span><span class="sxs-lookup"><span data-stu-id="4ee70-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ee70-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ee70-107">DESCRIPTION</span></span>
<span data-ttu-id="4ee70-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web App yuvasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ee70-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="4ee70-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ee70-109">EXAMPLES</span></span>

### <span data-ttu-id="4ee70-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4ee70-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="4ee70-111">Bu komut Slot001 ile ilişkili appservice planını, varsayılan-Web-WestUS kaynak grubuyla ilişkili WebApp ContosoWebApp 'de değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4ee70-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="4ee70-112">Bağlantıyı kullanarak appservice planının ve onunla ilişkilendirilmiş kısıtlamaların değiştirilmesiyle ilgili daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="4ee70-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="4ee70-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="4ee70-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="4ee70-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4ee70-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="4ee70-115">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="4ee70-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4ee70-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ee70-116">PARAMETERS</span></span>

### <span data-ttu-id="4ee70-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="4ee70-117">-AlwaysOn</span></span>
<span data-ttu-id="4ee70-118">Web uygulamasının, boşta kaldıktan sonra, her zaman yüklü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4ee70-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="4ee70-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4ee70-119">-AppServicePlan</span></span>
<span data-ttu-id="4ee70-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="4ee70-121">-AppSettings</span></span>
<span data-ttu-id="4ee70-122">Uygulama ayarları HashTable.</span><span class="sxs-lookup"><span data-stu-id="4ee70-122">App Settings HashTable.</span></span> <span data-ttu-id="4ee70-123">Mevcut uygulama ayarları değiştirilecek ve sağlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="4ee70-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="4ee70-124">-AsJob</span></span>
<span data-ttu-id="4ee70-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4ee70-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ee70-126">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="4ee70-126">-AssignIdentity</span></span>
<span data-ttu-id="4ee70-127">Var olan yuvada MSI 'yi etkinleştirme/devre dışı bırakma [ÖNIZLEME]</span><span class="sxs-lookup"><span data-stu-id="4ee70-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="4ee70-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="4ee70-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="4ee70-129">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="4ee70-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="4ee70-130">-AzureStoragePath</span></span>
<span data-ttu-id="4ee70-131">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="4ee70-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="4ee70-132">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="4ee70-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="4ee70-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="4ee70-133">-ConnectionStrings</span></span>
<span data-ttu-id="4ee70-134">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="4ee70-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-135">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="4ee70-135">-ContainerImageName</span></span>
<span data-ttu-id="4ee70-136">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-136">Container Image Name</span></span>

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

### <span data-ttu-id="4ee70-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="4ee70-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="4ee70-138">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="4ee70-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="4ee70-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="4ee70-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="4ee70-140">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="4ee70-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="4ee70-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="4ee70-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="4ee70-142">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="4ee70-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="4ee70-143">-DefaultDocuments</span></span>
<span data-ttu-id="4ee70-144">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="4ee70-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee70-145">-DefaultProfile</span></span>
<span data-ttu-id="4ee70-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ee70-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee70-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="4ee70-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="4ee70-148">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="4ee70-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="4ee70-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="4ee70-150">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="4ee70-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="4ee70-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="4ee70-151">-FtpsState</span></span>
<span data-ttu-id="4ee70-152">Bir uygulamanın FTPS durum değerini ayarlama.</span><span class="sxs-lookup"><span data-stu-id="4ee70-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="4ee70-153">İzin verilen değerler [AllAllowed | Devre dışı | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="4ee70-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="4ee70-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="4ee70-154">-HandlerMappings</span></span>
<span data-ttu-id="4ee70-155">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="4ee70-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="4ee70-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="4ee70-157">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="4ee70-157">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4ee70-158">-HttpsOnly</span></span>
<span data-ttu-id="4ee70-159">Var olan bir yuvada tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4ee70-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="4ee70-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="4ee70-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="4ee70-161">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-161">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4ee70-162">-MinTlsVersion</span></span>
<span data-ttu-id="4ee70-163">SSL istekleri için gereken en düşük TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="4ee70-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="4ee70-164">İzin verilen değerler [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="4ee70-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="4ee70-165">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ee70-165">-Name</span></span>
<span data-ttu-id="4ee70-166">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-166">WebApp Name</span></span>

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

### <span data-ttu-id="4ee70-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="4ee70-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="4ee70-168">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="4ee70-168">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-169">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="4ee70-169">-NumberOfWorkers</span></span>
<span data-ttu-id="4ee70-170">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="4ee70-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="4ee70-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="4ee70-171">-PhpVersion</span></span>
<span data-ttu-id="4ee70-172">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="4ee70-172">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="4ee70-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="4ee70-174">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="4ee70-174">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee70-175">-ResourceGroupName</span></span>
<span data-ttu-id="4ee70-176">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-176">Resource Group Name</span></span>

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

### <span data-ttu-id="4ee70-177">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4ee70-177">-Slot</span></span>
<span data-ttu-id="4ee70-178">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="4ee70-178">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="4ee70-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="4ee70-180">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="4ee70-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee70-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4ee70-181">-WebApp</span></span>
<span data-ttu-id="4ee70-182">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="4ee70-182">WebApp Object</span></span>

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

### <span data-ttu-id="4ee70-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="4ee70-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="4ee70-184">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="4ee70-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="4ee70-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee70-185">CommonParameters</span></span>
<span data-ttu-id="4ee70-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ee70-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee70-187">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4ee70-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee70-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ee70-188">INPUTS</span></span>

### <span data-ttu-id="4ee70-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4ee70-189">System.Int32</span></span>

### <span data-ttu-id="4ee70-190">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee70-190">System.String</span></span>

### <span data-ttu-id="4ee70-191">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="4ee70-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4ee70-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ee70-192">OUTPUTS</span></span>

### <span data-ttu-id="4ee70-193">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="4ee70-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4ee70-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ee70-194">NOTES</span></span>

## <span data-ttu-id="4ee70-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ee70-195">RELATED LINKS</span></span>

[<span data-ttu-id="4ee70-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ee70-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="4ee70-197">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ee70-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="4ee70-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ee70-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="4ee70-199">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ee70-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="4ee70-200">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ee70-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="4ee70-201">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ee70-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="4ee70-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4ee70-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
