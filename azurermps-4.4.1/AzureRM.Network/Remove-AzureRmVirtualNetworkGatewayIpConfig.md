---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d721feb80598e343fc5757eceee90136bbc51ae9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595000"
---
# <span data-ttu-id="143c8-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="143c8-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="143c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="143c8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="143c8-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="143c8-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="143c8-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="143c8-104">DESCRIPTION</span></span>

## <span data-ttu-id="143c8-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="143c8-105">EXAMPLES</span></span>

### <span data-ttu-id="143c8-106">2</span><span class="sxs-lookup"><span data-stu-id="143c8-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="143c8-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="143c8-107">PARAMETERS</span></span>

### <span data-ttu-id="143c8-108">-Ad</span><span class="sxs-lookup"><span data-stu-id="143c8-108">-Name</span></span>
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

### <span data-ttu-id="143c8-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="143c8-109">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="143c8-110">-Onay</span><span class="sxs-lookup"><span data-stu-id="143c8-110">-Confirm</span></span>
<span data-ttu-id="143c8-111">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="143c8-111">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c8-112">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="143c8-112">-WhatIf</span></span>
<span data-ttu-id="143c8-113">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="143c8-113">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="143c8-114">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="143c8-114">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143c8-115">-DefaultProfile</span></span>
<span data-ttu-id="143c8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="143c8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="143c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143c8-117">CommonParameters</span></span>
<span data-ttu-id="143c8-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="143c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143c8-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="143c8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143c8-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="143c8-120">INPUTS</span></span>

### <span data-ttu-id="143c8-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="143c8-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="143c8-122">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="143c8-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="143c8-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="143c8-123">OUTPUTS</span></span>

### <span data-ttu-id="143c8-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="143c8-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="143c8-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="143c8-125">NOTES</span></span>

## <span data-ttu-id="143c8-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="143c8-126">RELATED LINKS</span></span>

