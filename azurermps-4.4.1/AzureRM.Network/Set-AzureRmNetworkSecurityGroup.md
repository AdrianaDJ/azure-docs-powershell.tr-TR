---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589230"
---
# <span data-ttu-id="aebdc-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebdc-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="aebdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aebdc-102">SYNOPSIS</span></span>
<span data-ttu-id="aebdc-103">Ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aebdc-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aebdc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aebdc-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aebdc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aebdc-105">DESCRIPTION</span></span>
<span data-ttu-id="aebdc-106">**Set-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aebdc-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="aebdc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aebdc-107">EXAMPLES</span></span>

### <span data-ttu-id="aebdc-108">Örnek 1: ağ güvenlik grubunun hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="aebdc-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="aebdc-109">Bu komut, Nsg1 adlı Azure ağ güvenlik grubunu alır ve bağlantı noktası 3389 üzerinde, Add-AzureRmNetworkSecurityRuleConfig kullanarak bağlantı noktası ' da Internet trafiğine izin verecek bir ağ güvenliği Rdp-Rule kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="aebdc-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="aebdc-110">Komut, **set-AzureRmNetworkSecurityGroup** kullanarak değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="aebdc-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="aebdc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aebdc-111">PARAMETERS</span></span>

### <span data-ttu-id="aebdc-112">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebdc-112">-NetworkSecurityGroup</span></span>
<span data-ttu-id="aebdc-113">Cmdlet 'in ağ güvenlik grubunu ayarladığı hedef durumu temsil eden bir ağ güvenliği grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aebdc-113">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aebdc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebdc-114">-DefaultProfile</span></span>
<span data-ttu-id="aebdc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aebdc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aebdc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebdc-116">CommonParameters</span></span>
<span data-ttu-id="aebdc-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aebdc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebdc-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aebdc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebdc-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aebdc-119">INPUTS</span></span>

### <span data-ttu-id="aebdc-120">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebdc-120">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="aebdc-121">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="aebdc-121">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="aebdc-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aebdc-122">OUTPUTS</span></span>

### <span data-ttu-id="aebdc-123">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebdc-123">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="aebdc-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aebdc-124">NOTES</span></span>

## <span data-ttu-id="aebdc-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aebdc-125">RELATED LINKS</span></span>

[<span data-ttu-id="aebdc-126">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebdc-126">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="aebdc-127">Yeni-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebdc-127">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="aebdc-128">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebdc-128">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


