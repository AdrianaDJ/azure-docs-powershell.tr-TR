---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: 9522fe6925ac266ff87f3ba6b3540980d91c160f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765135"
---
# <span data-ttu-id="ed7b1-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed7b1-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ed7b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7b1-103">İki yuvaya Web uygulamasıyla takas etme</span><span class="sxs-lookup"><span data-stu-id="ed7b1-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed7b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed7b1-104">SYNTAX</span></span>

### <span data-ttu-id="ed7b1-105">S1</span><span class="sxs-lookup"><span data-stu-id="ed7b1-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed7b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="ed7b1-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed7b1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed7b1-107">DESCRIPTION</span></span>
<span data-ttu-id="ed7b1-108">**Switch-AzureRmWebAppSlot** , bir Azure Web uygulamasıyla ilişkilendirilmiş iki yuvaya geçer.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="ed7b1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed7b1-109">EXAMPLES</span></span>

### <span data-ttu-id="ed7b1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed7b1-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ed7b1-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp için yuva "sourceslotu" yuvasını</span><span class="sxs-lookup"><span data-stu-id="ed7b1-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ed7b1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed7b1-112">PARAMETERS</span></span>

### <span data-ttu-id="ed7b1-113">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="ed7b1-113">-DestinationSlotName</span></span>
<span data-ttu-id="ed7b1-114">Hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="ed7b1-114">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7b1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed7b1-115">-Name</span></span>
<span data-ttu-id="ed7b1-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ed7b1-116">WebApp Name</span></span>

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

### <span data-ttu-id="ed7b1-117">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="ed7b1-117">-PreserveVnet</span></span>
<span data-ttu-id="ed7b1-118">VNET Boole değeri</span><span class="sxs-lookup"><span data-stu-id="ed7b1-118">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed7b1-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ed7b1-120">Resource Group Name</span></span>

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

### <span data-ttu-id="ed7b1-121">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="ed7b1-121">-SourceSlotName</span></span>
<span data-ttu-id="ed7b1-122">Kaynak yuva adı</span><span class="sxs-lookup"><span data-stu-id="ed7b1-122">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7b1-123">-Swapwithpreview eylemi</span><span class="sxs-lookup"><span data-stu-id="ed7b1-123">-SwapWithPreviewAction</span></span>
<span data-ttu-id="ed7b1-124">Önizleme eylemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="ed7b1-124">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7b1-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ed7b1-125">-WebApp</span></span>
<span data-ttu-id="ed7b1-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="ed7b1-126">WebApp Object</span></span>

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

### <span data-ttu-id="ed7b1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed7b1-127">-Confirm</span></span>
<span data-ttu-id="ed7b1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed7b1-129">-WhatIf</span></span>
<span data-ttu-id="ed7b1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed7b1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7b1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7b1-132">-DefaultProfile</span></span>
<span data-ttu-id="ed7b1-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed7b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7b1-134">CommonParameters</span></span>
<span data-ttu-id="ed7b1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7b1-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7b1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7b1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed7b1-137">INPUTS</span></span>

### <span data-ttu-id="ed7b1-138">Bölge</span><span class="sxs-lookup"><span data-stu-id="ed7b1-138">Site</span></span>
<span data-ttu-id="ed7b1-139">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ed7b1-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ed7b1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed7b1-140">OUTPUTS</span></span>

## <span data-ttu-id="ed7b1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed7b1-141">NOTES</span></span>

## <span data-ttu-id="ed7b1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed7b1-142">RELATED LINKS</span></span>
