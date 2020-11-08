---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105638"
---
# <span data-ttu-id="e8f55-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="e8f55-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="e8f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f55-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f55-103">Alt ağın ağ güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="e8f55-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="e8f55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8f55-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8f55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8f55-105">DESCRIPTION</span></span>
<span data-ttu-id="e8f55-106">**Get-AzureNetworkSecurityGroupForSubnet** cmdlet 'i, bir alt ağla ilişkilendirilmiş ağ güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="e8f55-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="e8f55-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8f55-107">EXAMPLES</span></span>

## <span data-ttu-id="e8f55-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8f55-108">PARAMETERS</span></span>

### <span data-ttu-id="e8f55-109">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="e8f55-109">-Detailed</span></span>
<span data-ttu-id="e8f55-110">Bu cmdlet 'in ağ güvenlik kurallarını görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8f55-110">Indicates that this cmdlet displays the network security rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f55-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="e8f55-111">-Profile</span></span>
<span data-ttu-id="e8f55-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f55-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8f55-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e8f55-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f55-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e8f55-114">-SubnetName</span></span>
<span data-ttu-id="e8f55-115">Bu cmdlet 'in ağ güvenlik grubunu aldığı alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f55-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

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

### <span data-ttu-id="e8f55-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e8f55-116">-VirtualNetworkName</span></span>
<span data-ttu-id="e8f55-117">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f55-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="e8f55-118">Bu cmdlet, sanal ağda bu parametrenin belirttiği bir alt ağda ağ güvenlik grubu alır.</span><span class="sxs-lookup"><span data-stu-id="e8f55-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8f55-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f55-119">CommonParameters</span></span>
<span data-ttu-id="e8f55-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8f55-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f55-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f55-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f55-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8f55-122">INPUTS</span></span>

## <span data-ttu-id="e8f55-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8f55-123">OUTPUTS</span></span>

## <span data-ttu-id="e8f55-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8f55-124">NOTES</span></span>

## <span data-ttu-id="e8f55-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8f55-125">RELATED LINKS</span></span>

[<span data-ttu-id="e8f55-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="e8f55-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="e8f55-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="e8f55-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
