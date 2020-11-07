---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 196e653447204b65c7f431e29fe76078a268dda1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764503"
---
# <span data-ttu-id="55bdf-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="55bdf-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="55bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="55bdf-103">Web uygulaması yuva yapılandırması adlarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="55bdf-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55bdf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55bdf-104">SYNTAX</span></span>

### <span data-ttu-id="55bdf-105">S1</span><span class="sxs-lookup"><span data-stu-id="55bdf-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55bdf-106">S2</span><span class="sxs-lookup"><span data-stu-id="55bdf-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55bdf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55bdf-107">DESCRIPTION</span></span>
<span data-ttu-id="55bdf-108">**Get-AzureRmWebAppSlotConfigName** cmdlet 'i, şu anda yuva ayarları olarak Işaretlenen uygulama ayarı ve bağlantı dizesi adlarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="55bdf-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="55bdf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55bdf-109">EXAMPLES</span></span>

### <span data-ttu-id="55bdf-110">2</span><span class="sxs-lookup"><span data-stu-id="55bdf-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="55bdf-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş olan ContosoSite adındaki Web uygulamasıyla ilgili uygulama ayarlarını ve bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="55bdf-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="55bdf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55bdf-112">PARAMETERS</span></span>

### <span data-ttu-id="55bdf-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="55bdf-113">-Name</span></span>
<span data-ttu-id="55bdf-114">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="55bdf-114">WebApp Name</span></span>

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

### <span data-ttu-id="55bdf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55bdf-115">-ResourceGroupName</span></span>
<span data-ttu-id="55bdf-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="55bdf-116">Resource Group Name</span></span>

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

### <span data-ttu-id="55bdf-117">-WebApp</span><span class="sxs-lookup"><span data-stu-id="55bdf-117">-WebApp</span></span>
<span data-ttu-id="55bdf-118">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="55bdf-118">WebApp Object</span></span>

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

### <span data-ttu-id="55bdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55bdf-119">-DefaultProfile</span></span>
<span data-ttu-id="55bdf-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55bdf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55bdf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55bdf-121">CommonParameters</span></span>
<span data-ttu-id="55bdf-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55bdf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55bdf-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55bdf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55bdf-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55bdf-124">INPUTS</span></span>

### <span data-ttu-id="55bdf-125">Bölge</span><span class="sxs-lookup"><span data-stu-id="55bdf-125">Site</span></span>
<span data-ttu-id="55bdf-126">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="55bdf-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="55bdf-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55bdf-127">OUTPUTS</span></span>

## <span data-ttu-id="55bdf-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55bdf-128">NOTES</span></span>

## <span data-ttu-id="55bdf-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55bdf-129">RELATED LINKS</span></span>
