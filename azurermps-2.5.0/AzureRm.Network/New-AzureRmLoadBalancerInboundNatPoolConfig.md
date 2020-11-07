---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 247470ee878a37968cd690d27f8e5e16047febbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939286"
---
# <span data-ttu-id="d85b1-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d85b1-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d85b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85b1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d85b1-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d85b1-103">SYNTAX</span></span>

### <span data-ttu-id="d85b1-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d85b1-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d85b1-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d85b1-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d85b1-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d85b1-106">DESCRIPTION</span></span>

## <span data-ttu-id="d85b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d85b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d85b1-108">2</span><span class="sxs-lookup"><span data-stu-id="d85b1-108">1:</span></span>
```

```

## <span data-ttu-id="d85b1-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d85b1-109">PARAMETERS</span></span>

### <span data-ttu-id="d85b1-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="d85b1-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85b1-111">-DefaultProfile</span></span>
<span data-ttu-id="d85b1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d85b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d85b1-113">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="d85b1-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b1-114">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="d85b1-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b1-115">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="d85b1-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b1-116">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="d85b1-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d85b1-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b1-118">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d85b1-118">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85b1-119">CommonParameters</span></span>
<span data-ttu-id="d85b1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d85b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85b1-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d85b1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85b1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d85b1-122">INPUTS</span></span>

## <span data-ttu-id="d85b1-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d85b1-123">OUTPUTS</span></span>

### <span data-ttu-id="d85b1-124">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="d85b1-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="d85b1-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d85b1-125">NOTES</span></span>

## <span data-ttu-id="d85b1-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d85b1-126">RELATED LINKS</span></span>

