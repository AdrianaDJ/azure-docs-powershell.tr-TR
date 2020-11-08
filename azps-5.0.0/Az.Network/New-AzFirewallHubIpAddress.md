---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278324"
---
# <span data-ttu-id="5637e-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="5637e-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="5637e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5637e-102">SYNOPSIS</span></span>
<span data-ttu-id="5637e-103">Sanal hub 'daki güvenlik duvarına IP adresleri</span><span class="sxs-lookup"><span data-stu-id="5637e-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="5637e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5637e-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5637e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5637e-105">DESCRIPTION</span></span>
<span data-ttu-id="5637e-106">IP adresleri sanal hub 'daki güvenlik duvarına katılır.</span><span class="sxs-lookup"><span data-stu-id="5637e-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="5637e-107">Bunlar genel ve özel adresler olabilir</span><span class="sxs-lookup"><span data-stu-id="5637e-107">These can be public and private addresses</span></span>

## <span data-ttu-id="5637e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5637e-108">EXAMPLES</span></span>

### <span data-ttu-id="5637e-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5637e-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="5637e-110">Bu örnek, sayısı 2 genel IP olan bir hub IP adresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5637e-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="5637e-111">Hubıpaddress nesnesi sanal hub 'daki güvenlik duvarına katılır.</span><span class="sxs-lookup"><span data-stu-id="5637e-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="5637e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5637e-112">PARAMETERS</span></span>

### <span data-ttu-id="5637e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5637e-113">-DefaultProfile</span></span>
<span data-ttu-id="5637e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5637e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5637e-115">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="5637e-115">-PrivateIPAddress</span></span>
<span data-ttu-id="5637e-116">Hub 'a bağlı güvenlik duvarının özel IP adresi</span><span class="sxs-lookup"><span data-stu-id="5637e-116">The private Ip Address of the Firewall attached to a Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5637e-117">-Publicıp 'Ler</span><span class="sxs-lookup"><span data-stu-id="5637e-117">-PublicIPs</span></span>
<span data-ttu-id="5637e-118">Hub 'a bağlı güvenlik duvarının IP adresleri</span><span class="sxs-lookup"><span data-stu-id="5637e-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5637e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5637e-119">-Confirm</span></span>
<span data-ttu-id="5637e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5637e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5637e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5637e-121">-WhatIf</span></span>
<span data-ttu-id="5637e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5637e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5637e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5637e-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5637e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5637e-124">CommonParameters</span></span>
<span data-ttu-id="5637e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5637e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5637e-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5637e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5637e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5637e-127">INPUTS</span></span>

### <span data-ttu-id="5637e-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5637e-128">None</span></span>

## <span data-ttu-id="5637e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5637e-129">OUTPUTS</span></span>

### <span data-ttu-id="5637e-130">Microsoft. Azure. Commands. Network. model. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="5637e-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="5637e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5637e-131">NOTES</span></span>

## <span data-ttu-id="5637e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5637e-132">RELATED LINKS</span></span>
