---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dbd49a948108d23c0f824adaea2e06105152a36b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591365"
---
# <span data-ttu-id="e7231-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e7231-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e7231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7231-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7231-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7231-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7231-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7231-104">DESCRIPTION</span></span>

## <span data-ttu-id="e7231-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7231-105">EXAMPLES</span></span>

### <span data-ttu-id="e7231-106">1: Get</span><span class="sxs-lookup"><span data-stu-id="e7231-106">1: Get</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzureRmLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="e7231-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7231-107">PARAMETERS</span></span>

### <span data-ttu-id="e7231-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7231-108">-DefaultProfile</span></span>
<span data-ttu-id="e7231-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7231-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7231-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7231-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="e7231-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7231-111">-Name</span></span>
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

### <span data-ttu-id="e7231-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7231-112">CommonParameters</span></span>
<span data-ttu-id="e7231-113">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7231-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7231-114">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7231-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7231-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7231-115">INPUTS</span></span>

### <span data-ttu-id="e7231-116">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7231-116">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="e7231-117">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7231-117">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="e7231-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7231-118">OUTPUTS</span></span>

### <span data-ttu-id="e7231-119">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="e7231-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="e7231-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7231-120">NOTES</span></span>

## <span data-ttu-id="e7231-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7231-121">RELATED LINKS</span></span>
