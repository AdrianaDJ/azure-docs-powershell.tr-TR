---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a05dfcbf509ccb68c0b928467a5695361a4916e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589012"
---
# <span data-ttu-id="8c0bc-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="8c0bc-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="8c0bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0bc-103">Bir Azure Web App yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="8c0bc-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c0bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c0bc-104">SYNTAX</span></span>

### <span data-ttu-id="8c0bc-105">S1</span><span class="sxs-lookup"><span data-stu-id="8c0bc-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c0bc-106">S2</span><span class="sxs-lookup"><span data-stu-id="8c0bc-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c0bc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c0bc-107">DESCRIPTION</span></span>
<span data-ttu-id="8c0bc-108">**Get-AzureRmWebAppPublishingProfile** cmdlet 'ı bir Azure Web App Publishing profili alır.</span><span class="sxs-lookup"><span data-stu-id="8c0bc-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="8c0bc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c0bc-109">EXAMPLES</span></span>

### <span data-ttu-id="8c0bc-110">2</span><span class="sxs-lookup"><span data-stu-id="8c0bc-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="8c0bc-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yayımlama profilini alır ve belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="8c0bc-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="8c0bc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c0bc-112">PARAMETERS</span></span>

### <span data-ttu-id="8c0bc-113">Biçimli</span><span class="sxs-lookup"><span data-stu-id="8c0bc-113">-Format</span></span>
<span data-ttu-id="8c0bc-114">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="8c0bc-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0bc-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c0bc-115">-Name</span></span>
<span data-ttu-id="8c0bc-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8c0bc-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0bc-117">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="8c0bc-117">-OutputFile</span></span>
<span data-ttu-id="8c0bc-118">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="8c0bc-118">Output File</span></span>

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

### <span data-ttu-id="8c0bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c0bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="8c0bc-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8c0bc-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0bc-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8c0bc-121">-WebApp</span></span>
<span data-ttu-id="8c0bc-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8c0bc-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0bc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0bc-123">-DefaultProfile</span></span>
<span data-ttu-id="8c0bc-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c0bc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c0bc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0bc-125">CommonParameters</span></span>
<span data-ttu-id="8c0bc-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c0bc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0bc-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c0bc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0bc-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c0bc-128">INPUTS</span></span>

### <span data-ttu-id="8c0bc-129">Bölge</span><span class="sxs-lookup"><span data-stu-id="8c0bc-129">Site</span></span>
<span data-ttu-id="8c0bc-130">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8c0bc-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8c0bc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c0bc-131">OUTPUTS</span></span>

## <span data-ttu-id="8c0bc-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c0bc-132">NOTES</span></span>

## <span data-ttu-id="8c0bc-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c0bc-133">RELATED LINKS</span></span>

[<span data-ttu-id="8c0bc-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c0bc-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="8c0bc-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8c0bc-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


