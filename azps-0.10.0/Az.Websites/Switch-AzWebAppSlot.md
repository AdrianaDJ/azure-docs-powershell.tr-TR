---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/switch-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: e30179ce2e9198729771d406d1963ff0048e05b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936045"
---
# <span data-ttu-id="bbd81-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbd81-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="bbd81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd81-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd81-103">İki yuvaya Web uygulamasıyla takas etme</span><span class="sxs-lookup"><span data-stu-id="bbd81-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="bbd81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbd81-104">SYNTAX</span></span>

### <span data-ttu-id="bbd81-105">S1</span><span class="sxs-lookup"><span data-stu-id="bbd81-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbd81-106">S2</span><span class="sxs-lookup"><span data-stu-id="bbd81-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd81-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbd81-107">DESCRIPTION</span></span>
<span data-ttu-id="bbd81-108">**Switch-AzWebAppSlot** , bir Azure Web uygulamasıyla ilişkilendirilmiş iki yuvaya geçer.</span><span class="sxs-lookup"><span data-stu-id="bbd81-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="bbd81-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbd81-109">EXAMPLES</span></span>

### <span data-ttu-id="bbd81-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bbd81-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="bbd81-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp için yuva "sourceslotu" yuvasını</span><span class="sxs-lookup"><span data-stu-id="bbd81-111">This command will switch slot "sourceslot" slot with "destinationslot" for for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="bbd81-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbd81-112">PARAMETERS</span></span>

### <span data-ttu-id="bbd81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd81-113">-DefaultProfile</span></span>
<span data-ttu-id="bbd81-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbd81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbd81-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="bbd81-115">-DestinationSlotName</span></span>
<span data-ttu-id="bbd81-116">Hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="bbd81-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd81-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbd81-117">-Name</span></span>
<span data-ttu-id="bbd81-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="bbd81-118">WebApp Name</span></span>

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

### <span data-ttu-id="bbd81-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="bbd81-119">-PreserveVnet</span></span>
<span data-ttu-id="bbd81-120">VNET Boole değeri</span><span class="sxs-lookup"><span data-stu-id="bbd81-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd81-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd81-121">-ResourceGroupName</span></span>
<span data-ttu-id="bbd81-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bbd81-122">Resource Group Name</span></span>

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

### <span data-ttu-id="bbd81-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="bbd81-123">-SourceSlotName</span></span>
<span data-ttu-id="bbd81-124">Kaynak yuva adı</span><span class="sxs-lookup"><span data-stu-id="bbd81-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd81-125">-Swapwithpreview eylemi</span><span class="sxs-lookup"><span data-stu-id="bbd81-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="bbd81-126">Önizleme eylemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="bbd81-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd81-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bbd81-127">-WebApp</span></span>
<span data-ttu-id="bbd81-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="bbd81-128">WebApp Object</span></span>

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

### <span data-ttu-id="bbd81-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbd81-129">-Confirm</span></span>
<span data-ttu-id="bbd81-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbd81-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd81-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd81-131">-WhatIf</span></span>
<span data-ttu-id="bbd81-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbd81-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd81-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbd81-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd81-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd81-134">CommonParameters</span></span>
<span data-ttu-id="bbd81-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbd81-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd81-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd81-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd81-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbd81-137">INPUTS</span></span>

### <span data-ttu-id="bbd81-138">Bölge</span><span class="sxs-lookup"><span data-stu-id="bbd81-138">Site</span></span>
<span data-ttu-id="bbd81-139">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bbd81-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bbd81-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbd81-140">OUTPUTS</span></span>

## <span data-ttu-id="bbd81-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbd81-141">NOTES</span></span>

## <span data-ttu-id="bbd81-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbd81-142">RELATED LINKS</span></span>

