---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266182"
---
# <span data-ttu-id="b442d-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="b442d-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="b442d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b442d-102">SYNOPSIS</span></span>
<span data-ttu-id="b442d-103">Web uygulaması yuva yapılandırması adlarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="b442d-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="b442d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b442d-104">SYNTAX</span></span>

### <span data-ttu-id="b442d-105">S1</span><span class="sxs-lookup"><span data-stu-id="b442d-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b442d-106">S2</span><span class="sxs-lookup"><span data-stu-id="b442d-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b442d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b442d-107">DESCRIPTION</span></span>
<span data-ttu-id="b442d-108">**Get-AzWebAppSlotConfigName** cmdlet 'i, şu anda yuva ayarları olarak Işaretlenen uygulama ayarı ve bağlantı dizesi adlarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="b442d-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="b442d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b442d-109">EXAMPLES</span></span>

### <span data-ttu-id="b442d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b442d-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b442d-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş olan ContosoSite adındaki Web uygulamasıyla ilgili uygulama ayarlarını ve bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b442d-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b442d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b442d-112">PARAMETERS</span></span>

### <span data-ttu-id="b442d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b442d-113">-DefaultProfile</span></span>
<span data-ttu-id="b442d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b442d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b442d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b442d-115">-Name</span></span>
<span data-ttu-id="b442d-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="b442d-116">WebApp Name</span></span>

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

### <span data-ttu-id="b442d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b442d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b442d-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b442d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b442d-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b442d-119">-WebApp</span></span>
<span data-ttu-id="b442d-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="b442d-120">WebApp Object</span></span>

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

### <span data-ttu-id="b442d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b442d-121">CommonParameters</span></span>
<span data-ttu-id="b442d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b442d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b442d-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b442d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b442d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b442d-124">INPUTS</span></span>

### <span data-ttu-id="b442d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b442d-125">System.String</span></span>

### <span data-ttu-id="b442d-126">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="b442d-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b442d-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b442d-127">OUTPUTS</span></span>

### <span data-ttu-id="b442d-128">Microsoft. Azure. Management. Web sitesi. modeller. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="b442d-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="b442d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b442d-129">NOTES</span></span>

## <span data-ttu-id="b442d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b442d-130">RELATED LINKS</span></span>
