---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 4b58561783fac3d0c068ec61821c9669a97e1542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591942"
---
# <span data-ttu-id="e65c2-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e65c2-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="e65c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e65c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e65c2-103">Sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="e65c2-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e65c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e65c2-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e65c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e65c2-105">DESCRIPTION</span></span>
<span data-ttu-id="e65c2-106">**Get-Azurermvirtualnetworkeşleme** cmdlet 'i sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="e65c2-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="e65c2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e65c2-107">EXAMPLES</span></span>

### <span data-ttu-id="e65c2-108">Örnek 1: iki sanal ağ arasındaki eşlemeyi alma</span><span class="sxs-lookup"><span data-stu-id="e65c2-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e65c2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e65c2-109">PARAMETERS</span></span>

### <span data-ttu-id="e65c2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e65c2-110">-DefaultProfile</span></span>
<span data-ttu-id="e65c2-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e65c2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e65c2-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="e65c2-112">-Name</span></span>
<span data-ttu-id="e65c2-113">Sanal ağ eşleme adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e65c2-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e65c2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e65c2-114">-ResourceGroupName</span></span>
<span data-ttu-id="e65c2-115">Sanal ağ eşliğini ait olduğu kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e65c2-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="e65c2-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e65c2-116">-VirtualNetworkName</span></span>
<span data-ttu-id="e65c2-117">Bu cmdlet 'in aldığı sanal ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e65c2-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e65c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e65c2-118">CommonParameters</span></span>
<span data-ttu-id="e65c2-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e65c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e65c2-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e65c2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e65c2-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e65c2-121">INPUTS</span></span>

### <span data-ttu-id="e65c2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e65c2-122">System.String</span></span>

## <span data-ttu-id="e65c2-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e65c2-123">OUTPUTS</span></span>

### <span data-ttu-id="e65c2-124">Microsoft. Azure. Commands. Network. model. psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="e65c2-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="e65c2-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e65c2-125">NOTES</span></span>

## <span data-ttu-id="e65c2-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e65c2-126">RELATED LINKS</span></span>

[<span data-ttu-id="e65c2-127">Add-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="e65c2-127">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="e65c2-128">Remove-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="e65c2-128">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="e65c2-129">Set-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="e65c2-129">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


