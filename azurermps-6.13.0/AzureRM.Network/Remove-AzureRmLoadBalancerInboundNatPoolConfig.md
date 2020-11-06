---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572733"
---
# <span data-ttu-id="d4e0f-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d4e0f-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d4e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e0f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e0f-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4e0f-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e0f-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4e0f-104">DESCRIPTION</span></span>

## <span data-ttu-id="d4e0f-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4e0f-105">EXAMPLES</span></span>

### <span data-ttu-id="d4e0f-106">1: kaldırma</span><span class="sxs-lookup"><span data-stu-id="d4e0f-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="d4e0f-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4e0f-107">PARAMETERS</span></span>

### <span data-ttu-id="d4e0f-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e0f-108">-DefaultProfile</span></span>
<span data-ttu-id="d4e0f-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4e0f-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d4e0f-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4e0f-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0f-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4e0f-112">-Confirm</span></span>
<span data-ttu-id="d4e0f-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e0f-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e0f-114">-WhatIf</span></span>
<span data-ttu-id="d4e0f-115">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4e0f-116">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e0f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e0f-117">CommonParameters</span></span>
<span data-ttu-id="d4e0f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e0f-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e0f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e0f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4e0f-120">INPUTS</span></span>

### <span data-ttu-id="d4e0f-121">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d4e0f-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="d4e0f-122">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4e0f-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="d4e0f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4e0f-123">OUTPUTS</span></span>

### <span data-ttu-id="d4e0f-124">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d4e0f-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d4e0f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4e0f-125">NOTES</span></span>

## <span data-ttu-id="d4e0f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4e0f-126">RELATED LINKS</span></span>
