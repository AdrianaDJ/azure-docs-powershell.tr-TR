---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 20837f96bc17d2cfd71abc359ff4114b44e6c062
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939120"
---
# <span data-ttu-id="cd0fa-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="cd0fa-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="cd0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd0fa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd0fa-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd0fa-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd0fa-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd0fa-104">DESCRIPTION</span></span>

## <span data-ttu-id="cd0fa-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd0fa-105">EXAMPLES</span></span>

### <span data-ttu-id="cd0fa-106">2</span><span class="sxs-lookup"><span data-stu-id="cd0fa-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="cd0fa-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd0fa-107">PARAMETERS</span></span>

### <span data-ttu-id="cd0fa-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0fa-108">-DefaultProfile</span></span>
<span data-ttu-id="cd0fa-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd0fa-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cd0fa-110">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0fa-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd0fa-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0fa-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0fa-112">CommonParameters</span></span>
<span data-ttu-id="cd0fa-113">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0fa-114">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0fa-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0fa-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd0fa-115">INPUTS</span></span>

### <span data-ttu-id="cd0fa-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cd0fa-116">PSLoadBalancer</span></span>
<span data-ttu-id="cd0fa-117">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cd0fa-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="cd0fa-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd0fa-118">OUTPUTS</span></span>

### <span data-ttu-id="cd0fa-119">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="cd0fa-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="cd0fa-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd0fa-120">NOTES</span></span>

## <span data-ttu-id="cd0fa-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd0fa-121">RELATED LINKS</span></span>
