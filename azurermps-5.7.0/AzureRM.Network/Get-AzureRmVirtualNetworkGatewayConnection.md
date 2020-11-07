---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b4a6ae7db1221a2dee8a0bd5343ad78ed88a0abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762732"
---
# <span data-ttu-id="920bf-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="920bf-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="920bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="920bf-102">SYNOPSIS</span></span>
<span data-ttu-id="920bf-103">Sanal ağ geçidi bağlantısını alır</span><span class="sxs-lookup"><span data-stu-id="920bf-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="920bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="920bf-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="920bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="920bf-105">DESCRIPTION</span></span>
<span data-ttu-id="920bf-106">Sanal ağ geçidi bağlantısı, Azure 'daki sanal ağ geçidine bağlı olan IPSec tüneli (siteden siteye veya VNET arası) temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="920bf-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="920bf-107">**Get-AzureRmVirtualNetworkGatewayConnection** cmdlet 'i ad ve kaynak grubu adına dayalı olarak bağlantınızın nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="920bf-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="920bf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="920bf-108">EXAMPLES</span></span>

### <span data-ttu-id="920bf-109">1: sanal ağ geçidi bağlantısı edinin</span><span class="sxs-lookup"><span data-stu-id="920bf-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="920bf-110">Sanal Ağ Geçidi bağlantısının "myTunnel" adlı sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="920bf-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="920bf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="920bf-111">PARAMETERS</span></span>

### <span data-ttu-id="920bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920bf-112">-DefaultProfile</span></span>
<span data-ttu-id="920bf-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="920bf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="920bf-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="920bf-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="920bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="920bf-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="920bf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920bf-116">CommonParameters</span></span>
<span data-ttu-id="920bf-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="920bf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920bf-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="920bf-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920bf-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="920bf-119">INPUTS</span></span>

### <span data-ttu-id="920bf-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="920bf-120">None</span></span>
<span data-ttu-id="920bf-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="920bf-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="920bf-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="920bf-122">OUTPUTS</span></span>

### <span data-ttu-id="920bf-123">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="920bf-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="920bf-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="920bf-124">NOTES</span></span>

## <span data-ttu-id="920bf-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="920bf-125">RELATED LINKS</span></span>

