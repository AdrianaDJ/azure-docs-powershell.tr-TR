---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097158"
---
# <span data-ttu-id="41e9f-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41e9f-101">New-AzWebApp</span></span>

## <span data-ttu-id="41e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="41e9f-103">Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41e9f-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="41e9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41e9f-104">SYNTAX</span></span>

### <span data-ttu-id="41e9f-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="41e9f-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41e9f-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="41e9f-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41e9f-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="41e9f-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41e9f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="41e9f-108">DESCRIPTION</span></span>
<span data-ttu-id="41e9f-109">**New-AzWebApp** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41e9f-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="41e9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41e9f-110">EXAMPLES</span></span>

### <span data-ttu-id="41e9f-111">Örnek 1: Web uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="41e9f-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="41e9f-112">Bu komut, veri merkezi Batı 'da Default-Web-WestUS adlı var olan kaynak grubunda ContosoSite adlı bir Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41e9f-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="41e9f-113">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="41e9f-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="41e9f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41e9f-114">PARAMETERS</span></span>

### <span data-ttu-id="41e9f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="41e9f-115">-AppServicePlan</span></span>
<span data-ttu-id="41e9f-116">App Service planlama adı veya App Service planlama kimliği. WebApp ve App hizmet planı farklı kaynak gruplarınızda, ad yerine KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="41e9f-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="41e9f-117">App Service planlama kimliği,: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. id kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="41e9f-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="41e9f-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="41e9f-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="41e9f-119">Uygulama ayarları HashTable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="41e9f-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="41e9f-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="41e9f-120">-AseName</span></span>
<span data-ttu-id="41e9f-121">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="41e9f-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="41e9f-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e9f-122">-AseResourceGroupName</span></span>
<span data-ttu-id="41e9f-123">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="41e9f-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="41e9f-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="41e9f-124">-AsJob</span></span>
<span data-ttu-id="41e9f-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="41e9f-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41e9f-126">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="41e9f-126">-ContainerImageName</span></span>
<span data-ttu-id="41e9f-127">Kapsayıcı görüntü adı ve isteğe bağlı etiketi (Image: Tag)</span><span class="sxs-lookup"><span data-stu-id="41e9f-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="41e9f-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="41e9f-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="41e9f-129">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="41e9f-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="41e9f-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="41e9f-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="41e9f-131">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="41e9f-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="41e9f-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="41e9f-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="41e9f-133">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="41e9f-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="41e9f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e9f-134">-DefaultProfile</span></span>
<span data-ttu-id="41e9f-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41e9f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41e9f-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="41e9f-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="41e9f-137">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="41e9f-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="41e9f-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="41e9f-138">-GitRepositoryPath</span></span>
<span data-ttu-id="41e9f-139">Dağıtılacak Web uygulamasını içeren GitHub deposunun yolu.</span><span class="sxs-lookup"><span data-stu-id="41e9f-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="41e9f-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="41e9f-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="41e9f-141">Özel ana bilgisayar adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="41e9f-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="41e9f-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="41e9f-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="41e9f-143">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="41e9f-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="41e9f-144">-Includesourcewebappyuvaları</span><span class="sxs-lookup"><span data-stu-id="41e9f-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="41e9f-145">Kaynak WebApp yuvalarını ekleme seçeneği</span><span class="sxs-lookup"><span data-stu-id="41e9f-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="41e9f-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="41e9f-146">-Location</span></span>
<span data-ttu-id="41e9f-147">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="41e9f-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e9f-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="41e9f-148">-Name</span></span>
<span data-ttu-id="41e9f-149">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="41e9f-149">WebApp Name</span></span>

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

### <span data-ttu-id="41e9f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e9f-150">-ResourceGroupName</span></span>
<span data-ttu-id="41e9f-151">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="41e9f-151">Resource Group Name</span></span>

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

### <span data-ttu-id="41e9f-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="41e9f-152">-SourceWebApp</span></span>
<span data-ttu-id="41e9f-153">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="41e9f-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="41e9f-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e9f-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="41e9f-155">Var olan Traffic Manager profilinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="41e9f-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="41e9f-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="41e9f-156">-Confirm</span></span>
<span data-ttu-id="41e9f-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="41e9f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e9f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e9f-158">-WhatIf</span></span>
<span data-ttu-id="41e9f-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="41e9f-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41e9f-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="41e9f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e9f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e9f-161">CommonParameters</span></span>
<span data-ttu-id="41e9f-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41e9f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e9f-163">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e9f-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e9f-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41e9f-164">INPUTS</span></span>

### <span data-ttu-id="41e9f-165">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="41e9f-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41e9f-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41e9f-166">OUTPUTS</span></span>

### <span data-ttu-id="41e9f-167">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="41e9f-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41e9f-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41e9f-168">NOTES</span></span>

## <span data-ttu-id="41e9f-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41e9f-169">RELATED LINKS</span></span>

[<span data-ttu-id="41e9f-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41e9f-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="41e9f-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41e9f-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="41e9f-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41e9f-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="41e9f-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41e9f-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="41e9f-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41e9f-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

