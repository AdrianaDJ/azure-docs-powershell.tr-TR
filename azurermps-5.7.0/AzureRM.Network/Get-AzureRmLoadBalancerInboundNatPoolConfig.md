---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: f2fd08abbc9a01f1a6cacb9891d82fe1c89d13ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594939"
---
# <span data-ttu-id="2a37f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2a37f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="2a37f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a37f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a37f-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a37f-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a37f-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a37f-104">DESCRIPTION</span></span>

## <span data-ttu-id="2a37f-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a37f-105">EXAMPLES</span></span>

### <span data-ttu-id="2a37f-106">2</span><span class="sxs-lookup"><span data-stu-id="2a37f-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2a37f-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a37f-107">PARAMETERS</span></span>

### <span data-ttu-id="2a37f-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a37f-108">-DefaultProfile</span></span>
<span data-ttu-id="2a37f-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a37f-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a37f-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a37f-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="2a37f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a37f-111">-Name</span></span>
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

### <span data-ttu-id="2a37f-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a37f-112">CommonParameters</span></span>
<span data-ttu-id="2a37f-113">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a37f-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a37f-114">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a37f-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a37f-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a37f-115">INPUTS</span></span>

### <span data-ttu-id="2a37f-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a37f-116">PSLoadBalancer</span></span>
<span data-ttu-id="2a37f-117">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2a37f-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2a37f-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a37f-118">OUTPUTS</span></span>

### <span data-ttu-id="2a37f-119">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="2a37f-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="2a37f-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a37f-120">NOTES</span></span>

## <span data-ttu-id="2a37f-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a37f-121">RELATED LINKS</span></span>

