---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939988"
---
# <span data-ttu-id="e5c8a-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e5c8a-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e5c8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c8a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5c8a-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5c8a-103">SYNTAX</span></span>

### <span data-ttu-id="e5c8a-104">S1</span><span class="sxs-lookup"><span data-stu-id="e5c8a-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c8a-105">S2</span><span class="sxs-lookup"><span data-stu-id="e5c8a-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5c8a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5c8a-106">DESCRIPTION</span></span>
<span data-ttu-id="e5c8a-107">**Reset-AzureRmWebAppSlotPublishingProfile** cmdlet 'ı belirtilen Web App yuvasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="e5c8a-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="e5c8a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5c8a-108">EXAMPLES</span></span>

### <span data-ttu-id="e5c8a-109">2</span><span class="sxs-lookup"><span data-stu-id="e5c8a-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="e5c8a-110">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp için slot001 adındaki yuva profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="e5c8a-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e5c8a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5c8a-111">PARAMETERS</span></span>

### <span data-ttu-id="e5c8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c8a-112">-DefaultProfile</span></span>
<span data-ttu-id="e5c8a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5c8a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c8a-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5c8a-114">-Name</span></span>
<span data-ttu-id="e5c8a-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="e5c8a-115">WebApp Name</span></span>

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

### <span data-ttu-id="e5c8a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c8a-116">-ResourceGroupName</span></span>
<span data-ttu-id="e5c8a-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e5c8a-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e5c8a-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="e5c8a-118">-Slot</span></span>
<span data-ttu-id="e5c8a-119">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="e5c8a-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c8a-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e5c8a-120">-WebApp</span></span>
<span data-ttu-id="e5c8a-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="e5c8a-121">WebApp Object</span></span>

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

### <span data-ttu-id="e5c8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c8a-122">CommonParameters</span></span>
<span data-ttu-id="e5c8a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5c8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c8a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c8a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c8a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5c8a-125">INPUTS</span></span>

### <span data-ttu-id="e5c8a-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="e5c8a-126">Site</span></span>
<span data-ttu-id="e5c8a-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e5c8a-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e5c8a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5c8a-128">OUTPUTS</span></span>

## <span data-ttu-id="e5c8a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5c8a-129">NOTES</span></span>

## <span data-ttu-id="e5c8a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5c8a-130">RELATED LINKS</span></span>

