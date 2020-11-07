---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: e2b4625536124cdb5352c97564cd4c2792dadb96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918419"
---
# <span data-ttu-id="3c511-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3c511-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="3c511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c511-102">SYNOPSIS</span></span>
<span data-ttu-id="3c511-103">Sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="3c511-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="3c511-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c511-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c511-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c511-105">DESCRIPTION</span></span>
<span data-ttu-id="3c511-106">**Get-Azvirtualnetworkeşlemecmdlet** 'i sanal ağ eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="3c511-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="3c511-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c511-107">EXAMPLES</span></span>

### <span data-ttu-id="3c511-108">Örnek 1: iki sanal ağ arasındaki eşlemeyi alma</span><span class="sxs-lookup"><span data-stu-id="3c511-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="3c511-109">Örnek 2: sanal ağdaki tüm eş lamaları alma</span><span class="sxs-lookup"><span data-stu-id="3c511-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="3c511-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c511-110">PARAMETERS</span></span>

### <span data-ttu-id="3c511-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c511-111">-DefaultProfile</span></span>
<span data-ttu-id="3c511-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c511-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c511-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c511-113">-Name</span></span>
<span data-ttu-id="3c511-114">Sanal ağ eşleme adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c511-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="3c511-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c511-115">-ResourceGroupName</span></span>
<span data-ttu-id="3c511-116">Sanal ağ eşliğini ait olduğu kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c511-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="3c511-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3c511-117">-VirtualNetworkName</span></span>
<span data-ttu-id="3c511-118">Bu cmdlet 'in aldığı sanal ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c511-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3c511-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c511-119">CommonParameters</span></span>
<span data-ttu-id="3c511-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c511-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c511-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c511-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c511-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c511-122">INPUTS</span></span>

### <span data-ttu-id="3c511-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3c511-123">System.String</span></span>

## <span data-ttu-id="3c511-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c511-124">OUTPUTS</span></span>

### <span data-ttu-id="3c511-125">Microsoft. Azure. Commands. Network. model. psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c511-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="3c511-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c511-126">NOTES</span></span>

## <span data-ttu-id="3c511-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c511-127">RELATED LINKS</span></span>

[<span data-ttu-id="3c511-128">Add-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c511-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="3c511-129">Remove-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c511-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="3c511-130">Set-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c511-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
