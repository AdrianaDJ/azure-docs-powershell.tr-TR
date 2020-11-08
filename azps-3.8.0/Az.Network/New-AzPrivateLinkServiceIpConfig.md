---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: e1d7c2d78bf58240cc87e7a224be1632828984d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098735"
---
# <span data-ttu-id="37471-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="37471-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="37471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37471-102">SYNOPSIS</span></span>
<span data-ttu-id="37471-103">Özel bağlantı hizmeti IP yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="37471-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="37471-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37471-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37471-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="37471-105">DESCRIPTION</span></span>
<span data-ttu-id="37471-106">**Yeni-AzPrivateLinkServiceIpConfig** cmdlet 'i özel bağlantı hizmeti IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37471-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="37471-107">Bu yapılandırma, Özel uç noktadan gelen trafiği kaynak NAT için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="37471-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="37471-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37471-108">EXAMPLES</span></span>

### <span data-ttu-id="37471-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37471-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="37471-110">Bu örnek, bellekte özel bir bağlantı hizmeti IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37471-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="37471-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37471-111">PARAMETERS</span></span>

### <span data-ttu-id="37471-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37471-112">-DefaultProfile</span></span>
<span data-ttu-id="37471-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37471-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37471-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="37471-114">-Name</span></span>
<span data-ttu-id="37471-115">IP yapılandırması adı</span><span class="sxs-lookup"><span data-stu-id="37471-115">The name of the IpConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37471-116">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="37471-116">-PrivateIpAddress</span></span>
<span data-ttu-id="37471-117">Statik ayırma belirtildiyse, IP yapılandırması 'nın özel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="37471-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37471-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="37471-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="37471-119">IP yapılandırmasının IP sürümü</span><span class="sxs-lookup"><span data-stu-id="37471-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37471-120">-Birincil</span><span class="sxs-lookup"><span data-stu-id="37471-120">-Primary</span></span>
<span data-ttu-id="37471-121">Geçerli IP yapılandırmasının birincili olduğunu belirtme.</span><span class="sxs-lookup"><span data-stu-id="37471-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="37471-122">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="37471-122">-Subnet</span></span>
<span data-ttu-id="37471-123">AI</span><span class="sxs-lookup"><span data-stu-id="37471-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37471-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37471-124">CommonParameters</span></span>
<span data-ttu-id="37471-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37471-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37471-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="37471-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37471-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37471-127">INPUTS</span></span>

### <span data-ttu-id="37471-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="37471-128">None</span></span>

## <span data-ttu-id="37471-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37471-129">OUTPUTS</span></span>

### <span data-ttu-id="37471-130">Microsoft. Azure. Commands. Network. model. Psprivatelinkserviceıp 'ler</span><span class="sxs-lookup"><span data-stu-id="37471-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="37471-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37471-131">NOTES</span></span>

## <span data-ttu-id="37471-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37471-132">RELATED LINKS</span></span>

[<span data-ttu-id="37471-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37471-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)