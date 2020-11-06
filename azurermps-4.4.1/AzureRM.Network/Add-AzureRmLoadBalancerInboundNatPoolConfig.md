---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: e0999a5dc61574d600daf113e1641483c8a8bd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594233"
---
# <span data-ttu-id="8d08f-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8d08f-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="8d08f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d08f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d08f-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d08f-103">SYNTAX</span></span>

### <span data-ttu-id="8d08f-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8d08f-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d08f-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8d08f-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d08f-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d08f-106">DESCRIPTION</span></span>

## <span data-ttu-id="8d08f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d08f-107">EXAMPLES</span></span>

### <span data-ttu-id="8d08f-108">2</span><span class="sxs-lookup"><span data-stu-id="8d08f-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="8d08f-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d08f-109">PARAMETERS</span></span>

### <span data-ttu-id="8d08f-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="8d08f-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d08f-111">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="8d08f-111">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d08f-112">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="8d08f-112">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d08f-113">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="8d08f-113">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d08f-114">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="8d08f-114">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d08f-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d08f-115">-LoadBalancer</span></span>
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

### <span data-ttu-id="8d08f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d08f-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d08f-117">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="8d08f-117">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d08f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d08f-118">-DefaultProfile</span></span>
<span data-ttu-id="8d08f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d08f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d08f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d08f-120">CommonParameters</span></span>
<span data-ttu-id="8d08f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d08f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d08f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d08f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d08f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d08f-123">INPUTS</span></span>

### <span data-ttu-id="8d08f-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d08f-124">PSLoadBalancer</span></span>
<span data-ttu-id="8d08f-125">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8d08f-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8d08f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d08f-126">OUTPUTS</span></span>

### <span data-ttu-id="8d08f-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d08f-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8d08f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d08f-128">NOTES</span></span>

## <span data-ttu-id="8d08f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d08f-129">RELATED LINKS</span></span>

