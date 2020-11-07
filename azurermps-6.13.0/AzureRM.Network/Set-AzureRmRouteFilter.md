---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 5dc2b6a9650cdf4110858edf1b061f69adac48f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762918"
---
# <span data-ttu-id="9df43-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9df43-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="9df43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9df43-102">SYNOPSIS</span></span>
<span data-ttu-id="9df43-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="9df43-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9df43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9df43-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9df43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9df43-105">DESCRIPTION</span></span>
<span data-ttu-id="9df43-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="9df43-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9df43-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9df43-107">EXAMPLES</span></span>

### <span data-ttu-id="9df43-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9df43-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9df43-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="9df43-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9df43-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9df43-110">PARAMETERS</span></span>

### <span data-ttu-id="9df43-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="9df43-111">-AsJob</span></span>
<span data-ttu-id="9df43-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9df43-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df43-113">-DefaultProfile</span></span>
<span data-ttu-id="9df43-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9df43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9df43-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9df43-115">-Force</span></span>
<span data-ttu-id="9df43-116">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="9df43-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df43-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9df43-117">-RouteFilter</span></span>
<span data-ttu-id="9df43-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9df43-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9df43-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="9df43-119">-Confirm</span></span>
<span data-ttu-id="9df43-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9df43-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9df43-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9df43-121">-WhatIf</span></span>
<span data-ttu-id="9df43-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9df43-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9df43-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9df43-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9df43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df43-124">CommonParameters</span></span>
<span data-ttu-id="9df43-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9df43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df43-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9df43-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df43-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9df43-127">INPUTS</span></span>

### <span data-ttu-id="9df43-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9df43-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="9df43-129">Parametreler: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9df43-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="9df43-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9df43-130">OUTPUTS</span></span>

### <span data-ttu-id="9df43-131">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9df43-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9df43-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9df43-132">NOTES</span></span>

## <span data-ttu-id="9df43-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9df43-133">RELATED LINKS</span></span>
