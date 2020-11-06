---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: b519012104472d9b97f5f0a5e4b699829b99fff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593353"
---
# <span data-ttu-id="b6f5d-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b6f5d-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="b6f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f5d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f5d-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6f5d-103">SYNTAX</span></span>

### <span data-ttu-id="b6f5d-104">S1</span><span class="sxs-lookup"><span data-stu-id="b6f5d-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6f5d-105">S2</span><span class="sxs-lookup"><span data-stu-id="b6f5d-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6f5d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6f5d-106">DESCRIPTION</span></span>
<span data-ttu-id="b6f5d-107">**Reset-AzureRmWebAppPublishingProfile** cmdlet 'ı belirtilen Web uygulamasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="b6f5d-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="b6f5d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6f5d-108">EXAMPLES</span></span>

### <span data-ttu-id="b6f5d-109">2</span><span class="sxs-lookup"><span data-stu-id="b6f5d-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="b6f5d-110">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="b6f5d-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b6f5d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6f5d-111">PARAMETERS</span></span>

### <span data-ttu-id="b6f5d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f5d-112">-DefaultProfile</span></span>
<span data-ttu-id="b6f5d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6f5d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6f5d-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6f5d-114">-Name</span></span>
<span data-ttu-id="b6f5d-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="b6f5d-115">WebApp Name</span></span>

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

### <span data-ttu-id="b6f5d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f5d-116">-ResourceGroupName</span></span>
<span data-ttu-id="b6f5d-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b6f5d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="b6f5d-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b6f5d-118">-WebApp</span></span>
<span data-ttu-id="b6f5d-119">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="b6f5d-119">WebApp Object</span></span>

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

### <span data-ttu-id="b6f5d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f5d-120">CommonParameters</span></span>
<span data-ttu-id="b6f5d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6f5d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f5d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f5d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f5d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6f5d-123">INPUTS</span></span>

### <span data-ttu-id="b6f5d-124">Bölge</span><span class="sxs-lookup"><span data-stu-id="b6f5d-124">Site</span></span>
<span data-ttu-id="b6f5d-125">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b6f5d-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b6f5d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6f5d-126">OUTPUTS</span></span>

## <span data-ttu-id="b6f5d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6f5d-127">NOTES</span></span>

## <span data-ttu-id="b6f5d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6f5d-128">RELATED LINKS</span></span>

