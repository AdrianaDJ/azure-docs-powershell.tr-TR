---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939073"
---
# <span data-ttu-id="af770-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="af770-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="af770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af770-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af770-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af770-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af770-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="af770-104">DESCRIPTION</span></span>

## <span data-ttu-id="af770-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af770-105">EXAMPLES</span></span>

### <span data-ttu-id="af770-106">2</span><span class="sxs-lookup"><span data-stu-id="af770-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="af770-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af770-107">PARAMETERS</span></span>

### <span data-ttu-id="af770-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af770-108">-DefaultProfile</span></span>
<span data-ttu-id="af770-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af770-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af770-110">-Ad</span><span class="sxs-lookup"><span data-stu-id="af770-110">-Name</span></span>
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

### <span data-ttu-id="af770-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af770-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="af770-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="af770-112">-Confirm</span></span>
<span data-ttu-id="af770-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af770-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af770-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af770-114">-WhatIf</span></span>
<span data-ttu-id="af770-115">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af770-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af770-116">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af770-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af770-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af770-117">CommonParameters</span></span>
<span data-ttu-id="af770-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af770-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af770-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af770-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af770-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af770-120">INPUTS</span></span>

### <span data-ttu-id="af770-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af770-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="af770-122">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="af770-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="af770-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af770-123">OUTPUTS</span></span>

### <span data-ttu-id="af770-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af770-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="af770-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af770-125">NOTES</span></span>

## <span data-ttu-id="af770-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af770-126">RELATED LINKS</span></span>

