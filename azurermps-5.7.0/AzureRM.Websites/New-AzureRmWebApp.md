---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 05ee02fcb1a1f03c2a9b349754009a178a1668b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592367"
---
# <span data-ttu-id="73374-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="73374-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="73374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73374-102">SYNOPSIS</span></span>
<span data-ttu-id="73374-103">Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73374-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73374-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73374-104">SYNTAX</span></span>

### <span data-ttu-id="73374-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73374-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73374-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="73374-106">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73374-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="73374-107">DESCRIPTION</span></span>
<span data-ttu-id="73374-108">**Yeni-AzureRmWebApp** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan belirli bir kaynak grubunda Azure Web App oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73374-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="73374-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73374-109">EXAMPLES</span></span>

### <span data-ttu-id="73374-110">Örnek 1: Web uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="73374-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="73374-111">Bu komut, veri merkezi Batı 'da Default-Web-WestUS adlı var olan kaynak grubunda ContosoSite adlı bir Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73374-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="73374-112">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="73374-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="73374-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73374-113">PARAMETERS</span></span>

### <span data-ttu-id="73374-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="73374-114">-AppServicePlan</span></span>
<span data-ttu-id="73374-115">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="73374-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="73374-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="73374-117">Uygulama ayarları HashTable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="73374-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="73374-118">-AseName</span></span>
<span data-ttu-id="73374-119">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="73374-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73374-120">-AseResourceGroupName</span></span>
<span data-ttu-id="73374-121">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="73374-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="73374-122">-AsJob</span></span>
<span data-ttu-id="73374-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="73374-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73374-124">-DefaultProfile</span></span>
<span data-ttu-id="73374-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73374-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="73374-126">-GitRepositoryPath</span></span>
<span data-ttu-id="73374-127">Web uygulamasına dağıtılacak GitHub deposunun yolu.</span><span class="sxs-lookup"><span data-stu-id="73374-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="73374-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="73374-129">Özel ana bilgisayar adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="73374-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="73374-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="73374-131">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="73374-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-132">-Includesourcewebappyuvaları</span><span class="sxs-lookup"><span data-stu-id="73374-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="73374-133">Kaynak WebApp yuvalarını ekleme seçeneği</span><span class="sxs-lookup"><span data-stu-id="73374-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="73374-134">-Location</span></span>
<span data-ttu-id="73374-135">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="73374-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="73374-136">-Name</span></span>
<span data-ttu-id="73374-137">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="73374-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73374-138">-ResourceGroupName</span></span>
<span data-ttu-id="73374-139">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="73374-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="73374-140">-SourceWebApp</span></span>
<span data-ttu-id="73374-141">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="73374-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73374-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73374-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="73374-143">Var olan Traffic Manager profilinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="73374-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="73374-144">-Confirm</span></span>
<span data-ttu-id="73374-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73374-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73374-146">-WhatIf</span></span>
<span data-ttu-id="73374-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73374-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73374-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73374-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73374-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73374-149">CommonParameters</span></span>
<span data-ttu-id="73374-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73374-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73374-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73374-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73374-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73374-152">INPUTS</span></span>

### <span data-ttu-id="73374-153">Bölge</span><span class="sxs-lookup"><span data-stu-id="73374-153">Site</span></span>
<span data-ttu-id="73374-154">' SourceWebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="73374-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="73374-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73374-155">OUTPUTS</span></span>

### <span data-ttu-id="73374-156">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="73374-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="73374-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73374-157">NOTES</span></span>

## <span data-ttu-id="73374-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73374-158">RELATED LINKS</span></span>

[<span data-ttu-id="73374-159">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="73374-159">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="73374-160">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="73374-160">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="73374-161">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="73374-161">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="73374-162">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="73374-162">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="73374-163">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="73374-163">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


