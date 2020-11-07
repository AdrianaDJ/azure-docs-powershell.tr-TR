---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932014"
---
# <span data-ttu-id="42ae1-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="42ae1-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="42ae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="42ae1-103">Kullanılabilir Azure Güvenlik Duvarı FQDN etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="42ae1-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="42ae1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42ae1-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42ae1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42ae1-105">DESCRIPTION</span></span>
<span data-ttu-id="42ae1-106">**Get-AzFirewallFqdnTag** cmdlet 'ı, Azure Güvenlik Duvarı uygulama kuralları IÇIN kullanılabilen FQDN etiketlerinin listesini alır</span><span class="sxs-lookup"><span data-stu-id="42ae1-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="42ae1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42ae1-107">EXAMPLES</span></span>

### <span data-ttu-id="42ae1-108">1: kullanılabilir tüm FQDN etiketlerini alma</span><span class="sxs-lookup"><span data-stu-id="42ae1-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="42ae1-109">Bu örnekte, kullanılabilir tüm FQDN etiketleri alınır.</span><span class="sxs-lookup"><span data-stu-id="42ae1-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="42ae1-110">2: uygulama kuralında kullanılabilir ilk FQDN etiketini kullanın</span><span class="sxs-lookup"><span data-stu-id="42ae1-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="42ae1-111">Bu örnekte, kullanılabilir ilk FQDN etiketini kullanan bir güvenlik duvarı uygulaması kuralı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="42ae1-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="42ae1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42ae1-112">PARAMETERS</span></span>

### <span data-ttu-id="42ae1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ae1-113">-DefaultProfile</span></span>
<span data-ttu-id="42ae1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42ae1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42ae1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ae1-115">CommonParameters</span></span>
<span data-ttu-id="42ae1-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42ae1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ae1-117">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42ae1-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ae1-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42ae1-118">INPUTS</span></span>

### <span data-ttu-id="42ae1-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="42ae1-119">None</span></span>

## <span data-ttu-id="42ae1-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42ae1-120">OUTPUTS</span></span>

### <span data-ttu-id="42ae1-121">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="42ae1-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="42ae1-122">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="42ae1-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="42ae1-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42ae1-123">NOTES</span></span>

## <span data-ttu-id="42ae1-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42ae1-124">RELATED LINKS</span></span>

[<span data-ttu-id="42ae1-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="42ae1-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="42ae1-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="42ae1-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
