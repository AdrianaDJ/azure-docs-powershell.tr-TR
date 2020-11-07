---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 2486dadb4d1987a2a3c341bc9f66270ec1338a1b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935293"
---
# <span data-ttu-id="d3a7c-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d3a7c-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d3a7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a7c-102">SYNOPSIS</span></span>

## <span data-ttu-id="d3a7c-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3a7c-103">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a7c-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3a7c-104">DESCRIPTION</span></span>

## <span data-ttu-id="d3a7c-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3a7c-105">EXAMPLES</span></span>

### <span data-ttu-id="d3a7c-106">2</span><span class="sxs-lookup"><span data-stu-id="d3a7c-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d3a7c-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3a7c-107">PARAMETERS</span></span>

### <span data-ttu-id="d3a7c-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a7c-108">-DefaultProfile</span></span>
<span data-ttu-id="d3a7c-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3a7c-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3a7c-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3a7c-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="d3a7c-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3a7c-111">-Name</span></span>
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

### <span data-ttu-id="d3a7c-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a7c-112">CommonParameters</span></span>
<span data-ttu-id="d3a7c-113">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3a7c-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a7c-114">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a7c-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a7c-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3a7c-115">INPUTS</span></span>

### <span data-ttu-id="d3a7c-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3a7c-116">PSLoadBalancer</span></span>
<span data-ttu-id="d3a7c-117">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d3a7c-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d3a7c-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3a7c-118">OUTPUTS</span></span>

### <span data-ttu-id="d3a7c-119">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3a7c-119">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d3a7c-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3a7c-120">NOTES</span></span>

## <span data-ttu-id="d3a7c-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3a7c-121">RELATED LINKS</span></span>

