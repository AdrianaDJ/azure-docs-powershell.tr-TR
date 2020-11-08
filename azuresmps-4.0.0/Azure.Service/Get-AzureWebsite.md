---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106274"
---
# <span data-ttu-id="2eac4-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2eac4-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="2eac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eac4-102">SYNOPSIS</span></span>
<span data-ttu-id="2eac4-103">Geçerli abonelikteki Azure Web sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="2eac4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2eac4-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2eac4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2eac4-105">DESCRIPTION</span></span>
<span data-ttu-id="2eac4-106">**Get-AzureWebsite** cmdlet 'i geçerli abonelikteki Azure Web siteleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="2eac4-107">Varsayılan olarak **Get-AzureWebsite** , geçerli abonelikteki tüm Azure Web sitelerini alır ve siteler hakkında temel bilgiler sağlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2eac4-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="2eac4-108">*Name* parametresini kullandığınızda **Get-AzureWebsite** , yapılandırma ayrıntıları dahil kapsamlı bir bilgi içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2eac4-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="2eac4-109">Geçerli abonelik, "geçerli" olarak atanan aboneliğiniz.</span><span class="sxs-lookup"><span data-stu-id="2eac4-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="2eac4-110">Geçerli aboneliği bulmak için [Get-Azuyeniden gönderme scripscripts](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet 'inin *Current* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2eac4-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="2eac4-111">Geçerli aboneliği değiştirmek için, [Select-azuyeniden komut](https://go.microsoft.com/fwlink/?LinkID=397628) dosyası cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2eac4-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="2eac4-112">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2eac4-113">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2eac4-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="2eac4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2eac4-114">EXAMPLES</span></span>

### <span data-ttu-id="2eac4-115">Örnek 1: abonelikteki tüm Web sitelerini alma</span><span class="sxs-lookup"><span data-stu-id="2eac4-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="2eac4-116">Bu komut geçerli abonelikteki tüm Azure Web sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="2eac4-117">Örnek 2: ada göre bir Web sitesi alma</span><span class="sxs-lookup"><span data-stu-id="2eac4-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="2eac4-118">Bu komut, yapılandırma bilgileri de içinde olmak üzere ContosoWeb Azure Web sitesi hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="2eac4-119">*Name* parametresini kullandığınızda **Get-AzureWebsite** , Web sitesi hakkında genişletilmiş bilgilerin bulunduğu bir **sitewithconfig** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="2eac4-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="2eac4-120">Örnek 3: tüm Web siteleri hakkında ayrıntılı bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="2eac4-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="2eac4-121">Bu komut, abonelikteki tüm Web siteleri hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="2eac4-122">Tüm Web sitelerini almak için **Get-AzureWebsite** komutunu kullanır ve sonra her siteyi ada göre almak için **ForEach-Object** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="2eac4-123">Örnek 4: dağıtım yuvası hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="2eac4-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="2eac4-124">Bu komut, ContosoWeb sitesinin hazırlama dağıtım yuvasını alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="2eac4-125">Dağıtım yuvaları, Azure Web sitenizin farklı sürümlerini herkese bırakmadan test edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2eac4-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="2eac4-126">Örnek 5: Web sitesi örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="2eac4-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="2eac4-127">Bu örnekteki komutlar, çalışmakta olan Web sitesi örnekleri hakkında bilgi almak için bir Azure Web sitesinin örnekler özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="2eac4-128">**Instances** özelliği, Azure modülünün sürüm 0.8.3 ' da **sitewithconfig** nesnesine eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="2eac4-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="2eac4-129">İlk komut, Web sitesinin şu anda çalışan tüm örneklerinin örnek kimliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="2eac4-130">İkinci komut, Web sitesinin çalışan örneklerinin sayısını alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="2eac4-131">**Count** özelliğini herhangi bir dizide kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2eac4-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="2eac4-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2eac4-132">PARAMETERS</span></span>

### <span data-ttu-id="2eac4-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="2eac4-133">-Name</span></span>
<span data-ttu-id="2eac4-134">Belirtilen Web sitesi hakkında ayrıntılı yapılandırma bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="2eac4-135">Abonelikteki bir Web sitesinin adını girin.</span><span class="sxs-lookup"><span data-stu-id="2eac4-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="2eac4-136">**Get-AzureWebsite** , varsayılan olarak geçerli abonelikteki tüm Web sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="2eac4-137">*Ad* değeri joker karakterleri desteklemez.</span><span class="sxs-lookup"><span data-stu-id="2eac4-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="2eac4-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="2eac4-138">-Profile</span></span>
<span data-ttu-id="2eac4-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2eac4-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2eac4-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2eac4-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2eac4-141">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="2eac4-141">-Slot</span></span>
<span data-ttu-id="2eac4-142">Web sitesinin belirtilen dağıtım yuvasını alır.</span><span class="sxs-lookup"><span data-stu-id="2eac4-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="2eac4-143">"Hazırlama" veya "üretim" gibi yuva adını girin.</span><span class="sxs-lookup"><span data-stu-id="2eac4-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="2eac4-144">Dağıtım yuvaları hakkında daha fazla bilgi için Microsoft Azure Web sitelerinde aşamalı dağıtım konusuna bakın https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="2eac4-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="2eac4-145">Var olan bir Azure Web sitesine dağıtım yuvası eklemek için Set-AzureWebsite cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2eac4-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="2eac4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eac4-146">CommonParameters</span></span>
<span data-ttu-id="2eac4-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2eac4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eac4-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eac4-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eac4-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2eac4-149">INPUTS</span></span>

### <span data-ttu-id="2eac4-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2eac4-150">None</span></span>
<span data-ttu-id="2eac4-151">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2eac4-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2eac4-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2eac4-152">OUTPUTS</span></span>

### <span data-ttu-id="2eac4-153">Microsoft. Windowsazve. Commands. Utilities. WebEntities. Services. WebEntities. site</span><span class="sxs-lookup"><span data-stu-id="2eac4-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="2eac4-154">**Get-AzureWebsite** , varsayılan olarak **site** nesnelerinin dizisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2eac4-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="2eac4-155">Microsoft. Windowsazve. Commands. Utilities. WebEntities. Services. WebEntities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="2eac4-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="2eac4-156">*Name* parametresini kullandığınızda **Get-AzureWebsite** , bir **sitewithconfig** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="2eac4-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="2eac4-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2eac4-157">NOTES</span></span>

## <span data-ttu-id="2eac4-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2eac4-158">RELATED LINKS</span></span>

[<span data-ttu-id="2eac4-159">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2eac4-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="2eac4-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2eac4-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="2eac4-161">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2eac4-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="2eac4-162">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2eac4-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="2eac4-163">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2eac4-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


