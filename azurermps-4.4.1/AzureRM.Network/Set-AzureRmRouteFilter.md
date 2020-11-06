---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589225"
---
# <span data-ttu-id="c915e-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c915e-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="c915e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c915e-102">SYNOPSIS</span></span>
<span data-ttu-id="c915e-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="c915e-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c915e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c915e-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c915e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c915e-105">DESCRIPTION</span></span>
<span data-ttu-id="c915e-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="c915e-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c915e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c915e-107">EXAMPLES</span></span>

### <span data-ttu-id="c915e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c915e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c915e-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="c915e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c915e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c915e-110">PARAMETERS</span></span>

### <span data-ttu-id="c915e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c915e-111">-Force</span></span>
<span data-ttu-id="c915e-112">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="c915e-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c915e-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c915e-113">-RouteFilter</span></span>
<span data-ttu-id="c915e-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c915e-114">The RouteFilter</span></span>

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

### <span data-ttu-id="c915e-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="c915e-115">-Confirm</span></span>
<span data-ttu-id="c915e-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c915e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c915e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c915e-117">-WhatIf</span></span>
<span data-ttu-id="c915e-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c915e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c915e-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c915e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c915e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c915e-120">-DefaultProfile</span></span>
<span data-ttu-id="c915e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c915e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c915e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c915e-122">CommonParameters</span></span>
<span data-ttu-id="c915e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c915e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c915e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c915e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c915e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c915e-125">INPUTS</span></span>

### <span data-ttu-id="c915e-126">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c915e-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c915e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c915e-127">OUTPUTS</span></span>

### <span data-ttu-id="c915e-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c915e-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c915e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c915e-129">NOTES</span></span>

## <span data-ttu-id="c915e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c915e-130">RELATED LINKS</span></span>

