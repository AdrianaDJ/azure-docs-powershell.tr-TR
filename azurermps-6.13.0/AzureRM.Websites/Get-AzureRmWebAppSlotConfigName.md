---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: b1b9760d129a4177f979996f1ef46bd2a225f452
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761950"
---
# <span data-ttu-id="de44d-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="de44d-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="de44d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de44d-102">SYNOPSIS</span></span>
<span data-ttu-id="de44d-103">Web uygulaması yuva yapılandırması adlarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="de44d-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de44d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de44d-104">SYNTAX</span></span>

### <span data-ttu-id="de44d-105">S1</span><span class="sxs-lookup"><span data-stu-id="de44d-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de44d-106">S2</span><span class="sxs-lookup"><span data-stu-id="de44d-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de44d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="de44d-107">DESCRIPTION</span></span>
<span data-ttu-id="de44d-108">**Get-AzureRmWebAppSlotConfigName** cmdlet 'i, şu anda yuva ayarları olarak Işaretlenen uygulama ayarı ve bağlantı dizesi adlarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="de44d-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="de44d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de44d-109">EXAMPLES</span></span>

### <span data-ttu-id="de44d-110">2</span><span class="sxs-lookup"><span data-stu-id="de44d-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="de44d-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş olan ContosoSite adındaki Web uygulamasıyla ilgili uygulama ayarlarını ve bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="de44d-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="de44d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de44d-112">PARAMETERS</span></span>

### <span data-ttu-id="de44d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de44d-113">-DefaultProfile</span></span>
<span data-ttu-id="de44d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de44d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de44d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="de44d-115">-Name</span></span>
<span data-ttu-id="de44d-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="de44d-116">WebApp Name</span></span>

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

### <span data-ttu-id="de44d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de44d-117">-ResourceGroupName</span></span>
<span data-ttu-id="de44d-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="de44d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="de44d-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="de44d-119">-WebApp</span></span>
<span data-ttu-id="de44d-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="de44d-120">WebApp Object</span></span>

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

### <span data-ttu-id="de44d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de44d-121">CommonParameters</span></span>
<span data-ttu-id="de44d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de44d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de44d-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de44d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de44d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de44d-124">INPUTS</span></span>

### <span data-ttu-id="de44d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="de44d-125">System.String</span></span>

### <span data-ttu-id="de44d-126">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="de44d-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="de44d-127">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="de44d-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="de44d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de44d-128">OUTPUTS</span></span>

### <span data-ttu-id="de44d-129">Microsoft. Azure. Management. Web sitesi. modeller. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="de44d-129">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="de44d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de44d-130">NOTES</span></span>

## <span data-ttu-id="de44d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de44d-131">RELATED LINKS</span></span>
