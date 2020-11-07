---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938954"
---
# <span data-ttu-id="ce427-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce427-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ce427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce427-102">SYNOPSIS</span></span>
<span data-ttu-id="ce427-103">Uygulama ağ geçidinin WAF yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ce427-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce427-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce427-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce427-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce427-105">DESCRIPTION</span></span>
<span data-ttu-id="ce427-106">**Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i, uygulama ağ geçidinin Web uygulaması güvenlik duvarı (WAF) yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ce427-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="ce427-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce427-107">EXAMPLES</span></span>

### <span data-ttu-id="ce427-108">Örnek 1: uygulama ağ geçidi Web uygulaması güvenlik duvarı yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="ce427-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="ce427-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGW değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ce427-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="ce427-110">İkinci komut $AppGW uygulama ağ geçidinin güvenlik duvarı yapılandırmasını alır ve $FirewallConfig depolar.</span><span class="sxs-lookup"><span data-stu-id="ce427-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="ce427-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce427-111">PARAMETERS</span></span>

### <span data-ttu-id="ce427-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce427-112">-ApplicationGateway</span></span>
<span data-ttu-id="ce427-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce427-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="ce427-114">Uygulama ağ geçidi nesnesi almak için Get-AzureRmApplicationGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce427-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce427-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce427-115">-DefaultProfile</span></span>
<span data-ttu-id="ce427-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce427-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce427-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce427-117">CommonParameters</span></span>
<span data-ttu-id="ce427-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce427-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce427-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce427-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce427-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce427-120">INPUTS</span></span>

### <span data-ttu-id="ce427-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce427-121">PSApplicationGateway</span></span>
<span data-ttu-id="ce427-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ce427-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ce427-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce427-123">OUTPUTS</span></span>

### <span data-ttu-id="ce427-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce427-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ce427-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce427-125">NOTES</span></span>

## <span data-ttu-id="ce427-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce427-126">RELATED LINKS</span></span>

[<span data-ttu-id="ce427-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce427-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="ce427-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce427-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ce427-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce427-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


