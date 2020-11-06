---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572553"
---
# <span data-ttu-id="97b0d-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="97b0d-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="97b0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="97b0d-103">Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97b0d-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97b0d-104">SYNTAX</span></span>

### <span data-ttu-id="97b0d-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97b0d-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97b0d-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="97b0d-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b0d-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b0d-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97b0d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97b0d-108">DESCRIPTION</span></span>
<span data-ttu-id="97b0d-109">**Yeni-AzureRmWebApp** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan belirli bir kaynak grubunda Azure Web App oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97b0d-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="97b0d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97b0d-110">EXAMPLES</span></span>

### <span data-ttu-id="97b0d-111">Örnek 1: Web uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="97b0d-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="97b0d-112">Bu komut, veri merkezi Batı 'da Default-Web-WestUS adlı var olan kaynak grubunda ContosoSite adlı bir Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97b0d-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="97b0d-113">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="97b0d-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="97b0d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97b0d-114">PARAMETERS</span></span>

### <span data-ttu-id="97b0d-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97b0d-115">-AppServicePlan</span></span>
<span data-ttu-id="97b0d-116">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="97b0d-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="97b0d-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="97b0d-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="97b0d-118">Uygulama ayarları HashTable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="97b0d-118">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="97b0d-119">-AseName</span></span>
<span data-ttu-id="97b0d-120">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="97b0d-120">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b0d-121">-AseResourceGroupName</span></span>
<span data-ttu-id="97b0d-122">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="97b0d-122">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="97b0d-123">-AsJob</span></span>
<span data-ttu-id="97b0d-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="97b0d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97b0d-125">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="97b0d-125">-ContainerImageName</span></span>
<span data-ttu-id="97b0d-126">Kapsayıcı görüntü adı ve isteğe bağlı etiketi (Image: Tag)</span><span class="sxs-lookup"><span data-stu-id="97b0d-126">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="97b0d-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="97b0d-128">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="97b0d-128">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="97b0d-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="97b0d-130">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="97b0d-130">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="97b0d-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="97b0d-132">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="97b0d-132">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b0d-133">-DefaultProfile</span></span>
<span data-ttu-id="97b0d-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97b0d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b0d-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="97b0d-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="97b0d-136">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="97b0d-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="97b0d-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="97b0d-137">-GitRepositoryPath</span></span>
<span data-ttu-id="97b0d-138">Web uygulamasına dağıtılacak GitHub deposunun yolu.</span><span class="sxs-lookup"><span data-stu-id="97b0d-138">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="97b0d-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="97b0d-140">Özel ana bilgisayar adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="97b0d-140">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="97b0d-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="97b0d-142">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="97b0d-142">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-143">-Includesourcewebappyuvaları</span><span class="sxs-lookup"><span data-stu-id="97b0d-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="97b0d-144">Kaynak WebApp yuvalarını ekleme seçeneği</span><span class="sxs-lookup"><span data-stu-id="97b0d-144">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="97b0d-145">-Location</span></span>
<span data-ttu-id="97b0d-146">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="97b0d-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="97b0d-147">-Name</span></span>
<span data-ttu-id="97b0d-148">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="97b0d-148">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b0d-149">-ResourceGroupName</span></span>
<span data-ttu-id="97b0d-150">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="97b0d-150">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="97b0d-151">-SourceWebApp</span></span>
<span data-ttu-id="97b0d-152">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="97b0d-152">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97b0d-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="97b0d-154">Var olan Traffic Manager profilinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="97b0d-154">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="97b0d-155">-Confirm</span></span>
<span data-ttu-id="97b0d-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97b0d-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b0d-157">-WhatIf</span></span>
<span data-ttu-id="97b0d-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97b0d-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97b0d-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97b0d-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b0d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b0d-160">CommonParameters</span></span>
<span data-ttu-id="97b0d-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97b0d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b0d-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b0d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b0d-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97b0d-163">INPUTS</span></span>

### <span data-ttu-id="97b0d-164">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="97b0d-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="97b0d-165">Parametreler: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97b0d-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="97b0d-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97b0d-166">OUTPUTS</span></span>

### <span data-ttu-id="97b0d-167">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="97b0d-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="97b0d-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97b0d-168">NOTES</span></span>

## <span data-ttu-id="97b0d-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97b0d-169">RELATED LINKS</span></span>

[<span data-ttu-id="97b0d-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="97b0d-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="97b0d-171">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="97b0d-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="97b0d-172">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="97b0d-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="97b0d-173">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="97b0d-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="97b0d-174">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="97b0d-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


