---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 6f4981469bf9468de7fd05ec79b1d3d2b28daa93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939887"
---
# <span data-ttu-id="d884c-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d884c-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d884c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d884c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d884c-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d884c-103">SYNTAX</span></span>

### <span data-ttu-id="d884c-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d884c-104">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d884c-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d884c-105">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d884c-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d884c-106">DESCRIPTION</span></span>

## <span data-ttu-id="d884c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d884c-107">EXAMPLES</span></span>

### <span data-ttu-id="d884c-108">2</span><span class="sxs-lookup"><span data-stu-id="d884c-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d884c-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d884c-109">PARAMETERS</span></span>

### <span data-ttu-id="d884c-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="d884c-110">-BackendPort</span></span>
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

### <span data-ttu-id="d884c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d884c-111">-DefaultProfile</span></span>
<span data-ttu-id="d884c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d884c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d884c-113">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="d884c-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="d884c-114">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="d884c-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="d884c-115">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="d884c-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="d884c-116">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="d884c-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="d884c-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d884c-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="d884c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d884c-118">-Name</span></span>
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

### <span data-ttu-id="d884c-119">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d884c-119">-Protocol</span></span>
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

### <span data-ttu-id="d884c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d884c-120">CommonParameters</span></span>
<span data-ttu-id="d884c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d884c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d884c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d884c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d884c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d884c-123">INPUTS</span></span>

### <span data-ttu-id="d884c-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d884c-124">PSLoadBalancer</span></span>
<span data-ttu-id="d884c-125">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d884c-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d884c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d884c-126">OUTPUTS</span></span>

### <span data-ttu-id="d884c-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d884c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d884c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d884c-128">NOTES</span></span>

## <span data-ttu-id="d884c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d884c-129">RELATED LINKS</span></span>

[<span data-ttu-id="d884c-130">Add-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="d884c-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d884c-131">Get-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="d884c-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d884c-132">Yeni-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="d884c-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d884c-133">Remove-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="d884c-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


