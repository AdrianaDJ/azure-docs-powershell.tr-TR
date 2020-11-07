---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753776"
---
# <span data-ttu-id="71d97-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-101">Set-AzWebApp</span></span>



## <span data-ttu-id="71d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71d97-102">SYNOPSIS</span></span>

<span data-ttu-id="71d97-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="71d97-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="71d97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71d97-104">SYNTAX</span></span>



### <span data-ttu-id="71d97-105">S1</span><span class="sxs-lookup"><span data-stu-id="71d97-105">S1</span></span>

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



### <span data-ttu-id="71d97-106">S2</span><span class="sxs-lookup"><span data-stu-id="71d97-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="71d97-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="71d97-107">DESCRIPTION</span></span>

<span data-ttu-id="71d97-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="71d97-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="71d97-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71d97-109">EXAMPLES</span></span>



### <span data-ttu-id="71d97-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="71d97-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="71d97-111">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp ile ilişkili appservice planını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="71d97-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="71d97-112">Bu bağlantıyı kullanarak appservice planı ve onunla ilişkilendirilmiş kısıtlamaları değiştirme hakkında daha fazla bilgi.</span><span class="sxs-lookup"><span data-stu-id="71d97-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="71d97-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="71d97-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="71d97-114">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="71d97-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="71d97-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71d97-115">PARAMETERS</span></span>



### <span data-ttu-id="71d97-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="71d97-116">-AppServicePlan</span></span>

<span data-ttu-id="71d97-117">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="71d97-117">App Service Plan Name</span></span>



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



### <span data-ttu-id="71d97-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="71d97-118">-AppSettings</span></span>

<span data-ttu-id="71d97-119">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="71d97-119">App Settings HashTable</span></span>



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



### <span data-ttu-id="71d97-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="71d97-120">-AsJob</span></span>

<span data-ttu-id="71d97-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="71d97-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="71d97-122">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="71d97-122">-AssignIdentity</span></span>

<span data-ttu-id="71d97-123">Mevcut Azure WebApp veya functionapp 'te MSI 'yi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="71d97-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="71d97-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="71d97-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="71d97-125">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="71d97-125">Destination slot name for auto swap</span></span>



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



### <span data-ttu-id="71d97-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="71d97-126">-AzureStoragePath</span></span>

<span data-ttu-id="71d97-127">Kapsayıcı için bir Web uygulamasının içinde takılacak Azure depolaması.</span><span class="sxs-lookup"><span data-stu-id="71d97-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="71d97-128">Oluşturmak için New-AzureRmWebAppAzureStoragePath kullanma</span><span class="sxs-lookup"><span data-stu-id="71d97-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



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



### <span data-ttu-id="71d97-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="71d97-129">-ConnectionStrings</span></span>

<span data-ttu-id="71d97-130">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="71d97-130">Connection Strings HashTable</span></span>



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



### <span data-ttu-id="71d97-131">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="71d97-131">-ContainerImageName</span></span>

<span data-ttu-id="71d97-132">Kapsayıcı görüntü adı</span><span class="sxs-lookup"><span data-stu-id="71d97-132">Container Image Name</span></span>



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



### <span data-ttu-id="71d97-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="71d97-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="71d97-134">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="71d97-134">Private Container Registry Password</span></span>



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



### <span data-ttu-id="71d97-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="71d97-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="71d97-136">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="71d97-136">Private Container Registry Server Url</span></span>



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



### <span data-ttu-id="71d97-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="71d97-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="71d97-138">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="71d97-138">Private Container Registry Username</span></span>



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



### <span data-ttu-id="71d97-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="71d97-139">-DefaultDocuments</span></span>

<span data-ttu-id="71d97-140">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="71d97-140">Default Documents String Array</span></span>



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



### <span data-ttu-id="71d97-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d97-141">-DefaultProfile</span></span>

<span data-ttu-id="71d97-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71d97-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="71d97-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="71d97-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="71d97-144">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="71d97-144">Detailed Error Logging Enabled Boolean</span></span>



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



### <span data-ttu-id="71d97-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="71d97-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="71d97-146">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="71d97-146">Enables/Disables container continuous deployment webhook</span></span>



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



### <span data-ttu-id="71d97-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="71d97-147">-HandlerMappings</span></span>

<span data-ttu-id="71d97-148">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="71d97-148">Handler Mappings IList</span></span>



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



### <span data-ttu-id="71d97-149">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="71d97-149">-HostNames</span></span>

<span data-ttu-id="71d97-150">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="71d97-150">WebApp HostNames String Array</span></span>



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



### <span data-ttu-id="71d97-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="71d97-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="71d97-152">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="71d97-152">HttpLoggingEnabled Boolean</span></span>



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



### <span data-ttu-id="71d97-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="71d97-153">-HttpsOnly</span></span>

<span data-ttu-id="71d97-154">Var olan Azure WebApp veya functionapp 'te tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="71d97-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="71d97-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="71d97-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="71d97-156">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="71d97-156">Managed Pipeline Mode Name</span></span>



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



### <span data-ttu-id="71d97-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="71d97-157">-Name</span></span>

<span data-ttu-id="71d97-158">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="71d97-158">WebApp Name</span></span>



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



### <span data-ttu-id="71d97-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="71d97-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="71d97-160">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="71d97-160">Net Framework Version</span></span>



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



### <span data-ttu-id="71d97-161">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="71d97-161">-NumberOfWorkers</span></span>

<span data-ttu-id="71d97-162">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="71d97-162">The number of workers to be allocated</span></span>



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



### <span data-ttu-id="71d97-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="71d97-163">-PhpVersion</span></span>

<span data-ttu-id="71d97-164">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="71d97-164">Php Version</span></span>



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



### <span data-ttu-id="71d97-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="71d97-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="71d97-166">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="71d97-166">Request Tracing Enabled</span></span>



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



### <span data-ttu-id="71d97-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d97-167">-ResourceGroupName</span></span>

<span data-ttu-id="71d97-168">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="71d97-168">Resource Group Name</span></span>



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



### <span data-ttu-id="71d97-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="71d97-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="71d97-170">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="71d97-170">Use 32-bit Worker Process Boolean</span></span>



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



### <span data-ttu-id="71d97-171">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-171">-WebApp</span></span>

<span data-ttu-id="71d97-172">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="71d97-172">WebApp Object</span></span>



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



### <span data-ttu-id="71d97-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="71d97-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="71d97-174">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="71d97-174">WebSocketsEnabled Boolean</span></span>



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



### <span data-ttu-id="71d97-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d97-175">CommonParameters</span></span>

<span data-ttu-id="71d97-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71d97-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d97-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d97-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="71d97-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71d97-178">INPUTS</span></span>



### <span data-ttu-id="71d97-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71d97-179">System.Int32</span></span>



### <span data-ttu-id="71d97-180">System. String</span><span class="sxs-lookup"><span data-stu-id="71d97-180">System.String</span></span>



### <span data-ttu-id="71d97-181">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="71d97-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="71d97-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71d97-182">OUTPUTS</span></span>



### <span data-ttu-id="71d97-183">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="71d97-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="71d97-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71d97-184">NOTES</span></span>



## <span data-ttu-id="71d97-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71d97-185">RELATED LINKS</span></span>



[<span data-ttu-id="71d97-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="71d97-187">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="71d97-188">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="71d97-189">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="71d97-190">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="71d97-191">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71d97-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

