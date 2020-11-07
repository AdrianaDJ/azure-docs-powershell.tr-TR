---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753803"
---
# <span data-ttu-id="6635c-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6635c-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="6635c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6635c-102">SYNOPSIS</span></span>
<span data-ttu-id="6635c-103">Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6635c-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="6635c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6635c-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6635c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6635c-105">DESCRIPTION</span></span>
<span data-ttu-id="6635c-106">**Yeni-AzWebAppSlot** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6635c-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="6635c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6635c-107">EXAMPLES</span></span>

### <span data-ttu-id="6635c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6635c-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="6635c-109">Bu komut, veri merkezi Batı 'da varsayılan-Web-WestUS adlı var olan kaynak grubundaki Contosositesinin mevcut Web App adları altında Slot001 adlı bir yuva oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6635c-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="6635c-110">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="6635c-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="6635c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6635c-111">PARAMETERS</span></span>

### <span data-ttu-id="6635c-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6635c-112">-AppServicePlan</span></span>
<span data-ttu-id="6635c-113">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="6635c-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="6635c-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="6635c-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="6635c-115">Uygulama ayarları Hashtable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="6635c-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="6635c-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="6635c-116">-AseName</span></span>
<span data-ttu-id="6635c-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="6635c-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="6635c-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6635c-118">-AseResourceGroupName</span></span>
<span data-ttu-id="6635c-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6635c-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="6635c-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="6635c-120">-AsJob</span></span>
<span data-ttu-id="6635c-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6635c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6635c-122">-Containergörüntüadı</span><span class="sxs-lookup"><span data-stu-id="6635c-122">-ContainerImageName</span></span>
<span data-ttu-id="6635c-123">Kapsayıcı görüntü adı ve isteğe bağlı etiketi (Image: Tag)</span><span class="sxs-lookup"><span data-stu-id="6635c-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="6635c-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="6635c-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="6635c-125">Özel kapsayıcı kayıt defteri parolası</span><span class="sxs-lookup"><span data-stu-id="6635c-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="6635c-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="6635c-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="6635c-127">Özel kapsayıcı kayıt defteri sunucusu URL 'Si</span><span class="sxs-lookup"><span data-stu-id="6635c-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="6635c-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="6635c-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="6635c-129">Özel kapsayıcı kayıt defteri Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="6635c-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="6635c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6635c-130">-DefaultProfile</span></span>
<span data-ttu-id="6635c-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6635c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6635c-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="6635c-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="6635c-133">Kapsayıcıyı sürekli dağıtma Web kancasını ve devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="6635c-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="6635c-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="6635c-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="6635c-135">Özel konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="6635c-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="6635c-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="6635c-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="6635c-137">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="6635c-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="6635c-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="6635c-138">-Name</span></span>
<span data-ttu-id="6635c-139">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="6635c-139">Webapp Name</span></span>

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

### <span data-ttu-id="6635c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6635c-140">-ResourceGroupName</span></span>
<span data-ttu-id="6635c-141">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6635c-141">Resource Group Name</span></span>

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

### <span data-ttu-id="6635c-142">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="6635c-142">-Slot</span></span>
<span data-ttu-id="6635c-143">WEBAPP yuva adı</span><span class="sxs-lookup"><span data-stu-id="6635c-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="6635c-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="6635c-144">-SourceWebApp</span></span>
<span data-ttu-id="6635c-145">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="6635c-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="6635c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6635c-146">CommonParameters</span></span>
<span data-ttu-id="6635c-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6635c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6635c-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6635c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6635c-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6635c-149">INPUTS</span></span>

### <span data-ttu-id="6635c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6635c-150">System.String</span></span>

### <span data-ttu-id="6635c-151">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="6635c-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6635c-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6635c-152">OUTPUTS</span></span>

### <span data-ttu-id="6635c-153">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="6635c-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6635c-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6635c-154">NOTES</span></span>

## <span data-ttu-id="6635c-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6635c-155">RELATED LINKS</span></span>

[<span data-ttu-id="6635c-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6635c-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="6635c-157">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6635c-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="6635c-158">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6635c-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="6635c-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6635c-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="6635c-160">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6635c-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="6635c-161">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6635c-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="6635c-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6635c-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="6635c-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6635c-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
