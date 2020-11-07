---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 942669106e70bbb8c5b5b6f059fe934effe9b7fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936512"
---
# <span data-ttu-id="e2b07-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2b07-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="e2b07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b07-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b07-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="e2b07-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="e2b07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2b07-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2b07-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b07-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="e2b07-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e2b07-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2b07-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b07-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2b07-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e2b07-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="e2b07-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e2b07-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2b07-110">PARAMETERS</span></span>

### <span data-ttu-id="e2b07-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e2b07-111">-AsJob</span></span>
<span data-ttu-id="e2b07-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e2b07-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2b07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b07-113">-DefaultProfile</span></span>
<span data-ttu-id="e2b07-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2b07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2b07-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e2b07-115">-Force</span></span>
<span data-ttu-id="e2b07-116">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="e2b07-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="e2b07-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2b07-117">-RouteFilter</span></span>
<span data-ttu-id="e2b07-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2b07-118">The RouteFilter</span></span>

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

### <span data-ttu-id="e2b07-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2b07-119">-Confirm</span></span>
<span data-ttu-id="e2b07-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2b07-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b07-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b07-121">-WhatIf</span></span>
<span data-ttu-id="e2b07-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2b07-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2b07-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2b07-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b07-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b07-124">CommonParameters</span></span>
<span data-ttu-id="e2b07-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2b07-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b07-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b07-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b07-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2b07-127">INPUTS</span></span>

### <span data-ttu-id="e2b07-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2b07-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e2b07-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2b07-129">OUTPUTS</span></span>

### <span data-ttu-id="e2b07-130">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2b07-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e2b07-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2b07-131">NOTES</span></span>

## <span data-ttu-id="e2b07-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2b07-132">RELATED LINKS</span></span>

