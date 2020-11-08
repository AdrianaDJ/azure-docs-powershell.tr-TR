---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109437"
---
# <span data-ttu-id="64c94-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="64c94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c94-102">SYNOPSIS</span></span>
<span data-ttu-id="64c94-103">Sanal ağ geçidini sıfırlar</span><span class="sxs-lookup"><span data-stu-id="64c94-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="64c94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64c94-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64c94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64c94-105">DESCRIPTION</span></span>
<span data-ttu-id="64c94-106">Sanal ağ geçidini sıfırlar</span><span class="sxs-lookup"><span data-stu-id="64c94-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="64c94-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64c94-107">EXAMPLES</span></span>

### <span data-ttu-id="64c94-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="64c94-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="64c94-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64c94-109">PARAMETERS</span></span>

### <span data-ttu-id="64c94-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="64c94-110">-AsJob</span></span>
<span data-ttu-id="64c94-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="64c94-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c94-112">-DefaultProfile</span></span>
<span data-ttu-id="64c94-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64c94-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c94-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="64c94-114">-GatewayVip</span></span>
<span data-ttu-id="64c94-115">Ağ Geçidi VIP 'si (Active-Active özelliği etkin ağ geçitlerinde olduğu gibi). Varsayılan olarak, hiçbir değer geçirilmemişse ağ geçidi birincil örneği sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="64c94-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c94-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-116">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c94-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c94-117">CommonParameters</span></span>
<span data-ttu-id="64c94-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64c94-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c94-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c94-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c94-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64c94-120">INPUTS</span></span>

### <span data-ttu-id="64c94-121">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="64c94-122">System. String</span><span class="sxs-lookup"><span data-stu-id="64c94-122">System.String</span></span>

## <span data-ttu-id="64c94-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64c94-123">OUTPUTS</span></span>

### <span data-ttu-id="64c94-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="64c94-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64c94-125">NOTES</span></span>

## <span data-ttu-id="64c94-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64c94-126">RELATED LINKS</span></span>

[<span data-ttu-id="64c94-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="64c94-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="64c94-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="64c94-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="64c94-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64c94-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
