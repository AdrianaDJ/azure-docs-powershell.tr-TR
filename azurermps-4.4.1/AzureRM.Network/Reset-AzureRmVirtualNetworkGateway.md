---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764267"
---
# <span data-ttu-id="8b2c3-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="8b2c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b2c3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b2c3-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b2c3-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b2c3-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b2c3-104">DESCRIPTION</span></span>

## <span data-ttu-id="8b2c3-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b2c3-105">EXAMPLES</span></span>

## <span data-ttu-id="8b2c3-106">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b2c3-106">PARAMETERS</span></span>

### <span data-ttu-id="8b2c3-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="8b2c3-107">-GatewayVip</span></span>
<span data-ttu-id="8b2c3-108">Ağ Geçidi VIP 'si (Active-Active özelliği etkin ağ geçitlerinde olduğu gibi). Varsayılan olarak, hiçbir değer geçirilmemişse ağ geçidi birincil örneği sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="8b2c3-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-109">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="8b2c3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2c3-110">-DefaultProfile</span></span>
<span data-ttu-id="8b2c3-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b2c3-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2c3-112">CommonParameters</span></span>
<span data-ttu-id="8b2c3-113">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2c3-114">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b2c3-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2c3-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b2c3-115">INPUTS</span></span>

### <span data-ttu-id="8b2c3-116">Dizisi</span><span class="sxs-lookup"><span data-stu-id="8b2c3-116">String</span></span>
<span data-ttu-id="8b2c3-117">' GatewayVip ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8b2c3-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8b2c3-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8b2c3-119">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8b2c3-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="8b2c3-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b2c3-120">OUTPUTS</span></span>

### <span data-ttu-id="8b2c3-121">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8b2c3-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b2c3-122">NOTES</span></span>

## <span data-ttu-id="8b2c3-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b2c3-123">RELATED LINKS</span></span>

[<span data-ttu-id="8b2c3-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8b2c3-125">Yeni-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8b2c3-126">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8b2c3-127">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8b2c3-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c3-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)

