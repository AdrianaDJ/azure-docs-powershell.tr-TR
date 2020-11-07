---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf99aba02bc4dee18ec6cfd2bdaf9fd83036e6d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936540"
---
# <span data-ttu-id="f3068-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3068-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="f3068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3068-102">SYNOPSIS</span></span>

## <span data-ttu-id="f3068-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3068-103">SYNTAX</span></span>

### <span data-ttu-id="f3068-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f3068-104">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3068-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f3068-105">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3068-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3068-106">DESCRIPTION</span></span>

## <span data-ttu-id="f3068-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3068-107">EXAMPLES</span></span>

### <span data-ttu-id="f3068-108">2</span><span class="sxs-lookup"><span data-stu-id="f3068-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f3068-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3068-109">PARAMETERS</span></span>

### <span data-ttu-id="f3068-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="f3068-110">-BackendPort</span></span>
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

### <span data-ttu-id="f3068-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3068-111">-DefaultProfile</span></span>
<span data-ttu-id="f3068-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3068-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3068-113">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="f3068-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="f3068-114">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="f3068-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="f3068-115">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="f3068-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="f3068-116">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="f3068-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="f3068-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3068-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="f3068-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3068-118">-Name</span></span>
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

### <span data-ttu-id="f3068-119">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="f3068-119">-Protocol</span></span>
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

### <span data-ttu-id="f3068-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3068-120">CommonParameters</span></span>
<span data-ttu-id="f3068-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3068-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3068-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3068-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3068-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3068-123">INPUTS</span></span>

### <span data-ttu-id="f3068-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3068-124">PSLoadBalancer</span></span>
<span data-ttu-id="f3068-125">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f3068-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f3068-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3068-126">OUTPUTS</span></span>

### <span data-ttu-id="f3068-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3068-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f3068-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3068-128">NOTES</span></span>

## <span data-ttu-id="f3068-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3068-129">RELATED LINKS</span></span>

[<span data-ttu-id="f3068-130">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3068-130">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f3068-131">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3068-131">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f3068-132">Yeni-Azloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="f3068-132">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f3068-133">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3068-133">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)


