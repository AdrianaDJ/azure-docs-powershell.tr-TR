---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753802"
---
# <span data-ttu-id="39a65-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="39a65-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="39a65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39a65-102">SYNOPSIS</span></span>
<span data-ttu-id="39a65-103">Zipdeploy kullanarak bir ZIP, JAR veya WAR dosyasından Azure Web uygulaması dağıtır.</span><span class="sxs-lookup"><span data-stu-id="39a65-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="39a65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39a65-104">SYNTAX</span></span>

### <span data-ttu-id="39a65-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="39a65-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39a65-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="39a65-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39a65-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="39a65-107">DESCRIPTION</span></span>
<span data-ttu-id="39a65-108">**Publish-AzWebApp** cmdlet 'i mevcut bir Azure Web uygulamasına içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="39a65-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="39a65-109">.NET, Python veya düğüm gibi yığınları kullanıyorsanız veya Java kullanıyorsanız, bir ZIP dosyasında içerik paketlenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="39a65-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="39a65-110">Dağıtım sırasında ek derleme adımları yapılmadan içeriğin önceden oluşturulması ve kullanıma hazır olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="39a65-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="39a65-111">Bu cmdlet, içeriği dağıtmak için kudu zipdeploy ve wardeploy özelliklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="39a65-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="39a65-112">Bir e-posta ile çalışmanın nasıl dağıtılacağı ve bir Web uygulamasının dağıtım için uygun şekilde paketlendirileceklerini öğrenmek için kudu wiki 'ye başvurun.</span><span class="sxs-lookup"><span data-stu-id="39a65-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="39a65-113"> https://aka.ms/kuduzipdeploy ve https://aka.ms/kuduwardeploy zipdeploy ve wardeploy hakkında yararlı ayrıntılar içerir.</span><span class="sxs-lookup"><span data-stu-id="39a65-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="39a65-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39a65-114">EXAMPLES</span></span>

### <span data-ttu-id="39a65-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="39a65-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="39a65-116">app.zip içeriğini, varsayılan-Web-WestUS kaynak grubuna ait Uygulamam adlı Web uygulamasına yükler.</span><span class="sxs-lookup"><span data-stu-id="39a65-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="39a65-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="39a65-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="39a65-118">Javaproject. war içeriğini, kaynak grubuna ait olan ContosoApp adındaki Web uygulamasının hazırlama yuvasına yükler.</span><span class="sxs-lookup"><span data-stu-id="39a65-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="39a65-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="39a65-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="39a65-120">app.zip içeriğini, ContosoRG kaynak grubuna ait olan ContosoApp adındaki Web uygulamasına yükler.</span><span class="sxs-lookup"><span data-stu-id="39a65-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="39a65-121">Cmdlet, bir arka plan işinde çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="39a65-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="39a65-122">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="39a65-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="39a65-123">Java_app. jar içeriğini, ContosoRG kaynak grubuna ait olan ContosoApp adlı Web uygulamasına yükler.</span><span class="sxs-lookup"><span data-stu-id="39a65-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="39a65-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39a65-124">PARAMETERS</span></span>

### <span data-ttu-id="39a65-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="39a65-125">-ArchivePath</span></span>
<span data-ttu-id="39a65-126">Arşiv dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="39a65-126">The path of the archive file.</span></span> <span data-ttu-id="39a65-127">ZIP, WAR ve JAR destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="39a65-127">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="39a65-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="39a65-128">-AsJob</span></span>
<span data-ttu-id="39a65-129">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="39a65-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39a65-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a65-130">-DefaultProfile</span></span>
<span data-ttu-id="39a65-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39a65-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a65-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="39a65-132">-Name</span></span>
<span data-ttu-id="39a65-133">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="39a65-133">The name of the web app.</span></span>

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

### <span data-ttu-id="39a65-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a65-134">-ResourceGroupName</span></span>
<span data-ttu-id="39a65-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="39a65-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="39a65-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="39a65-136">-Slot</span></span>
<span data-ttu-id="39a65-137">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="39a65-137">The name of the web app slot.</span></span>

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

### <span data-ttu-id="39a65-138">-WebApp</span><span class="sxs-lookup"><span data-stu-id="39a65-138">-WebApp</span></span>
<span data-ttu-id="39a65-139">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="39a65-139">The web app object</span></span>

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

### <span data-ttu-id="39a65-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a65-140">CommonParameters</span></span>
<span data-ttu-id="39a65-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39a65-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a65-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39a65-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a65-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39a65-143">INPUTS</span></span>

### <span data-ttu-id="39a65-144">System. String</span><span class="sxs-lookup"><span data-stu-id="39a65-144">System.String</span></span>

### <span data-ttu-id="39a65-145">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="39a65-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="39a65-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39a65-146">OUTPUTS</span></span>

### <span data-ttu-id="39a65-147">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="39a65-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="39a65-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39a65-148">NOTES</span></span>

## <span data-ttu-id="39a65-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39a65-149">RELATED LINKS</span></span>
