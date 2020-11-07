---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939650"
---
# <span data-ttu-id="3a899-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a899-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="3a899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a899-102">SYNOPSIS</span></span>
<span data-ttu-id="3a899-103">Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="3a899-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a899-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a899-104">SYNTAX</span></span>

### <span data-ttu-id="3a899-105">S1</span><span class="sxs-lookup"><span data-stu-id="3a899-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a899-106">S2</span><span class="sxs-lookup"><span data-stu-id="3a899-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a899-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a899-107">DESCRIPTION</span></span>
<span data-ttu-id="3a899-108">**Stop-AzureRmWebAppSlot** cmdlet 'ı bir Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="3a899-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="3a899-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a899-109">EXAMPLES</span></span>

### <span data-ttu-id="3a899-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a899-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="3a899-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasının bulunduğu yuva Slot001.</span><span class="sxs-lookup"><span data-stu-id="3a899-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3a899-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a899-112">PARAMETERS</span></span>

### <span data-ttu-id="3a899-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a899-113">-DefaultProfile</span></span>
<span data-ttu-id="3a899-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a899-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a899-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a899-115">-Name</span></span>
<span data-ttu-id="3a899-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="3a899-116">WebApp Name</span></span>

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

### <span data-ttu-id="3a899-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a899-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a899-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3a899-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3a899-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="3a899-119">-Slot</span></span>
<span data-ttu-id="3a899-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="3a899-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3a899-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3a899-121">-WebApp</span></span>
<span data-ttu-id="3a899-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="3a899-122">WebApp Object</span></span>

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

### <span data-ttu-id="3a899-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a899-123">CommonParameters</span></span>
<span data-ttu-id="3a899-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a899-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a899-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a899-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a899-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a899-126">INPUTS</span></span>

### <span data-ttu-id="3a899-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="3a899-127">Site</span></span>
<span data-ttu-id="3a899-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a899-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3a899-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a899-129">OUTPUTS</span></span>

## <span data-ttu-id="3a899-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a899-130">NOTES</span></span>

## <span data-ttu-id="3a899-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a899-131">RELATED LINKS</span></span>

