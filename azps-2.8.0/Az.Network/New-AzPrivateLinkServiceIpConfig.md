---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: c7ea999af626206b741e86457d92627e4db196a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918215"
---
# <span data-ttu-id="91cbd-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="91cbd-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="91cbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="91cbd-103">Özel bağlantı hizmeti IP yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="91cbd-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="91cbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91cbd-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91cbd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91cbd-105">DESCRIPTION</span></span>
<span data-ttu-id="91cbd-106">**Yeni-AzPrivateLinkServiceIpConfig** cmdlet 'i özel bağlantı hizmeti IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91cbd-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="91cbd-107">Bu yapılandırma, Özel uç noktadan gelen trafiği kaynak NAT için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="91cbd-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="91cbd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91cbd-108">EXAMPLES</span></span>

### <span data-ttu-id="91cbd-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91cbd-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="91cbd-110">Bu örnek, bellekte özel bir bağlantı hizmeti IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91cbd-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="91cbd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91cbd-111">PARAMETERS</span></span>

### <span data-ttu-id="91cbd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cbd-112">-DefaultProfile</span></span>
<span data-ttu-id="91cbd-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91cbd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91cbd-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="91cbd-114">-Name</span></span>
<span data-ttu-id="91cbd-115">IP yapılandırması adı</span><span class="sxs-lookup"><span data-stu-id="91cbd-115">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="91cbd-116">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="91cbd-116">-PrivateIpAddress</span></span>
<span data-ttu-id="91cbd-117">Statik ayırma belirtildiyse, IP yapılandırması 'nın özel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="91cbd-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

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

### <span data-ttu-id="91cbd-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="91cbd-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="91cbd-119">IP yapılandırmasının IP sürümü</span><span class="sxs-lookup"><span data-stu-id="91cbd-119">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="91cbd-120">-Birincil</span><span class="sxs-lookup"><span data-stu-id="91cbd-120">-Primary</span></span>
<span data-ttu-id="91cbd-121">Geçerli IP yapılandırmasının birincili olduğunu belirtme.</span><span class="sxs-lookup"><span data-stu-id="91cbd-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="91cbd-122">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="91cbd-122">-Subnet</span></span>
<span data-ttu-id="91cbd-123">AI</span><span class="sxs-lookup"><span data-stu-id="91cbd-123">Subnet</span></span>

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

### <span data-ttu-id="91cbd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cbd-124">CommonParameters</span></span>
<span data-ttu-id="91cbd-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91cbd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cbd-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91cbd-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cbd-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91cbd-127">INPUTS</span></span>

### <span data-ttu-id="91cbd-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="91cbd-128">None</span></span>

## <span data-ttu-id="91cbd-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91cbd-129">OUTPUTS</span></span>

### <span data-ttu-id="91cbd-130">Microsoft. Azure. Commands. Network. model. Psprivatelinkserviceıp 'ler</span><span class="sxs-lookup"><span data-stu-id="91cbd-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="91cbd-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91cbd-131">NOTES</span></span>

## <span data-ttu-id="91cbd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91cbd-132">RELATED LINKS</span></span>

[<span data-ttu-id="91cbd-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="91cbd-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)