---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105877"
---
# <span data-ttu-id="1b601-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="1b601-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="1b601-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b601-102">SYNOPSIS</span></span>
<span data-ttu-id="1b601-103">Visual Studio Web projesini WebDeploy kullanarak bir Microsoft Azure Web sitesinde yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1b601-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="1b601-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b601-104">SYNTAX</span></span>

### <span data-ttu-id="1b601-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1b601-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b601-106">Paketini</span><span class="sxs-lookup"><span data-stu-id="1b601-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1b601-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b601-107">DESCRIPTION</span></span>
<span data-ttu-id="1b601-108">Visual Studio Web projesini WebDeploy kullanarak bir Microsoft Azure Web sitesinde yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1b601-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="1b601-109">Bir WebDeploy paketi alabilir ve doğrudan yayımlayabilir ya da Visual Studio Web projesi alabilir, projeyi oluşturabilir ve yayımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b601-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="1b601-110">Ayrıca, yayımlama sırasında Web.config bağlantı dizelerini de değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1b601-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="1b601-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b601-111">EXAMPLES</span></span>

### <span data-ttu-id="1b601-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b601-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="1b601-113">"Debug" yapılandırması (yani Web.Debug.config) ile bir Visual Studio Web projesi geliştirin ve WebDeploy kullanarak bir Microsoft Azure Web sitesinde yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1b601-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1b601-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1b601-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="1b601-115">WebDeploy Package. zip dosyasını, WebDeploy kullanarak bir Microsoft Azure Web sitesine yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1b601-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1b601-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1b601-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="1b601-117">WebDeploy paketi klasörünü WebDeploy kullanarak Microsoft Azure Web sitesine yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1b601-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1b601-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="1b601-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="1b601-119">Visual Studio Web projesi oluşturma, Web.config 'da "DefaultConnection" bağlantı dizesinin üzerine yazın ve WebDeploy kullanarak bir Microsoft Azure Web sitesine yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1b601-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1b601-120">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="1b601-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="1b601-121">Visual Studio Web projesi oluşturma, Web.config 'da "DefaultConnection" bağlantı dizesinin üzerine yazın ve WebDeploy kullanarak bir Microsoft Azure Web sitesine yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1b601-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="1b601-122">-DefaultConnection 'ın Web.config ayrıştırarak eklediği dinamik bir parametre olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="1b601-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="1b601-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b601-123">PARAMETERS</span></span>

### <span data-ttu-id="1b601-124">-Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1b601-124">-Configuration</span></span>
<span data-ttu-id="1b601-125">Visual Studio Web uygulaması projesini oluşturmak için kullanılan yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="1b601-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1b601-126">-ConnectionString</span></span>
<span data-ttu-id="1b601-127">Dağıtım için kullanılacak bağlantı dizeleri.</span><span class="sxs-lookup"><span data-stu-id="1b601-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="1b601-128">-DoNotDelete</span></span>
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

### <span data-ttu-id="1b601-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b601-129">-Name</span></span>
<span data-ttu-id="1b601-130">Web sitesi adı.</span><span class="sxs-lookup"><span data-stu-id="1b601-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-131">-Package</span><span class="sxs-lookup"><span data-stu-id="1b601-131">-Package</span></span>
<span data-ttu-id="1b601-132">Yayımlanacak Visual Studio Web uygulaması projesinin zip dosyasının WebDeploy Package klasörü.</span><span class="sxs-lookup"><span data-stu-id="1b601-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="1b601-133">-Profile</span></span>
<span data-ttu-id="1b601-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b601-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b601-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1b601-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1b601-136">-ProjectFile</span></span>
<span data-ttu-id="1b601-137">Yayımlanacak Visual Studio Web uygulaması projesi.</span><span class="sxs-lookup"><span data-stu-id="1b601-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="1b601-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="1b601-139">-SkipAppData</span></span>
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

### <span data-ttu-id="1b601-140">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="1b601-140">-Slot</span></span>
<span data-ttu-id="1b601-141">Web sitesi yuva adı.</span><span class="sxs-lookup"><span data-stu-id="1b601-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-142">-Belirteçler</span><span class="sxs-lookup"><span data-stu-id="1b601-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b601-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b601-143">CommonParameters</span></span>
<span data-ttu-id="1b601-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b601-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b601-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b601-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b601-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b601-146">INPUTS</span></span>

## <span data-ttu-id="1b601-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b601-147">OUTPUTS</span></span>

## <span data-ttu-id="1b601-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b601-148">NOTES</span></span>

## <span data-ttu-id="1b601-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b601-149">RELATED LINKS</span></span>

[<span data-ttu-id="1b601-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1b601-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="1b601-151">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1b601-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1b601-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1b601-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1b601-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1b601-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


