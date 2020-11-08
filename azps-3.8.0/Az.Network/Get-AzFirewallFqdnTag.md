---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098831"
---
# <span data-ttu-id="5c87b-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="5c87b-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="5c87b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c87b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c87b-103">Kullanılabilir Azure Güvenlik Duvarı FQDN etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5c87b-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="5c87b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c87b-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c87b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c87b-105">DESCRIPTION</span></span>
<span data-ttu-id="5c87b-106">**Get-AzFirewallFqdnTag** cmdlet 'ı, Azure Güvenlik Duvarı uygulama kuralları IÇIN kullanılabilen FQDN etiketlerinin listesini alır</span><span class="sxs-lookup"><span data-stu-id="5c87b-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="5c87b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c87b-107">EXAMPLES</span></span>

### <span data-ttu-id="5c87b-108">1: kullanılabilir tüm FQDN etiketlerini alma</span><span class="sxs-lookup"><span data-stu-id="5c87b-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="5c87b-109">Bu örnekte, kullanılabilir tüm FQDN etiketleri alınır.</span><span class="sxs-lookup"><span data-stu-id="5c87b-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="5c87b-110">2: uygulama kuralında kullanılabilir ilk FQDN etiketini kullanın</span><span class="sxs-lookup"><span data-stu-id="5c87b-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="5c87b-111">Bu örnekte, kullanılabilir ilk FQDN etiketini kullanan bir güvenlik duvarı uygulaması kuralı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="5c87b-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="5c87b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c87b-112">PARAMETERS</span></span>

### <span data-ttu-id="5c87b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c87b-113">-DefaultProfile</span></span>
<span data-ttu-id="5c87b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c87b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c87b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c87b-115">CommonParameters</span></span>
<span data-ttu-id="5c87b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c87b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c87b-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c87b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c87b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c87b-118">INPUTS</span></span>

### <span data-ttu-id="5c87b-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5c87b-119">None</span></span>

## <span data-ttu-id="5c87b-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c87b-120">OUTPUTS</span></span>

### <span data-ttu-id="5c87b-121">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="5c87b-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="5c87b-122">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5c87b-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5c87b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c87b-123">NOTES</span></span>

## <span data-ttu-id="5c87b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c87b-124">RELATED LINKS</span></span>

[<span data-ttu-id="5c87b-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="5c87b-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="5c87b-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5c87b-126">New-AzFirewall</span></span>](./New-AzFirewall.md)