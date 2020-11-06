---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 1091a8433cd226982d3f2addf7e02b2414020fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593719"
---
# <span data-ttu-id="1084f-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1084f-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="1084f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1084f-102">SYNOPSIS</span></span>
<span data-ttu-id="1084f-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="1084f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1084f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1084f-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1084f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1084f-105">DESCRIPTION</span></span>
<span data-ttu-id="1084f-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="1084f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1084f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1084f-107">EXAMPLES</span></span>

### <span data-ttu-id="1084f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1084f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1084f-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="1084f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1084f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1084f-110">PARAMETERS</span></span>

### <span data-ttu-id="1084f-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="1084f-111">-AsJob</span></span>
<span data-ttu-id="1084f-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1084f-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1084f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1084f-113">-DefaultProfile</span></span>
<span data-ttu-id="1084f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1084f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1084f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1084f-115">-Force</span></span>
<span data-ttu-id="1084f-116">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="1084f-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1084f-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1084f-117">-RouteFilter</span></span>
<span data-ttu-id="1084f-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1084f-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1084f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="1084f-119">-Confirm</span></span>
<span data-ttu-id="1084f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1084f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1084f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1084f-121">-WhatIf</span></span>
<span data-ttu-id="1084f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1084f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1084f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1084f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1084f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1084f-124">CommonParameters</span></span>
<span data-ttu-id="1084f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1084f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1084f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1084f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1084f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1084f-127">INPUTS</span></span>

### <span data-ttu-id="1084f-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1084f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1084f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1084f-129">OUTPUTS</span></span>

### <span data-ttu-id="1084f-130">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1084f-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1084f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1084f-131">NOTES</span></span>

## <span data-ttu-id="1084f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1084f-132">RELATED LINKS</span></span>

