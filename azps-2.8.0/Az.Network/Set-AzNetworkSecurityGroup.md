---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 78380af20ce5905b5c004424c1e17ac977de40ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932196"
---
# <span data-ttu-id="7c0ac-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7c0ac-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="7c0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0ac-103">Ağ güvenlik grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-103">Updates a network security group.</span></span>

## <span data-ttu-id="7c0ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c0ac-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c0ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c0ac-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0ac-106">**Set-AzNetworkSecurityGroup** cmdlet 'i bir ağ güvenlik grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="7c0ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c0ac-107">EXAMPLES</span></span>

### <span data-ttu-id="7c0ac-108">Örnek 1: varolan bir ağ güvenlik grubunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7c0ac-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="7c0ac-109">Bu komut, Nsg1 adlı Azure ağ güvenlik grubunu alır ve bağlantı noktası 3389 üzerinde Add-AzNetworkSecurityRuleConfig kullanarak bağlantı noktası ' da Internet trafiğine izin vermek için Rdp-Rule adlı bir ağ güvenliği kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="7c0ac-110">Komut, **set-AzNetworkSecurityGroup** kullanarak değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="7c0ac-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c0ac-111">PARAMETERS</span></span>

### <span data-ttu-id="7c0ac-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="7c0ac-112">-AsJob</span></span>
<span data-ttu-id="7c0ac-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7c0ac-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c0ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0ac-114">-DefaultProfile</span></span>
<span data-ttu-id="7c0ac-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c0ac-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7c0ac-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7c0ac-117">Ağ güvenlik grubunun ayarlanması gereken durumu temsil eden bir ağ güvenliği grubu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="7c0ac-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="7c0ac-118">-Confirm</span></span>
<span data-ttu-id="7c0ac-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c0ac-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c0ac-120">-WhatIf</span></span>
<span data-ttu-id="7c0ac-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c0ac-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c0ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0ac-123">CommonParameters</span></span>
<span data-ttu-id="7c0ac-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0ac-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c0ac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0ac-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c0ac-126">INPUTS</span></span>

### <span data-ttu-id="7c0ac-127">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7c0ac-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7c0ac-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c0ac-128">OUTPUTS</span></span>

### <span data-ttu-id="7c0ac-129">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7c0ac-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7c0ac-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c0ac-130">NOTES</span></span>

## <span data-ttu-id="7c0ac-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c0ac-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c0ac-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7c0ac-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="7c0ac-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7c0ac-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="7c0ac-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7c0ac-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

