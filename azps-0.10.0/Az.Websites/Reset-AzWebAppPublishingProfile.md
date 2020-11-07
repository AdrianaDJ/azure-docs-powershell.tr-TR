---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936079"
---
# <span data-ttu-id="c762b-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c762b-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="c762b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c762b-102">SYNOPSIS</span></span>

## <span data-ttu-id="c762b-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c762b-103">SYNTAX</span></span>

### <span data-ttu-id="c762b-104">S1</span><span class="sxs-lookup"><span data-stu-id="c762b-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c762b-105">S2</span><span class="sxs-lookup"><span data-stu-id="c762b-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c762b-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="c762b-106">DESCRIPTION</span></span>
<span data-ttu-id="c762b-107">**Reset-AzWebAppPublishingProfile** cmdlet 'i, belirtilen Web uygulamasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="c762b-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="c762b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c762b-108">EXAMPLES</span></span>

### <span data-ttu-id="c762b-109">2</span><span class="sxs-lookup"><span data-stu-id="c762b-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c762b-110">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="c762b-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c762b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c762b-111">PARAMETERS</span></span>

### <span data-ttu-id="c762b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c762b-112">-DefaultProfile</span></span>
<span data-ttu-id="c762b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c762b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c762b-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="c762b-114">-Name</span></span>
<span data-ttu-id="c762b-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="c762b-115">WebApp Name</span></span>

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

### <span data-ttu-id="c762b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c762b-116">-ResourceGroupName</span></span>
<span data-ttu-id="c762b-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c762b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="c762b-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c762b-118">-WebApp</span></span>
<span data-ttu-id="c762b-119">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="c762b-119">WebApp Object</span></span>

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

### <span data-ttu-id="c762b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c762b-120">CommonParameters</span></span>
<span data-ttu-id="c762b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c762b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c762b-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c762b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c762b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c762b-123">INPUTS</span></span>

### <span data-ttu-id="c762b-124">Bölge</span><span class="sxs-lookup"><span data-stu-id="c762b-124">Site</span></span>
<span data-ttu-id="c762b-125">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c762b-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c762b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c762b-126">OUTPUTS</span></span>

## <span data-ttu-id="c762b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c762b-127">NOTES</span></span>

## <span data-ttu-id="c762b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c762b-128">RELATED LINKS</span></span>

