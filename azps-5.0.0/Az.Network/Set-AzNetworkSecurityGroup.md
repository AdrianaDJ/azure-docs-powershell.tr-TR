---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277236"
---
# <span data-ttu-id="f9929-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9929-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="f9929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9929-102">SYNOPSIS</span></span>
<span data-ttu-id="f9929-103">Ağ güvenlik grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f9929-103">Updates a network security group.</span></span>

## <span data-ttu-id="f9929-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9929-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9929-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9929-105">DESCRIPTION</span></span>
<span data-ttu-id="f9929-106">**Set-AzNetworkSecurityGroup** cmdlet 'i bir ağ güvenlik grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f9929-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="f9929-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9929-107">EXAMPLES</span></span>

### <span data-ttu-id="f9929-108">Örnek 1: varolan bir ağ güvenlik grubunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f9929-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="f9929-109">Bu komut, Nsg1 adlı Azure ağ güvenlik grubunu alır ve bağlantı noktası 3389 üzerinde Add-AzNetworkSecurityRuleConfig kullanarak bağlantı noktası ' da Internet trafiğine izin vermek için Rdp-Rule adlı bir ağ güvenliği kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="f9929-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="f9929-110">Komut, **set-AzNetworkSecurityGroup** kullanarak değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="f9929-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="f9929-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9929-111">PARAMETERS</span></span>

### <span data-ttu-id="f9929-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="f9929-112">-AsJob</span></span>
<span data-ttu-id="f9929-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f9929-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9929-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9929-114">-DefaultProfile</span></span>
<span data-ttu-id="f9929-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9929-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9929-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9929-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f9929-117">Ağ güvenlik grubunun ayarlanması gereken durumu temsil eden bir ağ güvenliği grubu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9929-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="f9929-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9929-118">-Confirm</span></span>
<span data-ttu-id="f9929-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9929-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9929-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9929-120">-WhatIf</span></span>
<span data-ttu-id="f9929-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9929-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9929-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9929-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9929-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9929-123">CommonParameters</span></span>
<span data-ttu-id="f9929-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9929-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9929-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9929-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9929-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9929-126">INPUTS</span></span>

### <span data-ttu-id="f9929-127">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9929-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="f9929-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9929-128">OUTPUTS</span></span>

### <span data-ttu-id="f9929-129">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9929-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="f9929-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9929-130">NOTES</span></span>

## <span data-ttu-id="f9929-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9929-131">RELATED LINKS</span></span>

[<span data-ttu-id="f9929-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9929-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="f9929-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9929-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="f9929-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9929-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


