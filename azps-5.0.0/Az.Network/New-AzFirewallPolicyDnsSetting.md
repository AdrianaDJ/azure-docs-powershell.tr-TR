---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279663"
---
# <span data-ttu-id="76cd8-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="76cd8-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="76cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="76cd8-103">Azure Güvenlik Duvarı Ilkesi için yeni bir DNS ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="76cd8-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="76cd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76cd8-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76cd8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="76cd8-106">**New-AzFirewallPolicyDnsSetting** cmdlet 'ı Azure Güvenlik Duvarı ILKESI Için DNS ayar nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="76cd8-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="76cd8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="76cd8-108">1. boş ilke oluşturma</span><span class="sxs-lookup"><span data-stu-id="76cd8-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="76cd8-109">Bu örnek, DNS proxy 'yi etkinleştirmeye yönelik bir DNS ayar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76cd8-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="76cd8-110">2. Threatıntel moduyla boş bir ilke oluşturma</span><span class="sxs-lookup"><span data-stu-id="76cd8-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="76cd8-111">Bu örnek, DNS proxy 'yi etkinleştirme ve özel DNS sunucularını ayarlama gibi bir DNS ayar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76cd8-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="76cd8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76cd8-112">PARAMETERS</span></span>

### <span data-ttu-id="76cd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cd8-113">-DefaultProfile</span></span>
<span data-ttu-id="76cd8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76cd8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76cd8-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="76cd8-115">-EnableProxy</span></span>
<span data-ttu-id="76cd8-116">DNS proxy 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="76cd8-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="76cd8-117">Varsayılan olarak devre dışıdır.</span><span class="sxs-lookup"><span data-stu-id="76cd8-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="76cd8-118">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="76cd8-118">-Server</span></span>
<span data-ttu-id="76cd8-119">DNS sunucuları listesi</span><span class="sxs-lookup"><span data-stu-id="76cd8-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="76cd8-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="76cd8-120">-Confirm</span></span>
<span data-ttu-id="76cd8-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76cd8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76cd8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76cd8-122">-WhatIf</span></span>
<span data-ttu-id="76cd8-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76cd8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76cd8-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76cd8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76cd8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cd8-125">CommonParameters</span></span>
<span data-ttu-id="76cd8-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76cd8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cd8-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76cd8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cd8-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76cd8-128">INPUTS</span></span>

### <span data-ttu-id="76cd8-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76cd8-129">None</span></span>

## <span data-ttu-id="76cd8-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76cd8-130">OUTPUTS</span></span>

### <span data-ttu-id="76cd8-131">Microsoft. Azure. Commands. Network. model. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="76cd8-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="76cd8-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76cd8-132">NOTES</span></span>

## <span data-ttu-id="76cd8-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76cd8-133">RELATED LINKS</span></span>
