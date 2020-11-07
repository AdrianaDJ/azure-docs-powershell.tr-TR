---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 815f7d3fdc0f058f2abfce5687b129054814adab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764424"
---
# <span data-ttu-id="ec450-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="ec450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec450-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec450-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec450-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec450-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec450-104">DESCRIPTION</span></span>

## <span data-ttu-id="ec450-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec450-105">EXAMPLES</span></span>

## <span data-ttu-id="ec450-106">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec450-106">PARAMETERS</span></span>

### <span data-ttu-id="ec450-107">-Iş</span><span class="sxs-lookup"><span data-stu-id="ec450-107">-AsJob</span></span>
<span data-ttu-id="ec450-108">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ec450-108">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec450-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec450-109">-DefaultProfile</span></span>
<span data-ttu-id="ec450-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec450-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec450-111">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="ec450-111">-GatewayVip</span></span>
<span data-ttu-id="ec450-112">Ağ Geçidi VIP 'si (Active-Active özelliği etkin ağ geçitlerinde olduğu gibi). Varsayılan olarak, hiçbir değer geçirilmemişse ağ geçidi birincil örneği sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="ec450-112">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="ec450-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="ec450-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec450-114">CommonParameters</span></span>
<span data-ttu-id="ec450-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec450-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec450-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec450-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec450-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec450-117">INPUTS</span></span>

### <span data-ttu-id="ec450-118">Dizisi</span><span class="sxs-lookup"><span data-stu-id="ec450-118">String</span></span>
<span data-ttu-id="ec450-119">' GatewayVip ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ec450-119">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ec450-120">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-120">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ec450-121">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ec450-121">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="ec450-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec450-122">OUTPUTS</span></span>

### <span data-ttu-id="ec450-123">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ec450-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec450-124">NOTES</span></span>

## <span data-ttu-id="ec450-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec450-125">RELATED LINKS</span></span>

[<span data-ttu-id="ec450-126">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-126">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ec450-127">Yeni-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-127">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ec450-128">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-128">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ec450-129">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-129">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ec450-130">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec450-130">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


