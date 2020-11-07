---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 6be6c0d7993b44d807cad5bf8c06a203fe8ff7a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764165"
---
# <span data-ttu-id="47cee-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="47cee-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="47cee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47cee-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47cee-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47cee-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47cee-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="47cee-104">DESCRIPTION</span></span>

## <span data-ttu-id="47cee-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47cee-105">EXAMPLES</span></span>

### <span data-ttu-id="47cee-106">2</span><span class="sxs-lookup"><span data-stu-id="47cee-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="47cee-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47cee-107">PARAMETERS</span></span>

### <span data-ttu-id="47cee-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cee-108">-DefaultProfile</span></span>
<span data-ttu-id="47cee-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47cee-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47cee-110">-Ad</span><span class="sxs-lookup"><span data-stu-id="47cee-110">-Name</span></span>
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

### <span data-ttu-id="47cee-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47cee-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="47cee-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="47cee-112">-Confirm</span></span>
<span data-ttu-id="47cee-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47cee-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47cee-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47cee-114">-WhatIf</span></span>
<span data-ttu-id="47cee-115">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47cee-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47cee-116">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47cee-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47cee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cee-117">CommonParameters</span></span>
<span data-ttu-id="47cee-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47cee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cee-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47cee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cee-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47cee-120">INPUTS</span></span>

### <span data-ttu-id="47cee-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47cee-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="47cee-122">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="47cee-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="47cee-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47cee-123">OUTPUTS</span></span>

### <span data-ttu-id="47cee-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47cee-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="47cee-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47cee-125">NOTES</span></span>

## <span data-ttu-id="47cee-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47cee-126">RELATED LINKS</span></span>

