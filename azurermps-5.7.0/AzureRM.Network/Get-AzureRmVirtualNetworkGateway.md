---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 29d5ad86d9df7bddec8be600d8b7c680c7bcd7fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588169"
---
# <span data-ttu-id="26fe3-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="26fe3-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="26fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="26fe3-103">Sanal ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="26fe3-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26fe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26fe3-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26fe3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="26fe3-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="26fe3-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="26fe3-107">**Get-AzureRmVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="26fe3-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="26fe3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26fe3-108">EXAMPLES</span></span>

### <span data-ttu-id="26fe3-109">1: sanal ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="26fe3-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="26fe3-110">Sanal ağ geçidinin "myRG" adlı sanal ağ geçidinin nesnesini, "myRG"</span><span class="sxs-lookup"><span data-stu-id="26fe3-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="26fe3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26fe3-111">PARAMETERS</span></span>

### <span data-ttu-id="26fe3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fe3-112">-DefaultProfile</span></span>
<span data-ttu-id="26fe3-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26fe3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26fe3-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="26fe3-114">-Name</span></span>
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

### <span data-ttu-id="26fe3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26fe3-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="26fe3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fe3-116">CommonParameters</span></span>
<span data-ttu-id="26fe3-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26fe3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fe3-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26fe3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fe3-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26fe3-119">INPUTS</span></span>

### <span data-ttu-id="26fe3-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="26fe3-120">None</span></span>
<span data-ttu-id="26fe3-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="26fe3-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26fe3-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26fe3-122">OUTPUTS</span></span>

### <span data-ttu-id="26fe3-123">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="26fe3-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="26fe3-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26fe3-124">NOTES</span></span>

## <span data-ttu-id="26fe3-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26fe3-125">RELATED LINKS</span></span>

