---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 3ef8248f90e24da8818a0fa1a8ff6b05970be397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572694"
---
# <span data-ttu-id="f6475-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6475-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="f6475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6475-102">SYNOPSIS</span></span>
<span data-ttu-id="f6475-103">Ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f6475-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6475-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6475-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6475-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6475-105">DESCRIPTION</span></span>
<span data-ttu-id="f6475-106">**Set-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f6475-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="f6475-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6475-107">EXAMPLES</span></span>

### <span data-ttu-id="f6475-108">Örnek 1: ağ güvenlik grubunun hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="f6475-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="f6475-109">Bu komut, Nsg1 adlı Azure ağ güvenlik grubunu alır ve bağlantı noktası 3389 üzerinde, Add-AzureRmNetworkSecurityRuleConfig kullanarak bağlantı noktası ' da Internet trafiğine izin verecek bir ağ güvenliği Rdp-Rule kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="f6475-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="f6475-110">Komut, **set-AzureRmNetworkSecurityGroup** kullanarak değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="f6475-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="f6475-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6475-111">PARAMETERS</span></span>

### <span data-ttu-id="f6475-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="f6475-112">-AsJob</span></span>
<span data-ttu-id="f6475-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f6475-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6475-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6475-114">-DefaultProfile</span></span>
<span data-ttu-id="f6475-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6475-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6475-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6475-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f6475-117">Cmdlet 'in ağ güvenlik grubunu ayarladığı hedef durumu temsil eden bir ağ güvenliği grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f6475-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="f6475-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6475-118">-Confirm</span></span>
<span data-ttu-id="f6475-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6475-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6475-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6475-120">-WhatIf</span></span>
<span data-ttu-id="f6475-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6475-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6475-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6475-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6475-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6475-123">CommonParameters</span></span>
<span data-ttu-id="f6475-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6475-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6475-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6475-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6475-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6475-126">INPUTS</span></span>

### <span data-ttu-id="f6475-127">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6475-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="f6475-128">Parametreler: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f6475-128">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="f6475-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6475-129">OUTPUTS</span></span>

### <span data-ttu-id="f6475-130">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6475-130">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="f6475-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6475-131">NOTES</span></span>

## <span data-ttu-id="f6475-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6475-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6475-133">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6475-133">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="f6475-134">Yeni-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6475-134">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="f6475-135">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6475-135">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


