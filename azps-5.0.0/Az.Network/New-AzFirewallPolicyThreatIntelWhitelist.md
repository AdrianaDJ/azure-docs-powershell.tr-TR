---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276406"
---
# <span data-ttu-id="ac089-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ac089-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="ac089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac089-102">SYNOPSIS</span></span>
<span data-ttu-id="ac089-103">Azure Güvenlik Duvarı Ilkesi için yeni tehdit zekası beyaz listesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac089-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="ac089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac089-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac089-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac089-105">DESCRIPTION</span></span>
<span data-ttu-id="ac089-106">**New-Azfirewallpolicythreatıntelwhitelist** cmdlet 'i, bir Azure Güvenlik duvarı ilkesi oluştururken veya ayarlarken kullanılabilen bir tehdit Intel Whitelist nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac089-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ac089-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac089-107">EXAMPLES</span></span>

### <span data-ttu-id="ac089-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ac089-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="ac089-109">Bu örnek, bir girdinin FQDN beyaz listesini ve iki girdinin IP adresi beyaz listesini içeren bir tehdit Intel beyaz listesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="ac089-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="ac089-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac089-110">PARAMETERS</span></span>

### <span data-ttu-id="ac089-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac089-111">-DefaultProfile</span></span>
<span data-ttu-id="ac089-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac089-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac089-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="ac089-113">-FQDN</span></span>
<span data-ttu-id="ac089-114">Tehdit Intel Whitelist 'in FQDN 'leri</span><span class="sxs-lookup"><span data-stu-id="ac089-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac089-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="ac089-115">-IpAddress</span></span>
<span data-ttu-id="ac089-116">Tehdit Intel Whitelist 'in IP adresleri</span><span class="sxs-lookup"><span data-stu-id="ac089-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac089-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac089-117">CommonParameters</span></span>
<span data-ttu-id="ac089-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac089-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac089-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ac089-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac089-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac089-120">INPUTS</span></span>

### <span data-ttu-id="ac089-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ac089-121">None</span></span>

## <span data-ttu-id="ac089-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac089-122">OUTPUTS</span></span>

### <span data-ttu-id="ac089-123">Microsoft. Azure. Commands. Network. model. Psazurefirewallpolicythreatıntelwhitelist</span><span class="sxs-lookup"><span data-stu-id="ac089-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="ac089-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac089-124">NOTES</span></span>

## <span data-ttu-id="ac089-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac089-125">RELATED LINKS</span></span>
