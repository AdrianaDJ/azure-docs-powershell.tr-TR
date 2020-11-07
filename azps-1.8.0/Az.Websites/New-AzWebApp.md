---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 8120b22f02d137ff261b1b4e345b917d6ae82a5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753820"
---
# <span data-ttu-id="efd7e-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="efd7e-101">New-AzWebApp</span></span>

## <span data-ttu-id="efd7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd7e-102">SYNOPSIS</span></span>
<span data-ttu-id="efd7e-103">Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="efd7e-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="efd7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efd7e-104">SYNTAX</span></span>

### <span data-ttu-id="efd7e-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efd7e-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efd7e-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="efd7e-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd7e-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="efd7e-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd7e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="efd7e-108">DESCRIPTION</span></span>
<span data-ttu-id="efd7e-109">**New-AzWebApp** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App oluşturur.</span><span class="sxs-lookup"><span data-stu-id="efd7e-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="efd7e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efd7e-110">EXAMPLES</span></span>

### <span data-ttu-id="efd7e-111">Örnek 1: Web uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="efd7e-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="efd7e-112">Bu komut, veri merkezi Batı 'da Default-Web-WestUS adlı var olan kaynak grubunda ContosoSite adlı bir Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="efd7e-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="efd7e-113">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="efd7e-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="efd7e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efd7e-114">PARAMETERS</span></span>

### <span data-ttu-id="efd7e-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="efd7e-115">-AppServicePlan</span></span>
<span data-ttu-id="efd7e-116">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="efd7e-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="efd7e-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="efd7e-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="efd7e-118">Uygulama ayarları HashTable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="efd7e-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="efd7e-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="efd7e-119">-AseName</span></span>
<span data-ttu-id="efd7e-120">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="efd7e-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="efd7e-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd7e-121">-AseResourceGroupName</span></span>
<span data-ttu-id="efd7e-122">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="efd7e-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="efd7e-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="efd7e-123">-AsJob</span></span>
<span data-ttu-id="efd7e-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="efd7e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efd7e-125">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="efd7e-125">-ContainerImageName</span></span>
<span data-ttu-id="efd7e-126">Kapsayıcı görüntü adı ve isteğe bağlı etiketi (Image: Tag)</span><span class="sxs-lookup"><span data-stu-id="efd7e-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="efd7e-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="efd7e-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="efd7e-128">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="efd7e-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="efd7e-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="efd7e-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="efd7e-130">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="efd7e-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="efd7e-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="efd7e-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="efd7e-132">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="efd7e-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="efd7e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd7e-133">-DefaultProfile</span></span>
<span data-ttu-id="efd7e-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="efd7e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efd7e-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="efd7e-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="efd7e-136">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="efd7e-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="efd7e-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="efd7e-137">-GitRepositoryPath</span></span>
<span data-ttu-id="efd7e-138">Dağıtılacak Web uygulamasını içeren GitHub deposunun yolu.</span><span class="sxs-lookup"><span data-stu-id="efd7e-138">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="efd7e-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="efd7e-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="efd7e-140">Özel ana bilgisayar adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="efd7e-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="efd7e-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="efd7e-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="efd7e-142">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="efd7e-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="efd7e-143">-Includesourcewebappyuvaları</span><span class="sxs-lookup"><span data-stu-id="efd7e-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="efd7e-144">Kaynak WebApp yuvalarını ekleme seçeneği</span><span class="sxs-lookup"><span data-stu-id="efd7e-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="efd7e-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="efd7e-145">-Location</span></span>
<span data-ttu-id="efd7e-146">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="efd7e-146">Location</span></span>

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

### <span data-ttu-id="efd7e-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="efd7e-147">-Name</span></span>
<span data-ttu-id="efd7e-148">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="efd7e-148">WebApp Name</span></span>

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

### <span data-ttu-id="efd7e-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd7e-149">-ResourceGroupName</span></span>
<span data-ttu-id="efd7e-150">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="efd7e-150">Resource Group Name</span></span>

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

### <span data-ttu-id="efd7e-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="efd7e-151">-SourceWebApp</span></span>
<span data-ttu-id="efd7e-152">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="efd7e-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="efd7e-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="efd7e-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="efd7e-154">Var olan Traffic Manager profilinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="efd7e-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="efd7e-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="efd7e-155">-Confirm</span></span>
<span data-ttu-id="efd7e-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="efd7e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd7e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd7e-157">-WhatIf</span></span>
<span data-ttu-id="efd7e-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="efd7e-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efd7e-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="efd7e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd7e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd7e-160">CommonParameters</span></span>
<span data-ttu-id="efd7e-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efd7e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd7e-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efd7e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd7e-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efd7e-163">INPUTS</span></span>

### <span data-ttu-id="efd7e-164">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="efd7e-164">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="efd7e-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efd7e-165">OUTPUTS</span></span>

### <span data-ttu-id="efd7e-166">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="efd7e-166">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="efd7e-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efd7e-167">NOTES</span></span>

## <span data-ttu-id="efd7e-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efd7e-168">RELATED LINKS</span></span>

[<span data-ttu-id="efd7e-169">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="efd7e-169">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="efd7e-170">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="efd7e-170">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="efd7e-171">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="efd7e-171">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="efd7e-172">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="efd7e-172">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="efd7e-173">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="efd7e-173">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


