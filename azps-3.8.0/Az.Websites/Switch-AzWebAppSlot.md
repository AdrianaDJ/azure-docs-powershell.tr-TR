---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098064"
---
# <span data-ttu-id="762da-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="762da-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="762da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="762da-102">SYNOPSIS</span></span>
<span data-ttu-id="762da-103">İki yuvaya Web uygulamasıyla takas etme</span><span class="sxs-lookup"><span data-stu-id="762da-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="762da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="762da-104">SYNTAX</span></span>

### <span data-ttu-id="762da-105">S1</span><span class="sxs-lookup"><span data-stu-id="762da-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762da-106">S2</span><span class="sxs-lookup"><span data-stu-id="762da-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="762da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="762da-107">DESCRIPTION</span></span>
<span data-ttu-id="762da-108">**Switch-AzWebAppSlot** , bir Azure Web uygulamasıyla ilişkilendirilmiş iki yuvaya geçer.</span><span class="sxs-lookup"><span data-stu-id="762da-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="762da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="762da-109">EXAMPLES</span></span>

### <span data-ttu-id="762da-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="762da-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="762da-111">Bu komut, "sourcesslot" yuvasını "destinationslot" kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp</span><span class="sxs-lookup"><span data-stu-id="762da-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="762da-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="762da-112">PARAMETERS</span></span>

### <span data-ttu-id="762da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762da-113">-DefaultProfile</span></span>
<span data-ttu-id="762da-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="762da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="762da-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="762da-115">-DestinationSlotName</span></span>
<span data-ttu-id="762da-116">Hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="762da-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="762da-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="762da-117">-Name</span></span>
<span data-ttu-id="762da-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="762da-118">WebApp Name</span></span>

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

### <span data-ttu-id="762da-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="762da-119">-PreserveVnet</span></span>
<span data-ttu-id="762da-120">VNET Boole değeri</span><span class="sxs-lookup"><span data-stu-id="762da-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="762da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762da-121">-ResourceGroupName</span></span>
<span data-ttu-id="762da-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="762da-122">Resource Group Name</span></span>

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

### <span data-ttu-id="762da-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="762da-123">-SourceSlotName</span></span>
<span data-ttu-id="762da-124">Kaynak yuva adı</span><span class="sxs-lookup"><span data-stu-id="762da-124">Source Slot Name</span></span>

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

### <span data-ttu-id="762da-125">-Swapwithpreview eylemi</span><span class="sxs-lookup"><span data-stu-id="762da-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="762da-126">Önizleme eylemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="762da-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="762da-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="762da-127">-WebApp</span></span>
<span data-ttu-id="762da-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="762da-128">WebApp Object</span></span>

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

### <span data-ttu-id="762da-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="762da-129">-Confirm</span></span>
<span data-ttu-id="762da-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="762da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="762da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762da-131">-WhatIf</span></span>
<span data-ttu-id="762da-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="762da-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="762da-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="762da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="762da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762da-134">CommonParameters</span></span>
<span data-ttu-id="762da-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="762da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762da-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762da-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762da-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="762da-137">INPUTS</span></span>

### <span data-ttu-id="762da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="762da-138">System.String</span></span>

### <span data-ttu-id="762da-139">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="762da-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="762da-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="762da-140">OUTPUTS</span></span>

### <span data-ttu-id="762da-141">System. void</span><span class="sxs-lookup"><span data-stu-id="762da-141">System.Void</span></span>

## <span data-ttu-id="762da-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="762da-142">NOTES</span></span>

## <span data-ttu-id="762da-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="762da-143">RELATED LINKS</span></span>
