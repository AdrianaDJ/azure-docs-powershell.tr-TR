---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106184"
---
# <span data-ttu-id="95d1d-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95d1d-101">New-AzureWebsite</span></span>

## <span data-ttu-id="95d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="95d1d-103">Azure 'da çalıştırmak için yeni bir Web sitesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="95d1d-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="95d1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95d1d-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="95d1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="95d1d-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="95d1d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95d1d-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="95d1d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95d1d-108">Cmdlet, Azure 'da çalıştırmak için yeni bir Web sitesi oluşturur ve GitHub aracılığıyla dağıtıma hazırlar.</span><span class="sxs-lookup"><span data-stu-id="95d1d-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="95d1d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95d1d-109">EXAMPLES</span></span>

### <span data-ttu-id="95d1d-110">Örnek 1: git ile yeni bir Web sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="95d1d-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="95d1d-111">Bu örnek, Azure 'da yeni bir Web sitesi ve dosyaları yeni Web sitesine dağıtmak için yerel bir git deposu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95d1d-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="95d1d-112">Örnek 2: GitHub ile tümleştirilmiş Web sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="95d1d-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="95d1d-113">Bu örnek, myaccount/myrepo adlı GitHub havuzuna bağlı yeni bir Web sitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95d1d-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="95d1d-114">GitHub deposundaki işlemeler Azure 'daki Web sitesine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="95d1d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95d1d-115">PARAMETERS</span></span>

### <span data-ttu-id="95d1d-116">-Git</span><span class="sxs-lookup"><span data-stu-id="95d1d-116">-Git</span></span>
<span data-ttu-id="95d1d-117">Yerel bir git deposu kurar ve Web sitesine bağlar.</span><span class="sxs-lookup"><span data-stu-id="95d1d-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="95d1d-118">Belirtilmişse, bu parametre yerel dizinde bir git deposu ayarlar ve Azure 'daki Web sitesine bağlayan ' Azure ' adlı uzak bir depo ekler.</span><span class="sxs-lookup"><span data-stu-id="95d1d-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d1d-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="95d1d-119">-GitHub</span></span>
<span data-ttu-id="95d1d-120">Bu cmdlet 'in yeni Web sitesini varolan bir GitHub deposuna göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="95d1d-121">Gıuthub havuzuna yapılan işlemeler, Azure 'daki Web sitesine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d1d-122">-GithubCredentials</span><span class="sxs-lookup"><span data-stu-id="95d1d-122">-GithubCredentials</span></span>
<span data-ttu-id="95d1d-123">GitHub 'ya bağlanmak için Kullanıcı adı ve parola kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-123">Specifies the user name and password credentials to connect to Github.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d1d-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="95d1d-124">-GithubRepository</span></span>
<span data-ttu-id="95d1d-125">Bu Web sitesine bağlanacak GitHub deposunun tam adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="95d1d-126">Örneğin, `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="95d1d-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="95d1d-127">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="95d1d-127">-Hostname</span></span>
<span data-ttu-id="95d1d-128">Yeni Web sitesi için alternatif bir ana bilgisayar adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="95d1d-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="95d1d-129">-Location</span></span>
<span data-ttu-id="95d1d-130">Web sitesini dağıtmak istediğiniz veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="95d1d-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="95d1d-131">-Name</span></span>
<span data-ttu-id="95d1d-132">Web sitesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="95d1d-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="95d1d-133">-Profile</span></span>
<span data-ttu-id="95d1d-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95d1d-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="95d1d-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95d1d-136">-Publishingkullanıcıadı</span><span class="sxs-lookup"><span data-stu-id="95d1d-136">-PublishingUsername</span></span>
<span data-ttu-id="95d1d-137">Git dağıtımının Azure portalında belirttiğiniz kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="95d1d-138">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="95d1d-138">-Slot</span></span>
<span data-ttu-id="95d1d-139">Web sitesi için bir yuva adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="95d1d-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="95d1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d1d-140">CommonParameters</span></span>
<span data-ttu-id="95d1d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95d1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d1d-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d1d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d1d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95d1d-143">INPUTS</span></span>

## <span data-ttu-id="95d1d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95d1d-144">OUTPUTS</span></span>

## <span data-ttu-id="95d1d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95d1d-145">NOTES</span></span>

## <span data-ttu-id="95d1d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95d1d-146">RELATED LINKS</span></span>

[<span data-ttu-id="95d1d-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95d1d-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


