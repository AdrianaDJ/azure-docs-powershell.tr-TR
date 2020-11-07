---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9a6879d2b5ad18c33ca53befd94d5e8dc03225df
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935389"
---
# <span data-ttu-id="e6b2f-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e6b2f-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e6b2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b2f-102">SYNOPSIS</span></span>

## <span data-ttu-id="e6b2f-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6b2f-103">SYNTAX</span></span>

### <span data-ttu-id="e6b2f-104">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e6b2f-104">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b2f-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e6b2f-105">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6b2f-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6b2f-106">DESCRIPTION</span></span>

## <span data-ttu-id="e6b2f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b2f-108">2</span><span class="sxs-lookup"><span data-stu-id="e6b2f-108">1:</span></span>
```

```

## <span data-ttu-id="e6b2f-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6b2f-109">PARAMETERS</span></span>

### <span data-ttu-id="e6b2f-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="e6b2f-110">-BackendPort</span></span>
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

### <span data-ttu-id="e6b2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b2f-111">-DefaultProfile</span></span>
<span data-ttu-id="e6b2f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6b2f-113">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="e6b2f-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="e6b2f-114">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="e6b2f-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="e6b2f-115">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="e6b2f-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="e6b2f-116">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="e6b2f-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="e6b2f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6b2f-117">-Name</span></span>
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

### <span data-ttu-id="e6b2f-118">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e6b2f-118">-Protocol</span></span>
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

### <span data-ttu-id="e6b2f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b2f-119">CommonParameters</span></span>
<span data-ttu-id="e6b2f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b2f-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b2f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b2f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6b2f-122">INPUTS</span></span>

## <span data-ttu-id="e6b2f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6b2f-123">OUTPUTS</span></span>

### <span data-ttu-id="e6b2f-124">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="e6b2f-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="e6b2f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6b2f-125">NOTES</span></span>

## <span data-ttu-id="e6b2f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6b2f-126">RELATED LINKS</span></span>

