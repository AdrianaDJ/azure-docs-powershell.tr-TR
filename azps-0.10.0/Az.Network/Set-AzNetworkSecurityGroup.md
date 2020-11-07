---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936529"
---
# <span data-ttu-id="83279-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83279-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="83279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83279-102">SYNOPSIS</span></span>
<span data-ttu-id="83279-103">Ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83279-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="83279-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83279-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83279-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83279-105">DESCRIPTION</span></span>
<span data-ttu-id="83279-106">**Set-Azağsecuritygroup** cmdlet 'ı bir Azure ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83279-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="83279-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83279-107">EXAMPLES</span></span>

### <span data-ttu-id="83279-108">Örnek 1: ağ güvenlik grubunun hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="83279-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="83279-109">Bu komut, Nsg1 adlı Azure ağ güvenlik grubunu alır ve bağlantı noktası 3389 üzerinde Add-AzNetworkSecurityRuleConfig kullanarak bağlantı noktası ' da Internet trafiğine izin vermek için Rdp-Rule adlı bir ağ güvenliği kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="83279-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="83279-110">Komut, **set-AzNetworkSecurityGroup** kullanarak değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="83279-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="83279-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83279-111">PARAMETERS</span></span>

### <span data-ttu-id="83279-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="83279-112">-AsJob</span></span>
<span data-ttu-id="83279-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="83279-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83279-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83279-114">-DefaultProfile</span></span>
<span data-ttu-id="83279-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83279-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83279-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83279-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="83279-117">Cmdlet 'in ağ güvenlik grubunu ayarladığı hedef durumu temsil eden bir ağ güvenliği grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="83279-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83279-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83279-118">CommonParameters</span></span>
<span data-ttu-id="83279-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83279-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83279-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83279-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83279-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83279-121">INPUTS</span></span>

### <span data-ttu-id="83279-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83279-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="83279-123">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="83279-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="83279-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83279-124">OUTPUTS</span></span>

### <span data-ttu-id="83279-125">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83279-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="83279-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83279-126">NOTES</span></span>

## <span data-ttu-id="83279-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83279-127">RELATED LINKS</span></span>

[<span data-ttu-id="83279-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83279-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="83279-129">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83279-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="83279-130">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83279-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


