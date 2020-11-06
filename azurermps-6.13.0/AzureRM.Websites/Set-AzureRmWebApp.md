---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589985"
---
# <span data-ttu-id="7ea74-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="7ea74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ea74-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea74-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7ea74-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ea74-104">SYNTAX</span></span>

### <span data-ttu-id="7ea74-105">S1</span><span class="sxs-lookup"><span data-stu-id="7ea74-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea74-106">S2</span><span class="sxs-lookup"><span data-stu-id="7ea74-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ea74-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ea74-107">DESCRIPTION</span></span>
<span data-ttu-id="7ea74-108">**Set-AzureRmWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7ea74-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="7ea74-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ea74-109">EXAMPLES</span></span>

### <span data-ttu-id="7ea74-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ea74-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="7ea74-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="7ea74-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7ea74-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ea74-112">PARAMETERS</span></span>

### <span data-ttu-id="7ea74-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7ea74-113">-AppServicePlan</span></span>
<span data-ttu-id="7ea74-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="7ea74-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="7ea74-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="7ea74-115">-AppSettings</span></span>
<span data-ttu-id="7ea74-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="7ea74-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="7ea74-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="7ea74-117">-AsJob</span></span>
<span data-ttu-id="7ea74-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7ea74-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ea74-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="7ea74-119">-AssignIdentity</span></span>
<span data-ttu-id="7ea74-120">Mevcut Azure WebApp veya functionapp 'te MSI 'yi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7ea74-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="7ea74-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="7ea74-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="7ea74-122">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="7ea74-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="7ea74-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="7ea74-123">-ConnectionStrings</span></span>
<span data-ttu-id="7ea74-124">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="7ea74-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="7ea74-125">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="7ea74-125">-ContainerImageName</span></span>
<span data-ttu-id="7ea74-126">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="7ea74-126">Container Image Name</span></span>

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

### <span data-ttu-id="7ea74-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="7ea74-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="7ea74-128">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="7ea74-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="7ea74-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="7ea74-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="7ea74-130">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="7ea74-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="7ea74-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="7ea74-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="7ea74-132">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="7ea74-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="7ea74-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="7ea74-133">-DefaultDocuments</span></span>
<span data-ttu-id="7ea74-134">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="7ea74-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="7ea74-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea74-135">-DefaultProfile</span></span>
<span data-ttu-id="7ea74-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ea74-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea74-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7ea74-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="7ea74-138">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="7ea74-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="7ea74-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="7ea74-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="7ea74-140">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="7ea74-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="7ea74-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="7ea74-141">-HandlerMappings</span></span>
<span data-ttu-id="7ea74-142">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="7ea74-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="7ea74-143">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="7ea74-143">-HostNames</span></span>
<span data-ttu-id="7ea74-144">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="7ea74-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="7ea74-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7ea74-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="7ea74-146">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="7ea74-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="7ea74-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7ea74-147">-HttpsOnly</span></span>
<span data-ttu-id="7ea74-148">Var olan Azure WebApp veya functionapp 'te tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7ea74-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="7ea74-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="7ea74-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="7ea74-150">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="7ea74-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="7ea74-151">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ea74-151">-Name</span></span>
<span data-ttu-id="7ea74-152">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="7ea74-152">WebApp Name</span></span>

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

### <span data-ttu-id="7ea74-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="7ea74-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="7ea74-154">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="7ea74-154">Net Framework Version</span></span>

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

### <span data-ttu-id="7ea74-155">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="7ea74-155">-NumberOfWorkers</span></span>
<span data-ttu-id="7ea74-156">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="7ea74-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="7ea74-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="7ea74-157">-PhpVersion</span></span>
<span data-ttu-id="7ea74-158">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="7ea74-158">Php Version</span></span>

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

### <span data-ttu-id="7ea74-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="7ea74-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="7ea74-160">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="7ea74-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="7ea74-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea74-161">-ResourceGroupName</span></span>
<span data-ttu-id="7ea74-162">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7ea74-162">Resource Group Name</span></span>

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

### <span data-ttu-id="7ea74-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="7ea74-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="7ea74-164">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="7ea74-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="7ea74-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-165">-WebApp</span></span>
<span data-ttu-id="7ea74-166">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="7ea74-166">WebApp Object</span></span>

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

### <span data-ttu-id="7ea74-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="7ea74-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="7ea74-168">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="7ea74-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="7ea74-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea74-169">CommonParameters</span></span>
<span data-ttu-id="7ea74-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ea74-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea74-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea74-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea74-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ea74-172">INPUTS</span></span>

### <span data-ttu-id="7ea74-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7ea74-173">System.Int32</span></span>
<span data-ttu-id="7ea74-174">Parametreler: Işçilere (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7ea74-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="7ea74-175">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea74-175">System.String</span></span>

### <span data-ttu-id="7ea74-176">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="7ea74-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="7ea74-177">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7ea74-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="7ea74-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ea74-178">OUTPUTS</span></span>

### <span data-ttu-id="7ea74-179">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="7ea74-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="7ea74-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ea74-180">NOTES</span></span>

## <span data-ttu-id="7ea74-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ea74-181">RELATED LINKS</span></span>

[<span data-ttu-id="7ea74-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="7ea74-183">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="7ea74-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="7ea74-185">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="7ea74-186">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7ea74-187">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7ea74-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
