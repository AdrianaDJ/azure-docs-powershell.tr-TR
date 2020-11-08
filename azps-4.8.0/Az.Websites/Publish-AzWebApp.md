---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109315"
---
# <span data-ttu-id="9bf3c-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9bf3c-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="9bf3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf3c-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf3c-103">Zipdeploy kullanarak bir ZIP, JAR veya WAR dosyasından Azure Web uygulaması dağıtır.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="9bf3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bf3c-104">SYNTAX</span></span>

### <span data-ttu-id="9bf3c-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9bf3c-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf3c-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9bf3c-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="9bf3c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bf3c-107">DESCRIPTION</span></span>
<span data-ttu-id="9bf3c-108">**Publish-AzWebApp** cmdlet 'i mevcut bir Azure Web uygulamasına içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="9bf3c-109">.NET, Python veya düğüm gibi yığınları kullanıyorsanız veya Java kullanıyorsanız, bir ZIP dosyasında içerik paketlenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="9bf3c-110">Dağıtım sırasında ek derleme adımları yapılmadan içeriğin önceden oluşturulması ve kullanıma hazır olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="9bf3c-111">Bu cmdlet, içeriği dağıtmak için kudu zipdeploy ve wardeploy özelliklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="9bf3c-112">Bir e-posta ile çalışmanın nasıl dağıtılacağı ve bir Web uygulamasının dağıtım için uygun şekilde paketlendirileceklerini öğrenmek için kudu wiki 'ye başvurun.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="9bf3c-113"> https://aka.ms/kuduzipdeploy ve https://aka.ms/kuduwardeploy zipdeploy ve wardeploy hakkında yararlı ayrıntılar içerir.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="9bf3c-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bf3c-114">EXAMPLES</span></span>

### <span data-ttu-id="9bf3c-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9bf3c-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="9bf3c-116">app.zip içeriğini, varsayılan-Web-WestUS kaynak grubuna ait Uygulamam adlı Web uygulamasına yükler.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="9bf3c-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9bf3c-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="9bf3c-118">Javaproject. war içeriğini, kaynak grubuna ait olan ContosoApp adındaki Web uygulamasının hazırlama yuvasına yükler.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="9bf3c-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9bf3c-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="9bf3c-120">app.zip içeriğini, ContosoRG kaynak grubuna ait olan ContosoApp adındaki Web uygulamasına yükler.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="9bf3c-121">Cmdlet, bir arka plan işinde çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="9bf3c-122">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="9bf3c-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="9bf3c-123">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="9bf3c-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="9bf3c-124">Java_app. jar içeriğini, ContosoRG kaynak grubuna ait olan ContosoApp adlı Web uygulamasına yükler.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="9bf3c-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bf3c-125">PARAMETERS</span></span>

### <span data-ttu-id="9bf3c-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="9bf3c-126">-ArchivePath</span></span>
<span data-ttu-id="9bf3c-127">Arşiv dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-127">The path of the archive file.</span></span> <span data-ttu-id="9bf3c-128">ZIP, WAR ve JAR destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-128">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf3c-129">-Iş</span><span class="sxs-lookup"><span data-stu-id="9bf3c-129">-AsJob</span></span>
<span data-ttu-id="9bf3c-130">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9bf3c-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf3c-131">-Force</span><span class="sxs-lookup"><span data-stu-id="9bf3c-131">-Force</span></span>
<span data-ttu-id="9bf3c-132">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="9bf3c-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="9bf3c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf3c-133">-DefaultProfile</span></span>
<span data-ttu-id="9bf3c-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf3c-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bf3c-135">-Name</span></span>
<span data-ttu-id="9bf3c-136">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-136">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf3c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf3c-137">-ResourceGroupName</span></span>
<span data-ttu-id="9bf3c-138">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf3c-139">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="9bf3c-139">-Slot</span></span>
<span data-ttu-id="9bf3c-140">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-140">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf3c-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9bf3c-141">-WebApp</span></span>
<span data-ttu-id="9bf3c-142">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="9bf3c-142">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf3c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf3c-143">CommonParameters</span></span>
<span data-ttu-id="9bf3c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bf3c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf3c-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf3c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf3c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bf3c-146">INPUTS</span></span>

### <span data-ttu-id="9bf3c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf3c-147">System.String</span></span>

### <span data-ttu-id="9bf3c-148">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="9bf3c-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9bf3c-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bf3c-149">OUTPUTS</span></span>

### <span data-ttu-id="9bf3c-150">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="9bf3c-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9bf3c-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bf3c-151">NOTES</span></span>

## <span data-ttu-id="9bf3c-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bf3c-152">RELATED LINKS</span></span>
