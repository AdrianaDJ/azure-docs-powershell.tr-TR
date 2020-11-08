---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274874"
---
# <span data-ttu-id="59c16-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c16-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="59c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c16-102">SYNOPSIS</span></span>
<span data-ttu-id="59c16-103">Uygulama ağ geçidi için özel bağlantı yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="59c16-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="59c16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59c16-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59c16-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59c16-105">DESCRIPTION</span></span>
<span data-ttu-id="59c16-106">**Yeni-AzApplicationGatewayPrivateLinkConfiguration** cmdlet 'i, bir Azure Application Gateway Için Privatelink yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59c16-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="59c16-107">Özel bağlantı işlevselliğini etkinleştirmek için özel bağlantı yapılandırmasının bir ön uç IP yapılandırmasıyla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="59c16-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="59c16-108">Tek bir özel bağlantı yapılandırması, uygulama ağ geçidinde yalnızca bir ön uç IP yapılandırmasıyla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="59c16-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="59c16-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59c16-109">EXAMPLES</span></span>

### <span data-ttu-id="59c16-110">Örnek 1: tek IP yapılandırması ile özel bağlantı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="59c16-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="59c16-111">Bu komut, ' privateLinkConfig01 ' adlı bir PrivateLink yapılandırması oluşturur ve sonucu $PrivateLinkConfiguration adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="59c16-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="59c16-112">Örnek 2: birden çok IP yapılandırmasıyla özel bağlantı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="59c16-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="59c16-113">Bu komut iki ıpconfigurations ile ' privateLinkConfig01 ' adlı bir PrivateLink yapılandırması oluşturur ve sonucu $PrivateLinkConfiguration adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="59c16-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="59c16-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59c16-114">PARAMETERS</span></span>

### <span data-ttu-id="59c16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c16-115">-DefaultProfile</span></span>
<span data-ttu-id="59c16-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59c16-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c16-117">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="59c16-117">-IpConfiguration</span></span>
<span data-ttu-id="59c16-118">IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="59c16-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c16-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="59c16-119">-Name</span></span>
<span data-ttu-id="59c16-120">PrivateLink yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="59c16-120">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c16-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="59c16-121">-Confirm</span></span>
<span data-ttu-id="59c16-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59c16-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59c16-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c16-123">-WhatIf</span></span>
<span data-ttu-id="59c16-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59c16-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59c16-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59c16-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59c16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c16-126">CommonParameters</span></span>
<span data-ttu-id="59c16-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59c16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c16-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59c16-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c16-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59c16-129">INPUTS</span></span>

### <span data-ttu-id="59c16-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="59c16-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="59c16-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59c16-131">OUTPUTS</span></span>

### <span data-ttu-id="59c16-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c16-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="59c16-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59c16-133">NOTES</span></span>

## <span data-ttu-id="59c16-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59c16-134">RELATED LINKS</span></span>

[<span data-ttu-id="59c16-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c16-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="59c16-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c16-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="59c16-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c16-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="59c16-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c16-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
