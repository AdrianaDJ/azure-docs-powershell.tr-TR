---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590769"
---
# <span data-ttu-id="96b69-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96b69-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="96b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b69-102">SYNOPSIS</span></span>
<span data-ttu-id="96b69-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="96b69-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96b69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96b69-104">SYNTAX</span></span>

### <span data-ttu-id="96b69-105">S1</span><span class="sxs-lookup"><span data-stu-id="96b69-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96b69-106">S2</span><span class="sxs-lookup"><span data-stu-id="96b69-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96b69-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="96b69-107">DESCRIPTION</span></span>
<span data-ttu-id="96b69-108">**Set-AzureRmWebApp** cmdlet 'ı bir Azure Web App yuvası ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96b69-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="96b69-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96b69-109">EXAMPLES</span></span>

### <span data-ttu-id="96b69-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="96b69-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="96b69-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="96b69-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="96b69-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96b69-112">PARAMETERS</span></span>

### <span data-ttu-id="96b69-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="96b69-113">-AppServicePlan</span></span>
<span data-ttu-id="96b69-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="96b69-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="96b69-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="96b69-115">-AppSettings</span></span>
<span data-ttu-id="96b69-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="96b69-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="96b69-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="96b69-117">-AsJob</span></span>
<span data-ttu-id="96b69-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="96b69-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96b69-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="96b69-119">-AssignIdentity</span></span>
<span data-ttu-id="96b69-120">Var olan yuvada MSI 'yi etkinleştirme/devre dışı bırakma [ÖNIZLEME]</span><span class="sxs-lookup"><span data-stu-id="96b69-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="96b69-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="96b69-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="96b69-122">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="96b69-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="96b69-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="96b69-123">-ConnectionStrings</span></span>
<span data-ttu-id="96b69-124">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="96b69-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="96b69-125">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="96b69-125">-ContainerImageName</span></span>
<span data-ttu-id="96b69-126">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="96b69-126">Container Image Name</span></span>

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

### <span data-ttu-id="96b69-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="96b69-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="96b69-128">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="96b69-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="96b69-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="96b69-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="96b69-130">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="96b69-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="96b69-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="96b69-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="96b69-132">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="96b69-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="96b69-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="96b69-133">-DefaultDocuments</span></span>
<span data-ttu-id="96b69-134">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="96b69-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="96b69-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b69-135">-DefaultProfile</span></span>
<span data-ttu-id="96b69-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96b69-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96b69-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="96b69-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="96b69-138">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="96b69-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="96b69-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="96b69-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="96b69-140">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="96b69-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="96b69-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="96b69-141">-HandlerMappings</span></span>
<span data-ttu-id="96b69-142">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="96b69-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="96b69-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="96b69-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="96b69-144">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="96b69-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="96b69-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="96b69-145">-HttpsOnly</span></span>
<span data-ttu-id="96b69-146">Var olan bir yuvada tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="96b69-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="96b69-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="96b69-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="96b69-148">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="96b69-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="96b69-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="96b69-149">-Name</span></span>
<span data-ttu-id="96b69-150">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="96b69-150">WebApp Name</span></span>

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

### <span data-ttu-id="96b69-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="96b69-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="96b69-152">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="96b69-152">Net Framework Version</span></span>

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

### <span data-ttu-id="96b69-153">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="96b69-153">-NumberOfWorkers</span></span>
<span data-ttu-id="96b69-154">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="96b69-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="96b69-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="96b69-155">-PhpVersion</span></span>
<span data-ttu-id="96b69-156">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="96b69-156">Php Version</span></span>

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

### <span data-ttu-id="96b69-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="96b69-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="96b69-158">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="96b69-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="96b69-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b69-159">-ResourceGroupName</span></span>
<span data-ttu-id="96b69-160">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="96b69-160">Resource Group Name</span></span>

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

### <span data-ttu-id="96b69-161">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="96b69-161">-Slot</span></span>
<span data-ttu-id="96b69-162">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="96b69-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="96b69-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="96b69-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="96b69-164">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="96b69-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="96b69-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="96b69-165">-WebApp</span></span>
<span data-ttu-id="96b69-166">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="96b69-166">WebApp Object</span></span>

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

### <span data-ttu-id="96b69-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="96b69-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="96b69-168">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="96b69-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="96b69-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b69-169">CommonParameters</span></span>
<span data-ttu-id="96b69-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96b69-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b69-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b69-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b69-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96b69-172">INPUTS</span></span>

### <span data-ttu-id="96b69-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="96b69-173">System.Int32</span></span>
<span data-ttu-id="96b69-174">Parametreler: Işçilere (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96b69-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="96b69-175">System. String</span><span class="sxs-lookup"><span data-stu-id="96b69-175">System.String</span></span>

### <span data-ttu-id="96b69-176">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="96b69-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="96b69-177">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96b69-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="96b69-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96b69-178">OUTPUTS</span></span>

### <span data-ttu-id="96b69-179">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="96b69-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="96b69-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96b69-180">NOTES</span></span>

## <span data-ttu-id="96b69-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96b69-181">RELATED LINKS</span></span>

[<span data-ttu-id="96b69-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96b69-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="96b69-183">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96b69-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="96b69-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96b69-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="96b69-185">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96b69-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="96b69-186">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96b69-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="96b69-187">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96b69-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="96b69-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="96b69-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
