---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: ff05a30c495475b63b0385f3398c78e0b018a4bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939664"
---
# <span data-ttu-id="22d46-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="22d46-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="22d46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d46-102">SYNOPSIS</span></span>
<span data-ttu-id="22d46-103">Web uygulaması yuva yapılandırması adlarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="22d46-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22d46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22d46-104">SYNTAX</span></span>

### <span data-ttu-id="22d46-105">S1</span><span class="sxs-lookup"><span data-stu-id="22d46-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d46-106">S2</span><span class="sxs-lookup"><span data-stu-id="22d46-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22d46-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="22d46-107">DESCRIPTION</span></span>
<span data-ttu-id="22d46-108">**Get-AzureRmWebAppSlotConfigName** cmdlet 'i, şu anda yuva ayarları olarak Işaretlenen uygulama ayarı ve bağlantı dizesi adlarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="22d46-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="22d46-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22d46-109">EXAMPLES</span></span>

### <span data-ttu-id="22d46-110">2</span><span class="sxs-lookup"><span data-stu-id="22d46-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="22d46-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş olan ContosoSite adındaki Web uygulamasıyla ilgili uygulama ayarlarını ve bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="22d46-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="22d46-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22d46-112">PARAMETERS</span></span>

### <span data-ttu-id="22d46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d46-113">-DefaultProfile</span></span>
<span data-ttu-id="22d46-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22d46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22d46-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="22d46-115">-Name</span></span>
<span data-ttu-id="22d46-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="22d46-116">WebApp Name</span></span>

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

### <span data-ttu-id="22d46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d46-117">-ResourceGroupName</span></span>
<span data-ttu-id="22d46-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="22d46-118">Resource Group Name</span></span>

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

### <span data-ttu-id="22d46-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="22d46-119">-WebApp</span></span>
<span data-ttu-id="22d46-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="22d46-120">WebApp Object</span></span>

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

### <span data-ttu-id="22d46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d46-121">CommonParameters</span></span>
<span data-ttu-id="22d46-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22d46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d46-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d46-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d46-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22d46-124">INPUTS</span></span>

### <span data-ttu-id="22d46-125">Bölge</span><span class="sxs-lookup"><span data-stu-id="22d46-125">Site</span></span>
<span data-ttu-id="22d46-126">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="22d46-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="22d46-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22d46-127">OUTPUTS</span></span>

## <span data-ttu-id="22d46-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22d46-128">NOTES</span></span>

## <span data-ttu-id="22d46-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22d46-129">RELATED LINKS</span></span>

