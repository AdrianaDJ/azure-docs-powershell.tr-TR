---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934473"
---
# <span data-ttu-id="9ffa4-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9ffa4-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="9ffa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ffa4-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffa4-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="9ffa4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ffa4-104">SYNTAX</span></span>

### <span data-ttu-id="9ffa4-105">S1</span><span class="sxs-lookup"><span data-stu-id="9ffa4-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ffa4-106">S2</span><span class="sxs-lookup"><span data-stu-id="9ffa4-106">S2</span></span>
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

## <span data-ttu-id="9ffa4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ffa4-107">DESCRIPTION</span></span>
<span data-ttu-id="9ffa4-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web App yuvasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="9ffa4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ffa4-109">EXAMPLES</span></span>

### <span data-ttu-id="9ffa4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ffa4-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="9ffa4-111">Bu komut Slot001 ile ilişkili appservice planını, varsayılan-Web-WestUS kaynak grubuyla ilişkili WebApp ContosoWebApp 'de değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="9ffa4-112">Bağlantıyı kullanarak appservice planının ve onunla ilişkilendirilmiş kısıtlamaların değiştirilmesiyle ilgili daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="9ffa4-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="9ffa4-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="9ffa4-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9ffa4-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="9ffa4-115">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="9ffa4-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="9ffa4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ffa4-116">PARAMETERS</span></span>

### <span data-ttu-id="9ffa4-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ffa4-117">-AppServicePlan</span></span>
<span data-ttu-id="9ffa4-118">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="9ffa4-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9ffa4-119">-AppSettings</span></span>
<span data-ttu-id="9ffa4-120">Uygulama ayarları HashTable.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-120">App Settings HashTable.</span></span> <span data-ttu-id="9ffa4-121">Mevcut uygulama ayarları değiştirilecek ve sağlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="9ffa4-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="9ffa4-122">-AsJob</span></span>
<span data-ttu-id="9ffa4-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9ffa4-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ffa4-124">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="9ffa4-124">-AssignIdentity</span></span>
<span data-ttu-id="9ffa4-125">Var olan yuvada MSI 'yi etkinleştirme/devre dışı bırakma [ÖNIZLEME]</span><span class="sxs-lookup"><span data-stu-id="9ffa4-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="9ffa4-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9ffa4-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="9ffa4-127">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="9ffa4-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="9ffa4-128">-AzureStoragePath</span></span>
<span data-ttu-id="9ffa4-129">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="9ffa4-130">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="9ffa4-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="9ffa4-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="9ffa4-131">-ConnectionStrings</span></span>
<span data-ttu-id="9ffa4-132">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="9ffa4-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="9ffa4-133">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-133">-ContainerImageName</span></span>
<span data-ttu-id="9ffa4-134">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-134">Container Image Name</span></span>

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

### <span data-ttu-id="9ffa4-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9ffa4-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9ffa4-136">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="9ffa4-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9ffa4-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9ffa4-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9ffa4-138">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="9ffa4-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9ffa4-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9ffa4-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="9ffa4-140">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9ffa4-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="9ffa4-141">-DefaultDocuments</span></span>
<span data-ttu-id="9ffa4-142">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="9ffa4-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="9ffa4-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffa4-143">-DefaultProfile</span></span>
<span data-ttu-id="9ffa4-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ffa4-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9ffa4-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9ffa4-146">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="9ffa4-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="9ffa4-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9ffa4-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9ffa4-148">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="9ffa4-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9ffa4-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9ffa4-149">-HandlerMappings</span></span>
<span data-ttu-id="9ffa4-150">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="9ffa4-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="9ffa4-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9ffa4-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9ffa4-152">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="9ffa4-152">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="9ffa4-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9ffa4-153">-HttpsOnly</span></span>
<span data-ttu-id="9ffa4-154">Var olan bir yuvada tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9ffa4-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="9ffa4-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9ffa4-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="9ffa4-156">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-156">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="9ffa4-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ffa4-157">-Name</span></span>
<span data-ttu-id="9ffa4-158">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-158">WebApp Name</span></span>

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

### <span data-ttu-id="9ffa4-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9ffa4-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="9ffa4-160">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="9ffa4-160">Net Framework Version</span></span>

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

### <span data-ttu-id="9ffa4-161">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="9ffa4-161">-NumberOfWorkers</span></span>
<span data-ttu-id="9ffa4-162">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-162">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="9ffa4-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9ffa4-163">-PhpVersion</span></span>
<span data-ttu-id="9ffa4-164">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="9ffa4-164">Php Version</span></span>

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

### <span data-ttu-id="9ffa4-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9ffa4-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="9ffa4-166">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="9ffa4-166">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="9ffa4-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ffa4-167">-ResourceGroupName</span></span>
<span data-ttu-id="9ffa4-168">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-168">Resource Group Name</span></span>

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

### <span data-ttu-id="9ffa4-169">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-169">-Slot</span></span>
<span data-ttu-id="9ffa4-170">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="9ffa4-170">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9ffa4-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9ffa4-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9ffa4-172">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="9ffa4-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="9ffa4-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9ffa4-173">-WebApp</span></span>
<span data-ttu-id="9ffa4-174">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="9ffa4-174">WebApp Object</span></span>

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

### <span data-ttu-id="9ffa4-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9ffa4-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="9ffa4-176">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="9ffa4-176">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="9ffa4-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffa4-177">CommonParameters</span></span>
<span data-ttu-id="9ffa4-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ffa4-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffa4-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ffa4-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffa4-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ffa4-180">INPUTS</span></span>

### <span data-ttu-id="9ffa4-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9ffa4-181">System.Int32</span></span>

### <span data-ttu-id="9ffa4-182">System. String</span><span class="sxs-lookup"><span data-stu-id="9ffa4-182">System.String</span></span>

### <span data-ttu-id="9ffa4-183">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="9ffa4-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9ffa4-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ffa4-184">OUTPUTS</span></span>

### <span data-ttu-id="9ffa4-185">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="9ffa4-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9ffa4-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ffa4-186">NOTES</span></span>

## <span data-ttu-id="9ffa4-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ffa4-187">RELATED LINKS</span></span>

[<span data-ttu-id="9ffa4-188">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9ffa4-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="9ffa4-189">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9ffa4-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="9ffa4-190">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9ffa4-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="9ffa4-191">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9ffa4-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="9ffa4-192">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9ffa4-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="9ffa4-193">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9ffa4-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="9ffa4-194">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ffa4-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
