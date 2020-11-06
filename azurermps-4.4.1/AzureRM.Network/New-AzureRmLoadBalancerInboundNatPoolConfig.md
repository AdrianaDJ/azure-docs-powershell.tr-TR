---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 85d58154d8dd1d93e37a55b9fd0b9d306283b899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594221"
---
# <span data-ttu-id="36750-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="36750-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="36750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36750-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36750-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36750-103">SYNTAX</span></span>

### <span data-ttu-id="36750-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="36750-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36750-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="36750-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36750-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="36750-106">DESCRIPTION</span></span>

## <span data-ttu-id="36750-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36750-107">EXAMPLES</span></span>

## <span data-ttu-id="36750-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36750-108">PARAMETERS</span></span>

### <span data-ttu-id="36750-109">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="36750-109">-BackendPort</span></span>
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

### <span data-ttu-id="36750-110">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="36750-110">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="36750-111">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="36750-111">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="36750-112">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="36750-112">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="36750-113">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="36750-113">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="36750-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="36750-114">-Name</span></span>
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

### <span data-ttu-id="36750-115">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="36750-115">-Protocol</span></span>
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

### <span data-ttu-id="36750-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36750-116">-DefaultProfile</span></span>
<span data-ttu-id="36750-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36750-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36750-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36750-118">CommonParameters</span></span>
<span data-ttu-id="36750-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36750-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36750-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36750-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36750-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36750-121">INPUTS</span></span>

## <span data-ttu-id="36750-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36750-122">OUTPUTS</span></span>

### <span data-ttu-id="36750-123">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="36750-123">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="36750-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36750-124">NOTES</span></span>

## <span data-ttu-id="36750-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36750-125">RELATED LINKS</span></span>

