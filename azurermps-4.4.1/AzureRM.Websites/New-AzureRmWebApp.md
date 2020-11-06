---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594542"
---
# <span data-ttu-id="8a701-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8a701-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="8a701-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a701-102">SYNOPSIS</span></span>
<span data-ttu-id="8a701-103">Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a701-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a701-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a701-104">SYNTAX</span></span>

### <span data-ttu-id="8a701-105">S1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a701-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a701-106">S2</span><span class="sxs-lookup"><span data-stu-id="8a701-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a701-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a701-107">DESCRIPTION</span></span>
<span data-ttu-id="8a701-108">**Yeni-AzureRmWebApp** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan belirli bir kaynak grubunda Azure Web App oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a701-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="8a701-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a701-109">EXAMPLES</span></span>

### <span data-ttu-id="8a701-110">Örnek 1: Web uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a701-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="8a701-111">Bu komut, veri merkezi Batı 'da Default-Web-WestUS adlı var olan kaynak grubunda ContosoSite adlı bir Azure Web uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a701-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="8a701-112">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="8a701-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="8a701-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a701-113">PARAMETERS</span></span>

### <span data-ttu-id="8a701-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8a701-114">-AppServicePlan</span></span>
<span data-ttu-id="8a701-115">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="8a701-115">App Service Plan Name</span></span>

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

### <span data-ttu-id="8a701-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="8a701-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="8a701-117">Uygulama ayarları HashTable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="8a701-117">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="8a701-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="8a701-118">-AseName</span></span>
<span data-ttu-id="8a701-119">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="8a701-119">App Service Environment Name</span></span>

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

### <span data-ttu-id="8a701-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a701-120">-AseResourceGroupName</span></span>
<span data-ttu-id="8a701-121">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8a701-121">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="8a701-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="8a701-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="8a701-123">Özel ana bilgisayar adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="8a701-123">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="8a701-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="8a701-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="8a701-125">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="8a701-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="8a701-126">-Includesourcewebappyuvaları</span><span class="sxs-lookup"><span data-stu-id="8a701-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="8a701-127">Kaynak WebApp yuvalarını ekleme seçeneği</span><span class="sxs-lookup"><span data-stu-id="8a701-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="8a701-128">-Location</span></span>
<span data-ttu-id="8a701-129">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="8a701-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a701-130">-Name</span></span>
<span data-ttu-id="8a701-131">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8a701-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a701-132">-ResourceGroupName</span></span>
<span data-ttu-id="8a701-133">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8a701-133">Resource Group Name</span></span>

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

### <span data-ttu-id="8a701-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="8a701-134">-SourceWebApp</span></span>
<span data-ttu-id="8a701-135">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8a701-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="8a701-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="8a701-137">Traffic Manager profil kimliği</span><span class="sxs-lookup"><span data-stu-id="8a701-137">Traffic Manager Profile Id</span></span>

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

### <span data-ttu-id="8a701-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="8a701-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="8a701-139">Traffic Manager profil adı</span><span class="sxs-lookup"><span data-stu-id="8a701-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a701-140">-DefaultProfile</span></span>
<span data-ttu-id="8a701-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a701-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a701-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a701-142">CommonParameters</span></span>
<span data-ttu-id="8a701-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a701-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a701-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a701-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a701-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a701-145">INPUTS</span></span>

### <span data-ttu-id="8a701-146">Bölge</span><span class="sxs-lookup"><span data-stu-id="8a701-146">Site</span></span>
<span data-ttu-id="8a701-147">' SourceWebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8a701-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8a701-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a701-148">OUTPUTS</span></span>

## <span data-ttu-id="8a701-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a701-149">NOTES</span></span>

## <span data-ttu-id="8a701-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a701-150">RELATED LINKS</span></span>

[<span data-ttu-id="8a701-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8a701-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="8a701-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8a701-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="8a701-153">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8a701-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="8a701-154">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8a701-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="8a701-155">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8a701-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


