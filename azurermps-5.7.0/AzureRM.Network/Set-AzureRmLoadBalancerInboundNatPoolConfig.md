---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: d893ec451c99bded8320e5949d052aeb856a5d56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588875"
---
# <span data-ttu-id="24b73-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="24b73-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="24b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b73-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24b73-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24b73-103">SYNTAX</span></span>

### <span data-ttu-id="24b73-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="24b73-104">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24b73-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24b73-105">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24b73-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="24b73-106">DESCRIPTION</span></span>

## <span data-ttu-id="24b73-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24b73-107">EXAMPLES</span></span>

### <span data-ttu-id="24b73-108">2</span><span class="sxs-lookup"><span data-stu-id="24b73-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="24b73-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24b73-109">PARAMETERS</span></span>

### <span data-ttu-id="24b73-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="24b73-110">-BackendPort</span></span>
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

### <span data-ttu-id="24b73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b73-111">-DefaultProfile</span></span>
<span data-ttu-id="24b73-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24b73-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24b73-113">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="24b73-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="24b73-114">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="24b73-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="24b73-115">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="24b73-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="24b73-116">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="24b73-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="24b73-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="24b73-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="24b73-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="24b73-118">-Name</span></span>
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

### <span data-ttu-id="24b73-119">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="24b73-119">-Protocol</span></span>
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

### <span data-ttu-id="24b73-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b73-120">CommonParameters</span></span>
<span data-ttu-id="24b73-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24b73-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b73-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b73-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b73-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24b73-123">INPUTS</span></span>

### <span data-ttu-id="24b73-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="24b73-124">PSLoadBalancer</span></span>
<span data-ttu-id="24b73-125">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="24b73-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="24b73-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24b73-126">OUTPUTS</span></span>

### <span data-ttu-id="24b73-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="24b73-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="24b73-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24b73-128">NOTES</span></span>

## <span data-ttu-id="24b73-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24b73-129">RELATED LINKS</span></span>

[<span data-ttu-id="24b73-130">Add-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="24b73-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="24b73-131">Get-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="24b73-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="24b73-132">Yeni-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="24b73-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="24b73-133">Remove-Azurermloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="24b73-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


