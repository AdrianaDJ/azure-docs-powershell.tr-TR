---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096857"
---
# <span data-ttu-id="be9fa-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="be9fa-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="be9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="be9fa-103">Sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="be9fa-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="be9fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be9fa-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be9fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="be9fa-106">**Get-Azvirtualnetworkeşlemecmdlet** 'i sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="be9fa-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="be9fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="be9fa-108">Örnek 1: iki sanal ağ arasındaki eşlemeyi alma</span><span class="sxs-lookup"><span data-stu-id="be9fa-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="be9fa-109">Örnek 2: sanal ağdaki tüm eş lamaları alma</span><span class="sxs-lookup"><span data-stu-id="be9fa-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="be9fa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be9fa-110">PARAMETERS</span></span>

### <span data-ttu-id="be9fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be9fa-111">-DefaultProfile</span></span>
<span data-ttu-id="be9fa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be9fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be9fa-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="be9fa-113">-Name</span></span>
<span data-ttu-id="be9fa-114">Sanal ağ eşleme adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9fa-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="be9fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be9fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="be9fa-116">Sanal ağ eşliğini ait olduğu kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9fa-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="be9fa-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="be9fa-117">-VirtualNetworkName</span></span>
<span data-ttu-id="be9fa-118">Bu cmdlet 'in aldığı sanal ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9fa-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="be9fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be9fa-119">CommonParameters</span></span>
<span data-ttu-id="be9fa-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be9fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be9fa-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be9fa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be9fa-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be9fa-122">INPUTS</span></span>

### <span data-ttu-id="be9fa-123">System. String</span><span class="sxs-lookup"><span data-stu-id="be9fa-123">System.String</span></span>

## <span data-ttu-id="be9fa-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be9fa-124">OUTPUTS</span></span>

### <span data-ttu-id="be9fa-125">Microsoft. Azure. Commands. Network. model. psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="be9fa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="be9fa-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be9fa-126">NOTES</span></span>

## <span data-ttu-id="be9fa-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be9fa-127">RELATED LINKS</span></span>

[<span data-ttu-id="be9fa-128">Add-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="be9fa-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="be9fa-129">Remove-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="be9fa-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="be9fa-130">Set-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="be9fa-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)