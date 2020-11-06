---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 875a42742c153bf6a1fad8e2ae1ad2b0e025c833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592070"
---
# <span data-ttu-id="61f06-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="61f06-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="61f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f06-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f06-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61f06-103">SYNTAX</span></span>

### <span data-ttu-id="61f06-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="61f06-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f06-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="61f06-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61f06-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="61f06-106">DESCRIPTION</span></span>

## <span data-ttu-id="61f06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61f06-107">EXAMPLES</span></span>

## <span data-ttu-id="61f06-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61f06-108">PARAMETERS</span></span>

### <span data-ttu-id="61f06-109">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="61f06-109">-BackendPort</span></span>
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

### <span data-ttu-id="61f06-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f06-110">-DefaultProfile</span></span>
<span data-ttu-id="61f06-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61f06-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f06-112">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="61f06-112">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="61f06-113">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="61f06-113">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="61f06-114">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="61f06-114">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="61f06-115">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="61f06-115">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="61f06-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="61f06-116">-Name</span></span>
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

### <span data-ttu-id="61f06-117">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="61f06-117">-Protocol</span></span>
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

### <span data-ttu-id="61f06-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f06-118">CommonParameters</span></span>
<span data-ttu-id="61f06-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61f06-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f06-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f06-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f06-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61f06-121">INPUTS</span></span>

### <span data-ttu-id="61f06-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="61f06-122">None</span></span>
<span data-ttu-id="61f06-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="61f06-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61f06-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61f06-124">OUTPUTS</span></span>

### <span data-ttu-id="61f06-125">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="61f06-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="61f06-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61f06-126">NOTES</span></span>

## <span data-ttu-id="61f06-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61f06-127">RELATED LINKS</span></span>

