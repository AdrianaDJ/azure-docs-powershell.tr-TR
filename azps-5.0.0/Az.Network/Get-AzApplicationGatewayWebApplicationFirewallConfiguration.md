---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279971"
---
# <span data-ttu-id="74a1e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a1e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="74a1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="74a1e-103">Uygulama ağ geçidinin WAF yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="74a1e-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="74a1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74a1e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74a1e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74a1e-105">DESCRIPTION</span></span>
<span data-ttu-id="74a1e-106">**Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i, uygulama ağ geçidinin Web uygulaması güvenlik duvarı (WAF) yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="74a1e-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="74a1e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74a1e-107">EXAMPLES</span></span>

### <span data-ttu-id="74a1e-108">Örnek 1: uygulama ağ geçidi Web uygulaması güvenlik duvarı yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="74a1e-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="74a1e-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGW değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="74a1e-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="74a1e-110">İkinci komut $AppGW uygulama ağ geçidinin güvenlik duvarı yapılandırmasını alır ve $FirewallConfig depolar.</span><span class="sxs-lookup"><span data-stu-id="74a1e-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="74a1e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74a1e-111">PARAMETERS</span></span>

### <span data-ttu-id="74a1e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74a1e-112">-ApplicationGateway</span></span>
<span data-ttu-id="74a1e-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a1e-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="74a1e-114">Uygulama ağ geçidi nesnesi almak için Get-AzApplicationGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74a1e-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74a1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a1e-115">-DefaultProfile</span></span>
<span data-ttu-id="74a1e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74a1e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74a1e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a1e-117">CommonParameters</span></span>
<span data-ttu-id="74a1e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74a1e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a1e-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="74a1e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a1e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74a1e-120">INPUTS</span></span>

### <span data-ttu-id="74a1e-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74a1e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74a1e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74a1e-122">OUTPUTS</span></span>

### <span data-ttu-id="74a1e-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a1e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="74a1e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74a1e-124">NOTES</span></span>

## <span data-ttu-id="74a1e-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74a1e-125">RELATED LINKS</span></span>

[<span data-ttu-id="74a1e-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74a1e-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="74a1e-127">Yeni-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a1e-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="74a1e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a1e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


