---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940026"
---
# <span data-ttu-id="3be2a-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="3be2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3be2a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3be2a-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3be2a-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3be2a-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="3be2a-104">DESCRIPTION</span></span>

## <span data-ttu-id="3be2a-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3be2a-105">EXAMPLES</span></span>

### <span data-ttu-id="3be2a-106">2</span><span class="sxs-lookup"><span data-stu-id="3be2a-106">1:</span></span>
```

```

## <span data-ttu-id="3be2a-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3be2a-107">PARAMETERS</span></span>

### <span data-ttu-id="3be2a-108">-Iş</span><span class="sxs-lookup"><span data-stu-id="3be2a-108">-AsJob</span></span>
<span data-ttu-id="3be2a-109">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3be2a-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be2a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be2a-110">-DefaultProfile</span></span>
<span data-ttu-id="3be2a-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3be2a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3be2a-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="3be2a-112">-GatewayVip</span></span>
<span data-ttu-id="3be2a-113">Ağ Geçidi VIP 'si (Active-Active özelliği etkin ağ geçitlerinde olduğu gibi). Varsayılan olarak, hiçbir değer geçirilmemişse ağ geçidi birincil örneği sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="3be2a-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be2a-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="3be2a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be2a-115">CommonParameters</span></span>
<span data-ttu-id="3be2a-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3be2a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be2a-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be2a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be2a-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3be2a-118">INPUTS</span></span>

### <span data-ttu-id="3be2a-119">Dizisi</span><span class="sxs-lookup"><span data-stu-id="3be2a-119">String</span></span>
<span data-ttu-id="3be2a-120">' GatewayVip ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3be2a-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="3be2a-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3be2a-122">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3be2a-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="3be2a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3be2a-123">OUTPUTS</span></span>

### <span data-ttu-id="3be2a-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3be2a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3be2a-125">NOTES</span></span>

## <span data-ttu-id="3be2a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3be2a-126">RELATED LINKS</span></span>

[<span data-ttu-id="3be2a-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3be2a-128">Yeni-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3be2a-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3be2a-130">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3be2a-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be2a-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


