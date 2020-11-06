---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 565d0748104e537f448a40116a48f0cd34ebf16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588070"
---
# <span data-ttu-id="123a9-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="123a9-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="123a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123a9-102">SYNOPSIS</span></span>
<span data-ttu-id="123a9-103">Ağ arabiriminin geçerli ağ güvenliği grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="123a9-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="123a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="123a9-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="123a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="123a9-105">DESCRIPTION</span></span>
<span data-ttu-id="123a9-106">**Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet 'i, bir ağ arabirimine uygulanan geçerli ağ güvenlik grubunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="123a9-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="123a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="123a9-107">EXAMPLES</span></span>

### <span data-ttu-id="123a9-108">Örnek 1: ağ arabiriminde geçerli ağ güvenliği grubunu alma</span><span class="sxs-lookup"><span data-stu-id="123a9-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="123a9-109">Bu komut myResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili tüm etkili ağ güvenliği kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="123a9-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="123a9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="123a9-110">PARAMETERS</span></span>

### <span data-ttu-id="123a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123a9-111">-DefaultProfile</span></span>
<span data-ttu-id="123a9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="123a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="123a9-113">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="123a9-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="123a9-114">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="123a9-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="123a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="123a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="123a9-116">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="123a9-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="123a9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123a9-117">CommonParameters</span></span>
<span data-ttu-id="123a9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="123a9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123a9-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123a9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123a9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="123a9-120">INPUTS</span></span>

### <span data-ttu-id="123a9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="123a9-121">System.String</span></span>

## <span data-ttu-id="123a9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="123a9-122">OUTPUTS</span></span>

### <span data-ttu-id="123a9-123">Microsoft. Azure. Commands. Network. modeller. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="123a9-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="123a9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="123a9-124">NOTES</span></span>

## <span data-ttu-id="123a9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="123a9-125">RELATED LINKS</span></span>

[<span data-ttu-id="123a9-126">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="123a9-126">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


