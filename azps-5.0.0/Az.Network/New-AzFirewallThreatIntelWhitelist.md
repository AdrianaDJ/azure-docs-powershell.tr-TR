---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276405"
---
# <span data-ttu-id="7611a-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="7611a-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="7611a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7611a-102">SYNOPSIS</span></span>
<span data-ttu-id="7611a-103">Azure Güvenlik Duvarı için yeni tehdit zekası beyaz listesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7611a-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="7611a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7611a-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7611a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7611a-105">DESCRIPTION</span></span>
<span data-ttu-id="7611a-106">**New-Azfirewallthreatıntelwhitelist** cmdlet 'i, bir Azure Güvenlik duvarı oluştururken veya ayarlarken kullanılabilen bir tehdit Intel Whitelist nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611a-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="7611a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7611a-107">EXAMPLES</span></span>

### <span data-ttu-id="7611a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7611a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="7611a-109">Bu örnek, iki girişin FQDN beyaz listesini ve iki girişin IP adresi beyaz listesini içeren bir tehdit Intel beyaz listesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="7611a-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="7611a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7611a-110">PARAMETERS</span></span>

### <span data-ttu-id="7611a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7611a-111">-DefaultProfile</span></span>
<span data-ttu-id="7611a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7611a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7611a-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="7611a-113">-FQDN</span></span>
<span data-ttu-id="7611a-114">Tehdit Intel Whitelist 'in FQDN 'leri</span><span class="sxs-lookup"><span data-stu-id="7611a-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611a-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="7611a-115">-IpAddress</span></span>
<span data-ttu-id="7611a-116">Tehdit Intel Whitelist 'in IP adresleri</span><span class="sxs-lookup"><span data-stu-id="7611a-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7611a-117">CommonParameters</span></span>
<span data-ttu-id="7611a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7611a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7611a-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7611a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7611a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7611a-120">INPUTS</span></span>

### <span data-ttu-id="7611a-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7611a-121">None</span></span>

## <span data-ttu-id="7611a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7611a-122">OUTPUTS</span></span>

### <span data-ttu-id="7611a-123">Microsoft. Azure. Commands. Network. model. Psazurefirewallthreatıntelwhitelist</span><span class="sxs-lookup"><span data-stu-id="7611a-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="7611a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7611a-124">NOTES</span></span>

## <span data-ttu-id="7611a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7611a-125">RELATED LINKS</span></span>

[<span data-ttu-id="7611a-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7611a-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="7611a-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7611a-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="7611a-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7611a-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)