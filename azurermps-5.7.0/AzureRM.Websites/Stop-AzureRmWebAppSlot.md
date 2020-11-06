---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 59fb1d649f5893dc09caa9799cd3412feae06deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587377"
---
# <span data-ttu-id="090c2-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="090c2-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="090c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="090c2-102">SYNOPSIS</span></span>
<span data-ttu-id="090c2-103">Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="090c2-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="090c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="090c2-104">SYNTAX</span></span>

### <span data-ttu-id="090c2-105">S1</span><span class="sxs-lookup"><span data-stu-id="090c2-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="090c2-106">S2</span><span class="sxs-lookup"><span data-stu-id="090c2-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="090c2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="090c2-107">DESCRIPTION</span></span>
<span data-ttu-id="090c2-108">**Stop-AzureRmWebAppSlot** cmdlet 'ı bir Azure Web App yuvasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="090c2-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="090c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="090c2-109">EXAMPLES</span></span>

### <span data-ttu-id="090c2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="090c2-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="090c2-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adlı Web uygulamasının bulunduğu yuva Slot001.</span><span class="sxs-lookup"><span data-stu-id="090c2-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="090c2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="090c2-112">PARAMETERS</span></span>

### <span data-ttu-id="090c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090c2-113">-DefaultProfile</span></span>
<span data-ttu-id="090c2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="090c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="090c2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="090c2-115">-Name</span></span>
<span data-ttu-id="090c2-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="090c2-116">WebApp Name</span></span>

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

### <span data-ttu-id="090c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="090c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="090c2-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="090c2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="090c2-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="090c2-119">-Slot</span></span>
<span data-ttu-id="090c2-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="090c2-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="090c2-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="090c2-121">-WebApp</span></span>
<span data-ttu-id="090c2-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="090c2-122">WebApp Object</span></span>

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

### <span data-ttu-id="090c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090c2-123">CommonParameters</span></span>
<span data-ttu-id="090c2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="090c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090c2-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="090c2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090c2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="090c2-126">INPUTS</span></span>

### <span data-ttu-id="090c2-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="090c2-127">Site</span></span>
<span data-ttu-id="090c2-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="090c2-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="090c2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="090c2-129">OUTPUTS</span></span>

## <span data-ttu-id="090c2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="090c2-130">NOTES</span></span>

## <span data-ttu-id="090c2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="090c2-131">RELATED LINKS</span></span>

