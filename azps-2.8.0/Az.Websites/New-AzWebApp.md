---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 9d544d48a430aa671c0c18721e6dece6f1351424
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934325"
---
# <span data-ttu-id="7d1dd-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1dd-101">New-AzWebApp</span></span>

## <span data-ttu-id="7d1dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1dd-103">Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="7d1dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d1dd-104">SYNTAX</span></span>

### <span data-ttu-id="7d1dd-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d1dd-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1dd-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="7d1dd-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1dd-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1dd-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1dd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d1dd-108">DESCRIPTION</span></span>
<span data-ttu-id="7d1dd-109">**New-AzWebApp** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="7d1dd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d1dd-110">EXAMPLES</span></span>

### <span data-ttu-id="7d1dd-111">Örnek 1: Web uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7d1dd-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="7d1dd-112">Bu komut, veri merkezi Batı 'da Default-Web-WestUS adlı var olan kaynak grubunda ContosoSite adlı bir Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="7d1dd-113">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="7d1dd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d1dd-114">PARAMETERS</span></span>

### <span data-ttu-id="7d1dd-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7d1dd-115">-AppServicePlan</span></span>
<span data-ttu-id="7d1dd-116">App Service planlama adı veya App Service planlama kimliği. WebApp ve App hizmet planı farklı kaynak gruplarınızda, ad yerine KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="7d1dd-117">App Service planlama kimliği,: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. id kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="7d1dd-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="7d1dd-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="7d1dd-119">Uygulama ayarları HashTable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="7d1dd-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="7d1dd-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="7d1dd-120">-AseName</span></span>
<span data-ttu-id="7d1dd-121">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="7d1dd-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="7d1dd-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1dd-122">-AseResourceGroupName</span></span>
<span data-ttu-id="7d1dd-123">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7d1dd-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="7d1dd-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="7d1dd-124">-AsJob</span></span>
<span data-ttu-id="7d1dd-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7d1dd-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d1dd-126">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="7d1dd-126">-ContainerImageName</span></span>
<span data-ttu-id="7d1dd-127">Kapsayıcı görüntü adı ve isteğe bağlı etiketi (Image: Tag)</span><span class="sxs-lookup"><span data-stu-id="7d1dd-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="7d1dd-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="7d1dd-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="7d1dd-129">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="7d1dd-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="7d1dd-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="7d1dd-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="7d1dd-131">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="7d1dd-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="7d1dd-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="7d1dd-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="7d1dd-133">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="7d1dd-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="7d1dd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1dd-134">-DefaultProfile</span></span>
<span data-ttu-id="7d1dd-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d1dd-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="7d1dd-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="7d1dd-137">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="7d1dd-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="7d1dd-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="7d1dd-138">-GitRepositoryPath</span></span>
<span data-ttu-id="7d1dd-139">Dağıtılacak Web uygulamasını içeren GitHub deposunun yolu.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="7d1dd-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="7d1dd-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="7d1dd-141">Özel ana bilgisayar adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="7d1dd-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="7d1dd-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="7d1dd-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="7d1dd-143">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="7d1dd-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="7d1dd-144">-Includesourcewebappyuvaları</span><span class="sxs-lookup"><span data-stu-id="7d1dd-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="7d1dd-145">Kaynak WebApp yuvalarını ekleme seçeneği</span><span class="sxs-lookup"><span data-stu-id="7d1dd-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="7d1dd-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="7d1dd-146">-Location</span></span>
<span data-ttu-id="7d1dd-147">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="7d1dd-147">Location</span></span>

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

### <span data-ttu-id="7d1dd-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d1dd-148">-Name</span></span>
<span data-ttu-id="7d1dd-149">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="7d1dd-149">WebApp Name</span></span>

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

### <span data-ttu-id="7d1dd-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1dd-150">-ResourceGroupName</span></span>
<span data-ttu-id="7d1dd-151">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7d1dd-151">Resource Group Name</span></span>

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

### <span data-ttu-id="7d1dd-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1dd-152">-SourceWebApp</span></span>
<span data-ttu-id="7d1dd-153">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="7d1dd-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="7d1dd-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d1dd-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="7d1dd-155">Var olan Traffic Manager profilinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7d1dd-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="7d1dd-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="7d1dd-156">-Confirm</span></span>
<span data-ttu-id="7d1dd-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1dd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1dd-158">-WhatIf</span></span>
<span data-ttu-id="7d1dd-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d1dd-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1dd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1dd-161">CommonParameters</span></span>
<span data-ttu-id="7d1dd-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d1dd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1dd-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1dd-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1dd-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d1dd-164">INPUTS</span></span>

### <span data-ttu-id="7d1dd-165">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="7d1dd-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7d1dd-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d1dd-166">OUTPUTS</span></span>

### <span data-ttu-id="7d1dd-167">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="7d1dd-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7d1dd-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d1dd-168">NOTES</span></span>

## <span data-ttu-id="7d1dd-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d1dd-169">RELATED LINKS</span></span>

[<span data-ttu-id="7d1dd-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1dd-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="7d1dd-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1dd-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="7d1dd-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1dd-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="7d1dd-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1dd-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="7d1dd-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1dd-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


