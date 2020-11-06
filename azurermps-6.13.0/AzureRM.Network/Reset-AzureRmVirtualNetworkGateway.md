---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593943"
---
# <span data-ttu-id="d06a5-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="d06a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d06a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d06a5-103">Sanal ağ geçidini sıfırlar</span><span class="sxs-lookup"><span data-stu-id="d06a5-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d06a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d06a5-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d06a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d06a5-105">DESCRIPTION</span></span>
<span data-ttu-id="d06a5-106">Sanal ağ geçidini sıfırlar</span><span class="sxs-lookup"><span data-stu-id="d06a5-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="d06a5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d06a5-107">EXAMPLES</span></span>

### <span data-ttu-id="d06a5-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="d06a5-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="d06a5-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d06a5-109">PARAMETERS</span></span>

### <span data-ttu-id="d06a5-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="d06a5-110">-AsJob</span></span>
<span data-ttu-id="d06a5-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d06a5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d06a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06a5-112">-DefaultProfile</span></span>
<span data-ttu-id="d06a5-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d06a5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d06a5-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="d06a5-114">-GatewayVip</span></span>
<span data-ttu-id="d06a5-115">Ağ Geçidi VIP 'si (Active-Active özelliği etkin ağ geçitlerinde olduğu gibi). Varsayılan olarak, hiçbir değer geçirilmemişse ağ geçidi birincil örneği sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="d06a5-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="d06a5-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="d06a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06a5-117">CommonParameters</span></span>
<span data-ttu-id="d06a5-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d06a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06a5-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06a5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06a5-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d06a5-120">INPUTS</span></span>

### <span data-ttu-id="d06a5-121">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="d06a5-122">Parametreler: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d06a5-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="d06a5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d06a5-123">System.String</span></span>
<span data-ttu-id="d06a5-124">Parametreler: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d06a5-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="d06a5-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d06a5-125">OUTPUTS</span></span>

### <span data-ttu-id="d06a5-126">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d06a5-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d06a5-127">NOTES</span></span>

## <span data-ttu-id="d06a5-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d06a5-128">RELATED LINKS</span></span>

[<span data-ttu-id="d06a5-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d06a5-130">Yeni-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d06a5-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d06a5-132">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d06a5-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d06a5-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


