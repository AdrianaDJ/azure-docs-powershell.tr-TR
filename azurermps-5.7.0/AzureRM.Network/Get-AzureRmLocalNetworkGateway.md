---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594935"
---
# <span data-ttu-id="0febe-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0febe-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="0febe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0febe-102">SYNOPSIS</span></span>
<span data-ttu-id="0febe-103">Yerel ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="0febe-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0febe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0febe-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0febe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0febe-105">DESCRIPTION</span></span>
<span data-ttu-id="0febe-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="0febe-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="0febe-107">**Get-AzureRmLocalNetworkGateway** cmdlet 'i, şirket içi ağ geçidinizi temsil eden nesneyi ad ve kaynak grubu adına göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="0febe-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="0febe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0febe-108">EXAMPLES</span></span>

### <span data-ttu-id="0febe-109">1: yerel ağ ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="0febe-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="0febe-110">Yerel ağ geçidinin "myLocalGW" adlı yerel ağ geçidinin nesnesini, "myRG" kaynak grubunda döndürür</span><span class="sxs-lookup"><span data-stu-id="0febe-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="0febe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0febe-111">PARAMETERS</span></span>

### <span data-ttu-id="0febe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0febe-112">-DefaultProfile</span></span>
<span data-ttu-id="0febe-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0febe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0febe-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="0febe-114">-Name</span></span>
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

### <span data-ttu-id="0febe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0febe-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0febe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0febe-116">CommonParameters</span></span>
<span data-ttu-id="0febe-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0febe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0febe-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0febe-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0febe-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0febe-119">INPUTS</span></span>

### <span data-ttu-id="0febe-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0febe-120">None</span></span>
<span data-ttu-id="0febe-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0febe-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0febe-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0febe-122">OUTPUTS</span></span>

### <span data-ttu-id="0febe-123">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0febe-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="0febe-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0febe-124">NOTES</span></span>

## <span data-ttu-id="0febe-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0febe-125">RELATED LINKS</span></span>

