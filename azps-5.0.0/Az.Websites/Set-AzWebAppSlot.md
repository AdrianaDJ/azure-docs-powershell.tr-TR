---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279418"
---
# <span data-ttu-id="8e0d9-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e0d9-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="8e0d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0d9-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="8e0d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e0d9-104">SYNTAX</span></span>

### <span data-ttu-id="8e0d9-105">S1</span><span class="sxs-lookup"><span data-stu-id="8e0d9-105">S1</span></span>
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

### <span data-ttu-id="8e0d9-106">S2</span><span class="sxs-lookup"><span data-stu-id="8e0d9-106">S2</span></span>
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

## <span data-ttu-id="8e0d9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e0d9-107">DESCRIPTION</span></span>
<span data-ttu-id="8e0d9-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web App yuvasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="8e0d9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e0d9-109">EXAMPLES</span></span>

### <span data-ttu-id="8e0d9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8e0d9-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="8e0d9-111">Bu komut Slot001 ile ilişkili appservice planını, varsayılan-Web-WestUS kaynak grubuyla ilişkili WebApp ContosoWebApp 'de değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="8e0d9-112">Bağlantıyı kullanarak appservice planının ve onunla ilişkilendirilmiş kısıtlamaların değiştirilmesiyle ilgili daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="8e0d9-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="8e0d9-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="8e0d9-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8e0d9-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="8e0d9-115">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="8e0d9-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="8e0d9-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8e0d9-116">Example 3</span></span>

<span data-ttu-id="8e0d9-117">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="8e0d9-118">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="8e0d9-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="8e0d9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e0d9-119">PARAMETERS</span></span>

### <span data-ttu-id="8e0d9-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="8e0d9-120">-AlwaysOn</span></span>
<span data-ttu-id="8e0d9-121">Web uygulamasının, boşta kaldıktan sonra, her zaman yüklü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="8e0d9-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8e0d9-122">-AppServicePlan</span></span>
<span data-ttu-id="8e0d9-123">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="8e0d9-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="8e0d9-124">-AppSettings</span></span>
<span data-ttu-id="8e0d9-125">Uygulama ayarları HashTable.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-125">App Settings HashTable.</span></span> <span data-ttu-id="8e0d9-126">Mevcut uygulama ayarları değiştirilecek ve sağlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="8e0d9-127">-Iş</span><span class="sxs-lookup"><span data-stu-id="8e0d9-127">-AsJob</span></span>
<span data-ttu-id="8e0d9-128">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8e0d9-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e0d9-129">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="8e0d9-129">-AssignIdentity</span></span>
<span data-ttu-id="8e0d9-130">Var olan yuvada MSI 'yi etkinleştirme/devre dışı bırakma [ÖNIZLEME]</span><span class="sxs-lookup"><span data-stu-id="8e0d9-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="8e0d9-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="8e0d9-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="8e0d9-132">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="8e0d9-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8e0d9-133">-AzureStoragePath</span></span>
<span data-ttu-id="8e0d9-134">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="8e0d9-135">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="8e0d9-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="8e0d9-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="8e0d9-136">-ConnectionStrings</span></span>
<span data-ttu-id="8e0d9-137">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="8e0d9-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="8e0d9-138">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-138">-ContainerImageName</span></span>
<span data-ttu-id="8e0d9-139">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-139">Container Image Name</span></span>

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

### <span data-ttu-id="8e0d9-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8e0d9-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8e0d9-141">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="8e0d9-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8e0d9-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8e0d9-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8e0d9-143">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="8e0d9-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8e0d9-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8e0d9-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="8e0d9-145">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8e0d9-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="8e0d9-146">-DefaultDocuments</span></span>
<span data-ttu-id="8e0d9-147">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="8e0d9-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="8e0d9-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0d9-148">-DefaultProfile</span></span>
<span data-ttu-id="8e0d9-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e0d9-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8e0d9-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="8e0d9-151">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="8e0d9-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="8e0d9-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8e0d9-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8e0d9-153">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="8e0d9-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8e0d9-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="8e0d9-154">-FtpsState</span></span>
<span data-ttu-id="8e0d9-155">Bir uygulamanın FTPS durum değerini ayarlama.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="8e0d9-156">İzin verilen değerler [AllAllowed | Devre dışı | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="8e0d9-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="8e0d9-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="8e0d9-157">-HandlerMappings</span></span>
<span data-ttu-id="8e0d9-158">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="8e0d9-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="8e0d9-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8e0d9-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="8e0d9-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="8e0d9-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="8e0d9-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8e0d9-161">-HttpsOnly</span></span>
<span data-ttu-id="8e0d9-162">Var olan bir yuvada tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="8e0d9-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="8e0d9-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="8e0d9-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="8e0d9-164">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="8e0d9-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8e0d9-165">-MinTlsVersion</span></span>
<span data-ttu-id="8e0d9-166">SSL istekleri için gereken en düşük TLS sürümü.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="8e0d9-167">İzin verilen değerler [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="8e0d9-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="8e0d9-168">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e0d9-168">-Name</span></span>
<span data-ttu-id="8e0d9-169">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-169">WebApp Name</span></span>

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

### <span data-ttu-id="8e0d9-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="8e0d9-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="8e0d9-171">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="8e0d9-171">Net Framework Version</span></span>

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

### <span data-ttu-id="8e0d9-172">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="8e0d9-172">-NumberOfWorkers</span></span>
<span data-ttu-id="8e0d9-173">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="8e0d9-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="8e0d9-174">-PhpVersion</span></span>
<span data-ttu-id="8e0d9-175">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="8e0d9-175">Php Version</span></span>

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

### <span data-ttu-id="8e0d9-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="8e0d9-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="8e0d9-177">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="8e0d9-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="8e0d9-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0d9-178">-ResourceGroupName</span></span>
<span data-ttu-id="8e0d9-179">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-179">Resource Group Name</span></span>

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

### <span data-ttu-id="8e0d9-180">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-180">-Slot</span></span>
<span data-ttu-id="8e0d9-181">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="8e0d9-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8e0d9-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="8e0d9-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="8e0d9-183">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="8e0d9-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="8e0d9-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8e0d9-184">-WebApp</span></span>
<span data-ttu-id="8e0d9-185">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8e0d9-185">WebApp Object</span></span>

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

### <span data-ttu-id="8e0d9-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="8e0d9-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="8e0d9-187">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="8e0d9-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="8e0d9-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0d9-188">CommonParameters</span></span>
<span data-ttu-id="8e0d9-189">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0d9-190">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8e0d9-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0d9-191">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e0d9-191">INPUTS</span></span>

### <span data-ttu-id="8e0d9-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8e0d9-192">System.Int32</span></span>

### <span data-ttu-id="8e0d9-193">System. String</span><span class="sxs-lookup"><span data-stu-id="8e0d9-193">System.String</span></span>

### <span data-ttu-id="8e0d9-194">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="8e0d9-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8e0d9-195">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e0d9-195">OUTPUTS</span></span>

### <span data-ttu-id="8e0d9-196">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="8e0d9-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8e0d9-197">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e0d9-197">NOTES</span></span>

## <span data-ttu-id="8e0d9-198">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e0d9-198">RELATED LINKS</span></span>

[<span data-ttu-id="8e0d9-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e0d9-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8e0d9-200">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e0d9-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8e0d9-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e0d9-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8e0d9-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e0d9-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8e0d9-203">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e0d9-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8e0d9-204">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e0d9-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8e0d9-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8e0d9-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
