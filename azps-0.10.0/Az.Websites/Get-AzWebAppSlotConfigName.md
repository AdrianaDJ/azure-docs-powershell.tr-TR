---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 414e25840b03127bbe94586248641e103c1f7d88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936104"
---
# <span data-ttu-id="c0a8e-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c0a8e-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="c0a8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a8e-103">Web uygulaması yuva yapılandırması adlarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="c0a8e-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="c0a8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0a8e-104">SYNTAX</span></span>

### <span data-ttu-id="c0a8e-105">S1</span><span class="sxs-lookup"><span data-stu-id="c0a8e-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0a8e-106">S2</span><span class="sxs-lookup"><span data-stu-id="c0a8e-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0a8e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0a8e-107">DESCRIPTION</span></span>
<span data-ttu-id="c0a8e-108">**Get-AzWebAppSlotConfigName** cmdlet 'i, şu anda yuva ayarları olarak Işaretlenen uygulama ayarı ve bağlantı dizesi adlarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="c0a8e-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="c0a8e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0a8e-109">EXAMPLES</span></span>

### <span data-ttu-id="c0a8e-110">2</span><span class="sxs-lookup"><span data-stu-id="c0a8e-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c0a8e-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş olan ContosoSite adındaki Web uygulamasıyla ilgili uygulama ayarlarını ve bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c0a8e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0a8e-112">PARAMETERS</span></span>

### <span data-ttu-id="c0a8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a8e-113">-DefaultProfile</span></span>
<span data-ttu-id="c0a8e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0a8e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0a8e-115">-Name</span></span>
<span data-ttu-id="c0a8e-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="c0a8e-116">WebApp Name</span></span>

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

### <span data-ttu-id="c0a8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0a8e-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c0a8e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c0a8e-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c0a8e-119">-WebApp</span></span>
<span data-ttu-id="c0a8e-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="c0a8e-120">WebApp Object</span></span>

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

### <span data-ttu-id="c0a8e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a8e-121">CommonParameters</span></span>
<span data-ttu-id="c0a8e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a8e-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a8e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a8e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0a8e-124">INPUTS</span></span>

### <span data-ttu-id="c0a8e-125">Bölge</span><span class="sxs-lookup"><span data-stu-id="c0a8e-125">Site</span></span>
<span data-ttu-id="c0a8e-126">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c0a8e-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c0a8e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0a8e-127">OUTPUTS</span></span>

## <span data-ttu-id="c0a8e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0a8e-128">NOTES</span></span>

## <span data-ttu-id="c0a8e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0a8e-129">RELATED LINKS</span></span>

