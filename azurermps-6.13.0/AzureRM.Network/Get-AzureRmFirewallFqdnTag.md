---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764618"
---
# <span data-ttu-id="e4e1f-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e4e1f-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="e4e1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e1f-103">Kullanılabilir Azure Güvenlik Duvarı FQDN etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4e1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4e1f-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4e1f-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e1f-106">**Get-AzureRmFirewallFqdnTag** cmdlet 'ı, Azure Güvenlik Duvarı uygulama kuralları IÇIN kullanılabilen FQDN etiketlerinin listesini alır</span><span class="sxs-lookup"><span data-stu-id="e4e1f-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="e4e1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4e1f-107">EXAMPLES</span></span>

### <span data-ttu-id="e4e1f-108">1: kullanılabilir tüm FQDN etiketlerini alma</span><span class="sxs-lookup"><span data-stu-id="e4e1f-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="e4e1f-109">Bu örnekte, kullanılabilir tüm FQDN etiketleri alınır.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="e4e1f-110">2: uygulama kuralında kullanılabilir ilk FQDN etiketini kullanın</span><span class="sxs-lookup"><span data-stu-id="e4e1f-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="e4e1f-111">Bu örnekte, kullanılabilir ilk FQDN etiketini kullanan bir güvenlik duvarı uygulaması kuralı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="e4e1f-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="e4e1f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4e1f-112">PARAMETERS</span></span>

### <span data-ttu-id="e4e1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e1f-113">-DefaultProfile</span></span>
<span data-ttu-id="e4e1f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4e1f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e1f-115">CommonParameters</span></span>
<span data-ttu-id="e4e1f-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e1f-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e1f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e1f-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4e1f-118">INPUTS</span></span>

### <span data-ttu-id="e4e1f-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e4e1f-119">None</span></span>
<span data-ttu-id="e4e1f-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4e1f-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4e1f-121">OUTPUTS</span></span>

### <span data-ttu-id="e4e1f-122">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e4e1f-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="e4e1f-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4e1f-123">NOTES</span></span>

## <span data-ttu-id="e4e1f-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4e1f-124">RELATED LINKS</span></span>

[<span data-ttu-id="e4e1f-125">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e4e1f-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="e4e1f-126">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e4e1f-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
