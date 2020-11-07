---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a7c131db8ce5a3489bc2a869e31b0ef7ab89f3c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763014"
---
# <span data-ttu-id="f037a-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f037a-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f037a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f037a-102">SYNOPSIS</span></span>
<span data-ttu-id="f037a-103">Ağ arabiriminin geçerli ağ güvenliği grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="f037a-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f037a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f037a-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f037a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f037a-105">DESCRIPTION</span></span>
<span data-ttu-id="f037a-106">**Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet 'i, bir ağ arabirimine uygulanan geçerli ağ güvenlik grubunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="f037a-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="f037a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f037a-107">EXAMPLES</span></span>

### <span data-ttu-id="f037a-108">Örnek 1: ağ arabiriminde geçerli ağ güvenliği grubunu alma</span><span class="sxs-lookup"><span data-stu-id="f037a-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="f037a-109">Bu komut myResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili tüm etkili ağ güvenliği kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="f037a-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="f037a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f037a-110">PARAMETERS</span></span>

### <span data-ttu-id="f037a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f037a-111">-DefaultProfile</span></span>
<span data-ttu-id="f037a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f037a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f037a-113">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="f037a-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="f037a-114">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="f037a-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="f037a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f037a-115">-ResourceGroupName</span></span>
<span data-ttu-id="f037a-116">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f037a-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="f037a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f037a-117">CommonParameters</span></span>
<span data-ttu-id="f037a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f037a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f037a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f037a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f037a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f037a-120">INPUTS</span></span>

### <span data-ttu-id="f037a-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f037a-121">None</span></span>
<span data-ttu-id="f037a-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f037a-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f037a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f037a-123">OUTPUTS</span></span>

### <span data-ttu-id="f037a-124">Microsoft. Azure. Commands. Network. modeller. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f037a-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f037a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f037a-125">NOTES</span></span>

## <span data-ttu-id="f037a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f037a-126">RELATED LINKS</span></span>

[<span data-ttu-id="f037a-127">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f037a-127">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


