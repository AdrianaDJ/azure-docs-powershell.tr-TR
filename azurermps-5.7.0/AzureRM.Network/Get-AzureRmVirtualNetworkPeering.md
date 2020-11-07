---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 0c68886906957204ee0885a00bfc07740fb6ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762632"
---
# <span data-ttu-id="05496-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="05496-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="05496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05496-102">SYNOPSIS</span></span>
<span data-ttu-id="05496-103">Sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="05496-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05496-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05496-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05496-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05496-105">DESCRIPTION</span></span>
<span data-ttu-id="05496-106">**Get-Azurermvirtualnetworkeşleme** cmdlet 'i sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="05496-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="05496-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05496-107">EXAMPLES</span></span>

### <span data-ttu-id="05496-108">Örnek 1: iki sanal ağ arasındaki eşlemeyi alma</span><span class="sxs-lookup"><span data-stu-id="05496-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="05496-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05496-109">PARAMETERS</span></span>

### <span data-ttu-id="05496-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05496-110">-DefaultProfile</span></span>
<span data-ttu-id="05496-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05496-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05496-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="05496-112">-Name</span></span>
<span data-ttu-id="05496-113">Sanal ağ eşleme adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05496-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05496-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05496-114">-ResourceGroupName</span></span>
<span data-ttu-id="05496-115">Sanal ağ eşliğini ait olduğu kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05496-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="05496-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="05496-116">-VirtualNetworkName</span></span>
<span data-ttu-id="05496-117">Bu cmdlet 'in aldığı sanal ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05496-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="05496-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05496-118">CommonParameters</span></span>
<span data-ttu-id="05496-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05496-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05496-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05496-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05496-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05496-121">INPUTS</span></span>

### <span data-ttu-id="05496-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="05496-122">None</span></span>
<span data-ttu-id="05496-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="05496-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05496-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05496-124">OUTPUTS</span></span>

### <span data-ttu-id="05496-125">Microsoft. Azure. Commands. Network. model. psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="05496-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="05496-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05496-126">NOTES</span></span>

## <span data-ttu-id="05496-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05496-127">RELATED LINKS</span></span>

[<span data-ttu-id="05496-128">Add-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="05496-128">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="05496-129">Remove-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="05496-129">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="05496-130">Set-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="05496-130">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


