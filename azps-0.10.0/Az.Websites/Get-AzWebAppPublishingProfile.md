---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 477b60400082954eb12bd0756fb4380ece2a35ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936106"
---
# <span data-ttu-id="87f9e-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="87f9e-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="87f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="87f9e-103">Bir Azure Web App yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="87f9e-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="87f9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87f9e-104">SYNTAX</span></span>

### <span data-ttu-id="87f9e-105">S1</span><span class="sxs-lookup"><span data-stu-id="87f9e-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87f9e-106">S2</span><span class="sxs-lookup"><span data-stu-id="87f9e-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87f9e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="87f9e-107">DESCRIPTION</span></span>
<span data-ttu-id="87f9e-108">**Get-AzWebAppPublishingProfile** cmdlet 'ı bir Azure Web App Publishing profili alır.</span><span class="sxs-lookup"><span data-stu-id="87f9e-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="87f9e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87f9e-109">EXAMPLES</span></span>

### <span data-ttu-id="87f9e-110">2</span><span class="sxs-lookup"><span data-stu-id="87f9e-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="87f9e-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yayımlama profilini alır ve belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="87f9e-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="87f9e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87f9e-112">PARAMETERS</span></span>

### <span data-ttu-id="87f9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f9e-113">-DefaultProfile</span></span>
<span data-ttu-id="87f9e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87f9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87f9e-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="87f9e-115">-Format</span></span>
<span data-ttu-id="87f9e-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="87f9e-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f9e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="87f9e-117">-Name</span></span>
<span data-ttu-id="87f9e-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="87f9e-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f9e-119">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="87f9e-119">-OutputFile</span></span>
<span data-ttu-id="87f9e-120">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="87f9e-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f9e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f9e-121">-ResourceGroupName</span></span>
<span data-ttu-id="87f9e-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="87f9e-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f9e-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="87f9e-123">-WebApp</span></span>
<span data-ttu-id="87f9e-124">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="87f9e-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87f9e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f9e-125">CommonParameters</span></span>
<span data-ttu-id="87f9e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87f9e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f9e-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f9e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f9e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87f9e-128">INPUTS</span></span>

### <span data-ttu-id="87f9e-129">Bölge</span><span class="sxs-lookup"><span data-stu-id="87f9e-129">Site</span></span>
<span data-ttu-id="87f9e-130">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="87f9e-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="87f9e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87f9e-131">OUTPUTS</span></span>

## <span data-ttu-id="87f9e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87f9e-132">NOTES</span></span>

## <span data-ttu-id="87f9e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87f9e-133">RELATED LINKS</span></span>

[<span data-ttu-id="87f9e-134">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="87f9e-134">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="87f9e-135">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="87f9e-135">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


