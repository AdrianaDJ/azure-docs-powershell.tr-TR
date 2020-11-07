---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: ab009608100bc4cbb4915f6bc3e82d44d9e08cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764168"
---
# <span data-ttu-id="c707f-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c707f-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="c707f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c707f-102">SYNOPSIS</span></span>
<span data-ttu-id="c707f-103">Ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c707f-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c707f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c707f-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c707f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c707f-105">DESCRIPTION</span></span>
<span data-ttu-id="c707f-106">**Set-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c707f-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="c707f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c707f-107">EXAMPLES</span></span>

### <span data-ttu-id="c707f-108">Örnek 1: ağ güvenlik grubunun hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="c707f-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="c707f-109">Bu komut, Nsg1 adlı Azure ağ güvenlik grubunu alır ve bağlantı noktası 3389 üzerinde, Add-AzureRmNetworkSecurityRuleConfig kullanarak bağlantı noktası ' da Internet trafiğine izin verecek bir ağ güvenliği Rdp-Rule kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="c707f-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="c707f-110">Komut, **set-AzureRmNetworkSecurityGroup** kullanarak değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="c707f-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="c707f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c707f-111">PARAMETERS</span></span>

### <span data-ttu-id="c707f-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="c707f-112">-AsJob</span></span>
<span data-ttu-id="c707f-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c707f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c707f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c707f-114">-DefaultProfile</span></span>
<span data-ttu-id="c707f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c707f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c707f-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c707f-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c707f-117">Cmdlet 'in ağ güvenlik grubunu ayarladığı hedef durumu temsil eden bir ağ güvenliği grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c707f-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="c707f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c707f-118">CommonParameters</span></span>
<span data-ttu-id="c707f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c707f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c707f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c707f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c707f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c707f-121">INPUTS</span></span>

### <span data-ttu-id="c707f-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c707f-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="c707f-123">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c707f-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="c707f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c707f-124">OUTPUTS</span></span>

### <span data-ttu-id="c707f-125">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c707f-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c707f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c707f-126">NOTES</span></span>

## <span data-ttu-id="c707f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c707f-127">RELATED LINKS</span></span>

[<span data-ttu-id="c707f-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c707f-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="c707f-129">Yeni-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c707f-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="c707f-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c707f-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


