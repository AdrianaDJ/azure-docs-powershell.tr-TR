---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938748"
---
# <span data-ttu-id="5ab80-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5ab80-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="5ab80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab80-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab80-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ab80-103">SYNTAX</span></span>

### <span data-ttu-id="5ab80-104">S1</span><span class="sxs-lookup"><span data-stu-id="5ab80-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ab80-105">S2</span><span class="sxs-lookup"><span data-stu-id="5ab80-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ab80-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ab80-106">DESCRIPTION</span></span>
<span data-ttu-id="5ab80-107">**Reset-AzureRmWebAppPublishingProfile** cmdlet 'ı belirtilen Web uygulamasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="5ab80-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="5ab80-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ab80-108">EXAMPLES</span></span>

### <span data-ttu-id="5ab80-109">2</span><span class="sxs-lookup"><span data-stu-id="5ab80-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="5ab80-110">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="5ab80-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5ab80-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ab80-111">PARAMETERS</span></span>

### <span data-ttu-id="5ab80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab80-112">-DefaultProfile</span></span>
<span data-ttu-id="5ab80-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ab80-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ab80-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ab80-114">-Name</span></span>
<span data-ttu-id="5ab80-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="5ab80-115">WebApp Name</span></span>

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

### <span data-ttu-id="5ab80-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab80-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ab80-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5ab80-117">Resource Group Name</span></span>

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

### <span data-ttu-id="5ab80-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5ab80-118">-WebApp</span></span>
<span data-ttu-id="5ab80-119">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ab80-119">WebApp Object</span></span>

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

### <span data-ttu-id="5ab80-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab80-120">CommonParameters</span></span>
<span data-ttu-id="5ab80-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ab80-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab80-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab80-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab80-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ab80-123">INPUTS</span></span>

### <span data-ttu-id="5ab80-124">Bölge</span><span class="sxs-lookup"><span data-stu-id="5ab80-124">Site</span></span>
<span data-ttu-id="5ab80-125">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5ab80-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5ab80-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ab80-126">OUTPUTS</span></span>

## <span data-ttu-id="5ab80-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ab80-127">NOTES</span></span>

## <span data-ttu-id="5ab80-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ab80-128">RELATED LINKS</span></span>

