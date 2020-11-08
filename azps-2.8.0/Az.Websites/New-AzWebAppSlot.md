---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 6ca4eeba17af918ec73f0fe108b4179ea6513e2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934432"
---
# <span data-ttu-id="447c5-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="447c5-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="447c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="447c5-102">SYNOPSIS</span></span>
<span data-ttu-id="447c5-103">Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="447c5-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="447c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="447c5-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="447c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="447c5-105">DESCRIPTION</span></span>
<span data-ttu-id="447c5-106">**Yeni-AzWebAppSlot** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="447c5-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="447c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="447c5-107">EXAMPLES</span></span>

### <span data-ttu-id="447c5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="447c5-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="447c5-109">Bu komut, veri merkezi Batı 'da varsayılan-Web-WestUS adlı var olan kaynak grubundaki Contosositesinin mevcut Web App adları altında Slot001 adlı bir yuva oluşturur.</span><span class="sxs-lookup"><span data-stu-id="447c5-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="447c5-110">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="447c5-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="447c5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="447c5-111">PARAMETERS</span></span>

### <span data-ttu-id="447c5-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="447c5-112">-AppServicePlan</span></span>
<span data-ttu-id="447c5-113">App Service planlama adı veya App Service planlama kimliği. Yuva ve uygulama hizmeti planı farklı kaynak gruplarınızda, ad yerine KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="447c5-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="447c5-114">App Service planlama kimliği,: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. id kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="447c5-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="447c5-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="447c5-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="447c5-116">Uygulama ayarları Hashtable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="447c5-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="447c5-117">-AseName</span></span>
<span data-ttu-id="447c5-118">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="447c5-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447c5-119">-AseResourceGroupName</span></span>
<span data-ttu-id="447c5-120">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="447c5-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="447c5-121">-AsJob</span></span>
<span data-ttu-id="447c5-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="447c5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="447c5-123">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="447c5-123">-ContainerImageName</span></span>
<span data-ttu-id="447c5-124">Kapsayıcı görüntü adı ve isteğe bağlı etiketi (Image: Tag)</span><span class="sxs-lookup"><span data-stu-id="447c5-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="447c5-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="447c5-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="447c5-126">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="447c5-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="447c5-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="447c5-128">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="447c5-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="447c5-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="447c5-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="447c5-130">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="447c5-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="447c5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447c5-131">-DefaultProfile</span></span>
<span data-ttu-id="447c5-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="447c5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="447c5-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="447c5-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="447c5-134">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="447c5-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="447c5-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="447c5-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="447c5-136">Özel konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="447c5-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="447c5-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="447c5-138">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="447c5-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="447c5-139">-Name</span></span>
<span data-ttu-id="447c5-140">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="447c5-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447c5-141">-ResourceGroupName</span></span>
<span data-ttu-id="447c5-142">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="447c5-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-143">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="447c5-143">-Slot</span></span>
<span data-ttu-id="447c5-144">WEBAPP yuva adı</span><span class="sxs-lookup"><span data-stu-id="447c5-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="447c5-145">-SourceWebApp</span></span>
<span data-ttu-id="447c5-146">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="447c5-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="447c5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447c5-147">CommonParameters</span></span>
<span data-ttu-id="447c5-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="447c5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447c5-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447c5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447c5-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="447c5-150">INPUTS</span></span>

### <span data-ttu-id="447c5-151">System. String</span><span class="sxs-lookup"><span data-stu-id="447c5-151">System.String</span></span>

### <span data-ttu-id="447c5-152">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="447c5-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="447c5-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="447c5-153">OUTPUTS</span></span>

### <span data-ttu-id="447c5-154">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="447c5-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="447c5-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="447c5-155">NOTES</span></span>

## <span data-ttu-id="447c5-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="447c5-156">RELATED LINKS</span></span>

[<span data-ttu-id="447c5-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="447c5-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="447c5-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="447c5-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="447c5-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="447c5-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="447c5-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="447c5-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="447c5-161">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="447c5-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="447c5-162">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="447c5-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="447c5-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="447c5-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="447c5-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="447c5-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)