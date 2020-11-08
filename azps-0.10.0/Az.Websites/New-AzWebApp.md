---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: ec5f9cf60025e6b35248b2e7f8058040b404ec42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936100"
---
# <span data-ttu-id="d25b1-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d25b1-101">New-AzWebApp</span></span>

## <span data-ttu-id="d25b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d25b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d25b1-103">Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d25b1-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="d25b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d25b1-104">SYNTAX</span></span>

### <span data-ttu-id="d25b1-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d25b1-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25b1-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="d25b1-106">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d25b1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d25b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d25b1-108">**New-AzWebApp** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d25b1-108">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="d25b1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d25b1-109">EXAMPLES</span></span>

### <span data-ttu-id="d25b1-110">Örnek 1: Web uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d25b1-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="d25b1-111">Bu komut, veri merkezi Batı 'da Default-Web-WestUS adlı var olan kaynak grubunda ContosoSite adlı bir Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d25b1-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="d25b1-112">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="d25b1-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="d25b1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d25b1-113">PARAMETERS</span></span>

### <span data-ttu-id="d25b1-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d25b1-114">-AppServicePlan</span></span>
<span data-ttu-id="d25b1-115">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="d25b1-115">App Service Plan Name</span></span>

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

### <span data-ttu-id="d25b1-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="d25b1-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="d25b1-117">Uygulama ayarları HashTable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="d25b1-117">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="d25b1-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="d25b1-118">-AseName</span></span>
<span data-ttu-id="d25b1-119">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="d25b1-119">App Service Environment Name</span></span>

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

### <span data-ttu-id="d25b1-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25b1-120">-AseResourceGroupName</span></span>
<span data-ttu-id="d25b1-121">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d25b1-121">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="d25b1-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="d25b1-122">-AsJob</span></span>
<span data-ttu-id="d25b1-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d25b1-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d25b1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25b1-124">-DefaultProfile</span></span>
<span data-ttu-id="d25b1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d25b1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25b1-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="d25b1-126">-GitRepositoryPath</span></span>
<span data-ttu-id="d25b1-127">Web uygulamasına dağıtılacak GitHub deposunun yolu.</span><span class="sxs-lookup"><span data-stu-id="d25b1-127">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="d25b1-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="d25b1-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="d25b1-129">Özel ana bilgisayar adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="d25b1-129">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="d25b1-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="d25b1-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="d25b1-131">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="d25b1-131">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="d25b1-132">-Includesourcewebappyuvaları</span><span class="sxs-lookup"><span data-stu-id="d25b1-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="d25b1-133">Kaynak WebApp yuvalarını ekleme seçeneği</span><span class="sxs-lookup"><span data-stu-id="d25b1-133">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="d25b1-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="d25b1-134">-Location</span></span>
<span data-ttu-id="d25b1-135">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="d25b1-135">Location</span></span>

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

### <span data-ttu-id="d25b1-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="d25b1-136">-Name</span></span>
<span data-ttu-id="d25b1-137">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d25b1-137">WebApp Name</span></span>

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

### <span data-ttu-id="d25b1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25b1-138">-ResourceGroupName</span></span>
<span data-ttu-id="d25b1-139">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d25b1-139">Resource Group Name</span></span>

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

### <span data-ttu-id="d25b1-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="d25b1-140">-SourceWebApp</span></span>
<span data-ttu-id="d25b1-141">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="d25b1-141">Source WebApp Object</span></span>

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

### <span data-ttu-id="d25b1-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d25b1-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="d25b1-143">Var olan Traffic Manager profilinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d25b1-143">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="d25b1-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="d25b1-144">-Confirm</span></span>
<span data-ttu-id="d25b1-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d25b1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d25b1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25b1-146">-WhatIf</span></span>
<span data-ttu-id="d25b1-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d25b1-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d25b1-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d25b1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d25b1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25b1-149">CommonParameters</span></span>
<span data-ttu-id="d25b1-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d25b1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25b1-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d25b1-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25b1-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d25b1-152">INPUTS</span></span>

### <span data-ttu-id="d25b1-153">Bölge</span><span class="sxs-lookup"><span data-stu-id="d25b1-153">Site</span></span>
<span data-ttu-id="d25b1-154">' SourceWebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d25b1-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d25b1-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d25b1-155">OUTPUTS</span></span>

### <span data-ttu-id="d25b1-156">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="d25b1-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="d25b1-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d25b1-157">NOTES</span></span>

## <span data-ttu-id="d25b1-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d25b1-158">RELATED LINKS</span></span>

[<span data-ttu-id="d25b1-159">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d25b1-159">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d25b1-160">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d25b1-160">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d25b1-161">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d25b1-161">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d25b1-162">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d25b1-162">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d25b1-163">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d25b1-163">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

