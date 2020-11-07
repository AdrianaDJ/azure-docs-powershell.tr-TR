---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9f9e14b94cbe38ba643d2c39beca5e1fe52138b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763105"
---
# <span data-ttu-id="f547c-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f547c-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="f547c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f547c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f547c-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f547c-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f547c-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="f547c-104">DESCRIPTION</span></span>

## <span data-ttu-id="f547c-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f547c-105">EXAMPLES</span></span>

### <span data-ttu-id="f547c-106">2</span><span class="sxs-lookup"><span data-stu-id="f547c-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f547c-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f547c-107">PARAMETERS</span></span>

### <span data-ttu-id="f547c-108">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f547c-108">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f547c-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="f547c-109">-Name</span></span>
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

### <span data-ttu-id="f547c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f547c-110">-DefaultProfile</span></span>
<span data-ttu-id="f547c-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f547c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f547c-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f547c-112">CommonParameters</span></span>
<span data-ttu-id="f547c-113">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f547c-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f547c-114">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f547c-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f547c-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f547c-115">INPUTS</span></span>

### <span data-ttu-id="f547c-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f547c-116">PSLoadBalancer</span></span>
<span data-ttu-id="f547c-117">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f547c-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f547c-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f547c-118">OUTPUTS</span></span>

### <span data-ttu-id="f547c-119">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="f547c-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="f547c-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f547c-120">NOTES</span></span>

## <span data-ttu-id="f547c-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f547c-121">RELATED LINKS</span></span>

