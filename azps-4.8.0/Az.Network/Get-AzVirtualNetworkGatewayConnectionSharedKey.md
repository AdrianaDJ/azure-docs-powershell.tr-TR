---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266506"
---
# <span data-ttu-id="80fdc-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="80fdc-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="80fdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="80fdc-103">Bağlantı için kullanılan paylaşılan anahtarı görüntüler.</span><span class="sxs-lookup"><span data-stu-id="80fdc-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="80fdc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80fdc-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80fdc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="80fdc-106">Bağlantı için kullanılan paylaşılan anahtarı görüntüler.</span><span class="sxs-lookup"><span data-stu-id="80fdc-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="80fdc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80fdc-107">EXAMPLES</span></span>

### <span data-ttu-id="80fdc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="80fdc-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="80fdc-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80fdc-109">PARAMETERS</span></span>

### <span data-ttu-id="80fdc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fdc-110">-DefaultProfile</span></span>
<span data-ttu-id="80fdc-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80fdc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80fdc-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="80fdc-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80fdc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80fdc-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80fdc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fdc-114">CommonParameters</span></span>
<span data-ttu-id="80fdc-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80fdc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fdc-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="80fdc-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fdc-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80fdc-117">INPUTS</span></span>

### <span data-ttu-id="80fdc-118">System. String</span><span class="sxs-lookup"><span data-stu-id="80fdc-118">System.String</span></span>

## <span data-ttu-id="80fdc-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80fdc-119">OUTPUTS</span></span>

### <span data-ttu-id="80fdc-120">System. String</span><span class="sxs-lookup"><span data-stu-id="80fdc-120">System.String</span></span>

## <span data-ttu-id="80fdc-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80fdc-121">NOTES</span></span>

## <span data-ttu-id="80fdc-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80fdc-122">RELATED LINKS</span></span>

[<span data-ttu-id="80fdc-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="80fdc-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="80fdc-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="80fdc-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
