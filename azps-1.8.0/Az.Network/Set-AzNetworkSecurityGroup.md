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
ms.locfileid: "93759987"
---
# <span data-ttu-id="13ada-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="13ada-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="13ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ada-102">SYNOPSIS</span></span>
<span data-ttu-id="13ada-103">Ağ güvenlik grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="13ada-103">Updates a network security group.</span></span>

## <span data-ttu-id="13ada-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13ada-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13ada-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="13ada-105">DESCRIPTION</span></span>
<span data-ttu-id="13ada-106">**Set-AzNetworkSecurityGroup** cmdlet 'i bir ağ güvenlik grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="13ada-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="13ada-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13ada-107">EXAMPLES</span></span>

### <span data-ttu-id="13ada-108">Örnek 1: varolan bir ağ güvenlik grubunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="13ada-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="13ada-109">Bu komut, Nsg1 adlı Azure ağ güvenlik grubunu alır ve bağlantı noktası 3389 üzerinde Add-AzNetworkSecurityRuleConfig kullanarak bağlantı noktası ' da Internet trafiğine izin vermek için Rdp-Rule adlı bir ağ güvenliği kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="13ada-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="13ada-110">Komut, **set-AzNetworkSecurityGroup** kullanarak değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="13ada-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="13ada-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13ada-111">PARAMETERS</span></span>

### <span data-ttu-id="13ada-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="13ada-112">-AsJob</span></span>
<span data-ttu-id="13ada-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="13ada-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13ada-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ada-114">-DefaultProfile</span></span>
<span data-ttu-id="13ada-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13ada-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13ada-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="13ada-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="13ada-117">Ağ güvenlik grubunun ayarlanması gereken durumu temsil eden bir ağ güvenliği grubu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="13ada-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="13ada-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="13ada-118">-Confirm</span></span>
<span data-ttu-id="13ada-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="13ada-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ada-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ada-120">-WhatIf</span></span>
<span data-ttu-id="13ada-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13ada-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13ada-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="13ada-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ada-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ada-123">CommonParameters</span></span>
<span data-ttu-id="13ada-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13ada-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ada-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ada-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ada-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13ada-126">INPUTS</span></span>

### <span data-ttu-id="13ada-127">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="13ada-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="13ada-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13ada-128">OUTPUTS</span></span>

### <span data-ttu-id="13ada-129">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="13ada-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="13ada-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13ada-130">NOTES</span></span>

## <span data-ttu-id="13ada-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13ada-131">RELATED LINKS</span></span>

[<span data-ttu-id="13ada-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="13ada-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="13ada-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="13ada-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="13ada-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="13ada-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


