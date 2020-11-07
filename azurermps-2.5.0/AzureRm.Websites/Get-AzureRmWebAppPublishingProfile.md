---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: 5884092a7520517844d6d0137023f99dc744cb86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939025"
---
# <span data-ttu-id="b11d4-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b11d4-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="b11d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b11d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b11d4-103">Bir Azure Web App yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="b11d4-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b11d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b11d4-104">SYNTAX</span></span>

### <span data-ttu-id="b11d4-105">S1</span><span class="sxs-lookup"><span data-stu-id="b11d4-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b11d4-106">S2</span><span class="sxs-lookup"><span data-stu-id="b11d4-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b11d4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b11d4-107">DESCRIPTION</span></span>
<span data-ttu-id="b11d4-108">**Get-AzureRmWebAppPublishingProfile** cmdlet 'ı bir Azure Web App Publishing profili alır.</span><span class="sxs-lookup"><span data-stu-id="b11d4-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="b11d4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b11d4-109">EXAMPLES</span></span>

### <span data-ttu-id="b11d4-110">2</span><span class="sxs-lookup"><span data-stu-id="b11d4-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="b11d4-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yayımlama profilini alır ve belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="b11d4-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="b11d4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b11d4-112">PARAMETERS</span></span>

### <span data-ttu-id="b11d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11d4-113">-DefaultProfile</span></span>
<span data-ttu-id="b11d4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b11d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11d4-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="b11d4-115">-Format</span></span>
<span data-ttu-id="b11d4-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="b11d4-116">Format</span></span>

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

### <span data-ttu-id="b11d4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b11d4-117">-Name</span></span>
<span data-ttu-id="b11d4-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="b11d4-118">WebApp Name</span></span>

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

### <span data-ttu-id="b11d4-119">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="b11d4-119">-OutputFile</span></span>
<span data-ttu-id="b11d4-120">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="b11d4-120">Output File</span></span>

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

### <span data-ttu-id="b11d4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b11d4-121">-ResourceGroupName</span></span>
<span data-ttu-id="b11d4-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b11d4-122">Resource Group Name</span></span>

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

### <span data-ttu-id="b11d4-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b11d4-123">-WebApp</span></span>
<span data-ttu-id="b11d4-124">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="b11d4-124">WebApp Object</span></span>

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

### <span data-ttu-id="b11d4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11d4-125">CommonParameters</span></span>
<span data-ttu-id="b11d4-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b11d4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11d4-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11d4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11d4-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b11d4-128">INPUTS</span></span>

### <span data-ttu-id="b11d4-129">Bölge</span><span class="sxs-lookup"><span data-stu-id="b11d4-129">Site</span></span>
<span data-ttu-id="b11d4-130">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b11d4-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b11d4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b11d4-131">OUTPUTS</span></span>

## <span data-ttu-id="b11d4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b11d4-132">NOTES</span></span>

## <span data-ttu-id="b11d4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b11d4-133">RELATED LINKS</span></span>

[<span data-ttu-id="b11d4-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b11d4-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="b11d4-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b11d4-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


