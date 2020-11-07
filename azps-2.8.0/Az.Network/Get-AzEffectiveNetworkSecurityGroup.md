---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c9dd7695e195386b9dd0921b4a9161a5fb175c6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931776"
---
# <span data-ttu-id="c043f-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c043f-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="c043f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c043f-102">SYNOPSIS</span></span>
<span data-ttu-id="c043f-103">Ağ arabiriminin geçerli ağ güvenliği grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="c043f-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="c043f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c043f-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c043f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c043f-105">DESCRIPTION</span></span>
<span data-ttu-id="c043f-106">**Get-AzEffectiveNetworkSecurityGroup** cmdlet 'i, bir ağ arabirimine uygulanan geçerli ağ güvenlik grubunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="c043f-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="c043f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c043f-107">EXAMPLES</span></span>

### <span data-ttu-id="c043f-108">Örnek 1: ağ arabiriminde geçerli ağ güvenliği grubunu alma</span><span class="sxs-lookup"><span data-stu-id="c043f-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="c043f-109">Bu komut myResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili tüm etkili ağ güvenliği kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="c043f-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="c043f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c043f-110">PARAMETERS</span></span>

### <span data-ttu-id="c043f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c043f-111">-DefaultProfile</span></span>
<span data-ttu-id="c043f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c043f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c043f-113">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="c043f-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="c043f-114">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="c043f-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="c043f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c043f-115">-ResourceGroupName</span></span>
<span data-ttu-id="c043f-116">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c043f-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="c043f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c043f-117">CommonParameters</span></span>
<span data-ttu-id="c043f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c043f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c043f-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c043f-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c043f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c043f-120">INPUTS</span></span>

### <span data-ttu-id="c043f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c043f-121">System.String</span></span>

## <span data-ttu-id="c043f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c043f-122">OUTPUTS</span></span>

### <span data-ttu-id="c043f-123">Microsoft. Azure. Commands. Network. modeller. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c043f-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="c043f-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c043f-124">NOTES</span></span>

## <span data-ttu-id="c043f-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c043f-125">RELATED LINKS</span></span>

[<span data-ttu-id="c043f-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c043f-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


