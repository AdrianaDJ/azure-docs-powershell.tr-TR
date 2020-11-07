---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936587"
---
# <span data-ttu-id="1cf92-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="1cf92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cf92-102">SYNOPSIS</span></span>

## <span data-ttu-id="1cf92-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cf92-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cf92-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cf92-104">DESCRIPTION</span></span>

## <span data-ttu-id="1cf92-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cf92-105">EXAMPLES</span></span>

### <span data-ttu-id="1cf92-106">2</span><span class="sxs-lookup"><span data-stu-id="1cf92-106">1:</span></span>
```

```

## <span data-ttu-id="1cf92-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cf92-107">PARAMETERS</span></span>

### <span data-ttu-id="1cf92-108">-Iş</span><span class="sxs-lookup"><span data-stu-id="1cf92-108">-AsJob</span></span>
<span data-ttu-id="1cf92-109">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1cf92-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cf92-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf92-110">-DefaultProfile</span></span>
<span data-ttu-id="1cf92-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1cf92-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cf92-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="1cf92-112">-GatewayVip</span></span>
<span data-ttu-id="1cf92-113">Ağ Geçidi VIP 'si (Active-Active özelliği etkin ağ geçitlerinde olduğu gibi). Varsayılan olarak, hiçbir değer geçirilmemişse ağ geçidi birincil örneği sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="1cf92-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="1cf92-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="1cf92-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf92-115">CommonParameters</span></span>
<span data-ttu-id="1cf92-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1cf92-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf92-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf92-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf92-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cf92-118">INPUTS</span></span>

### <span data-ttu-id="1cf92-119">Dizisi</span><span class="sxs-lookup"><span data-stu-id="1cf92-119">String</span></span>
<span data-ttu-id="1cf92-120">' GatewayVip ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1cf92-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="1cf92-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="1cf92-122">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1cf92-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="1cf92-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cf92-123">OUTPUTS</span></span>

### <span data-ttu-id="1cf92-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1cf92-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cf92-125">NOTES</span></span>

## <span data-ttu-id="1cf92-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cf92-126">RELATED LINKS</span></span>

[<span data-ttu-id="1cf92-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1cf92-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1cf92-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1cf92-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1cf92-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cf92-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


