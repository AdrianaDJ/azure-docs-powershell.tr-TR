---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936595"
---
# <span data-ttu-id="4de79-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4de79-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="4de79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de79-102">SYNOPSIS</span></span>

## <span data-ttu-id="4de79-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4de79-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de79-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="4de79-104">DESCRIPTION</span></span>

## <span data-ttu-id="4de79-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4de79-105">EXAMPLES</span></span>

### <span data-ttu-id="4de79-106">2</span><span class="sxs-lookup"><span data-stu-id="4de79-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="4de79-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4de79-107">PARAMETERS</span></span>

### <span data-ttu-id="4de79-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de79-108">-DefaultProfile</span></span>
<span data-ttu-id="4de79-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4de79-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de79-110">-Ad</span><span class="sxs-lookup"><span data-stu-id="4de79-110">-Name</span></span>
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

### <span data-ttu-id="4de79-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4de79-111">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4de79-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="4de79-112">-Confirm</span></span>
<span data-ttu-id="4de79-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4de79-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de79-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de79-114">-WhatIf</span></span>
<span data-ttu-id="4de79-115">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4de79-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de79-116">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4de79-116">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de79-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de79-117">CommonParameters</span></span>
<span data-ttu-id="4de79-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4de79-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de79-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de79-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de79-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4de79-120">INPUTS</span></span>

### <span data-ttu-id="4de79-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4de79-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="4de79-122">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4de79-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="4de79-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4de79-123">OUTPUTS</span></span>

### <span data-ttu-id="4de79-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4de79-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4de79-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4de79-125">NOTES</span></span>

## <span data-ttu-id="4de79-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4de79-126">RELATED LINKS</span></span>

