---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 214ab7f91791fa05453e2f4ef4238440d9c78a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939132"
---
# <span data-ttu-id="d2d5b-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d2d5b-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="d2d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d5b-103">Ağ arabiriminin geçerli ağ güvenliği grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2d5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2d5b-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2d5b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="d2d5b-106">**Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet 'i, bir ağ arabirimine uygulanan geçerli ağ güvenlik grubunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="d2d5b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2d5b-107">EXAMPLES</span></span>

### <span data-ttu-id="d2d5b-108">Örnek 1: ağ arabiriminde geçerli ağ güvenliği grubunu alma</span><span class="sxs-lookup"><span data-stu-id="d2d5b-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d2d5b-109">Bu komut myResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili tüm etkili ağ güvenliği kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="d2d5b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2d5b-110">PARAMETERS</span></span>

### <span data-ttu-id="d2d5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d5b-111">-DefaultProfile</span></span>
<span data-ttu-id="d2d5b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d5b-113">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="d2d5b-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="d2d5b-114">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="d2d5b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d5b-115">-ResourceGroupName</span></span>
<span data-ttu-id="d2d5b-116">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="d2d5b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d5b-117">CommonParameters</span></span>
<span data-ttu-id="d2d5b-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d5b-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d5b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d5b-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2d5b-120">INPUTS</span></span>

## <span data-ttu-id="d2d5b-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2d5b-121">OUTPUTS</span></span>

### <span data-ttu-id="d2d5b-122">Microsoft. Azure. Commands. Network. modeller. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d2d5b-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="d2d5b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2d5b-123">NOTES</span></span>

## <span data-ttu-id="d2d5b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2d5b-124">RELATED LINKS</span></span>

[<span data-ttu-id="d2d5b-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d2d5b-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


