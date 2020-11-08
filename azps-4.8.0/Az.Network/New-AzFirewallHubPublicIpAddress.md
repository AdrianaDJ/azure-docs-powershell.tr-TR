---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274858"
---
# <span data-ttu-id="e2aad-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2aad-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="e2aad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2aad-102">SYNOPSIS</span></span>
<span data-ttu-id="e2aad-103">Sanal hub 'da ortak IP 'ler güvenlik duvarına katılır</span><span class="sxs-lookup"><span data-stu-id="e2aad-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="e2aad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2aad-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2aad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2aad-105">DESCRIPTION</span></span>
<span data-ttu-id="e2aad-106">Sanal hub 'da ortak IP 'ler güvenlik duvarına katılır</span><span class="sxs-lookup"><span data-stu-id="e2aad-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="e2aad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2aad-107">EXAMPLES</span></span>

### <span data-ttu-id="e2aad-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2aad-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="e2aad-109">Bu, sanal hub 'a bağlı güvenlik duvarında 2 genel IP oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2aad-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="e2aad-110">Bu, IP adresini arka planda oluşturur. Yeni bir güvenlik duvarı için özel olarak IP adresi sağlayamıyoruz.</span><span class="sxs-lookup"><span data-stu-id="e2aad-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="e2aad-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e2aad-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="e2aad-112">Bu, güvenlik duvarında $publicIp 1 ' i korur $publicIp 2 ' yi güvenlik duvarında var olan yeni genel IP 'yi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2aad-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="e2aad-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2aad-113">PARAMETERS</span></span>

### <span data-ttu-id="e2aad-114">-Adresler</span><span class="sxs-lookup"><span data-stu-id="e2aad-114">-Addresses</span></span>
<span data-ttu-id="e2aad-115">Hub 'a bağlı güvenlik duvarının genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="e2aad-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2aad-116">-Sayı</span><span class="sxs-lookup"><span data-stu-id="e2aad-116">-Count</span></span>
<span data-ttu-id="e2aad-117">Genel IP adreslerinin sayısı</span><span class="sxs-lookup"><span data-stu-id="e2aad-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2aad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2aad-118">-DefaultProfile</span></span>
<span data-ttu-id="e2aad-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2aad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2aad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2aad-120">CommonParameters</span></span>
<span data-ttu-id="e2aad-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2aad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2aad-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2aad-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2aad-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2aad-123">INPUTS</span></span>

### <span data-ttu-id="e2aad-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e2aad-124">None</span></span>

## <span data-ttu-id="e2aad-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2aad-125">OUTPUTS</span></span>

### <span data-ttu-id="e2aad-126">Microsoft. Azure. Commands. Network. model. Psazurefirewallhubpublicıpaddresses</span><span class="sxs-lookup"><span data-stu-id="e2aad-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="e2aad-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2aad-127">NOTES</span></span>

## <span data-ttu-id="e2aad-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2aad-128">RELATED LINKS</span></span>
