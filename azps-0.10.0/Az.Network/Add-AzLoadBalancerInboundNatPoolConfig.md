---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a5cd44d1b4b7ac1a1494047affa721dd21d85919
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935637"
---
# <span data-ttu-id="240c5-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="240c5-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="240c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="240c5-102">SYNOPSIS</span></span>

## <span data-ttu-id="240c5-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="240c5-103">SYNTAX</span></span>

### <span data-ttu-id="240c5-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="240c5-104">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="240c5-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="240c5-105">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="240c5-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="240c5-106">DESCRIPTION</span></span>

## <span data-ttu-id="240c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="240c5-107">EXAMPLES</span></span>

### <span data-ttu-id="240c5-108">2</span><span class="sxs-lookup"><span data-stu-id="240c5-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="240c5-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="240c5-109">PARAMETERS</span></span>

### <span data-ttu-id="240c5-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="240c5-110">-BackendPort</span></span>
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

### <span data-ttu-id="240c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240c5-111">-DefaultProfile</span></span>
<span data-ttu-id="240c5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="240c5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="240c5-113">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="240c5-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="240c5-114">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="240c5-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="240c5-115">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="240c5-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="240c5-116">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="240c5-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="240c5-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="240c5-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="240c5-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="240c5-118">-Name</span></span>
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

### <span data-ttu-id="240c5-119">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="240c5-119">-Protocol</span></span>
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

### <span data-ttu-id="240c5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240c5-120">CommonParameters</span></span>
<span data-ttu-id="240c5-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="240c5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240c5-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240c5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240c5-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="240c5-123">INPUTS</span></span>

### <span data-ttu-id="240c5-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="240c5-124">PSLoadBalancer</span></span>
<span data-ttu-id="240c5-125">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="240c5-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="240c5-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="240c5-126">OUTPUTS</span></span>

### <span data-ttu-id="240c5-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="240c5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="240c5-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="240c5-128">NOTES</span></span>

## <span data-ttu-id="240c5-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="240c5-129">RELATED LINKS</span></span>

