---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: bd871e75e5a4f9c8e5c28e8788c8ef291a88e6db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753823"
---
# <span data-ttu-id="b2a60-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="b2a60-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="b2a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2a60-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a60-103">Web uygulaması yuva yapılandırması adlarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="b2a60-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="b2a60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2a60-104">SYNTAX</span></span>

### <span data-ttu-id="b2a60-105">S1</span><span class="sxs-lookup"><span data-stu-id="b2a60-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2a60-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2a60-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2a60-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2a60-107">DESCRIPTION</span></span>
<span data-ttu-id="b2a60-108">**Get-AzWebAppSlotConfigName** cmdlet 'i, şu anda yuva ayarları olarak Işaretlenen uygulama ayarı ve bağlantı dizesi adlarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="b2a60-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="b2a60-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2a60-109">EXAMPLES</span></span>

### <span data-ttu-id="b2a60-110">2</span><span class="sxs-lookup"><span data-stu-id="b2a60-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b2a60-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş olan ContosoSite adındaki Web uygulamasıyla ilgili uygulama ayarlarını ve bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b2a60-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b2a60-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2a60-112">PARAMETERS</span></span>

### <span data-ttu-id="b2a60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a60-113">-DefaultProfile</span></span>
<span data-ttu-id="b2a60-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2a60-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2a60-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2a60-115">-Name</span></span>
<span data-ttu-id="b2a60-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="b2a60-116">WebApp Name</span></span>

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

### <span data-ttu-id="b2a60-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2a60-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2a60-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b2a60-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b2a60-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b2a60-119">-WebApp</span></span>
<span data-ttu-id="b2a60-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="b2a60-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a60-121">CommonParameters</span></span>
<span data-ttu-id="b2a60-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2a60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a60-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2a60-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a60-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2a60-124">INPUTS</span></span>

### <span data-ttu-id="b2a60-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b2a60-125">System.String</span></span>

### <span data-ttu-id="b2a60-126">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="b2a60-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b2a60-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2a60-127">OUTPUTS</span></span>

### <span data-ttu-id="b2a60-128">Microsoft. Azure. Management. Web sitesi. modeller. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="b2a60-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="b2a60-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2a60-129">NOTES</span></span>

## <span data-ttu-id="b2a60-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2a60-130">RELATED LINKS</span></span>
