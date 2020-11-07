---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9516d132f2c6b26c162dcbb8abc742e69dccfc14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760106"
---
# <span data-ttu-id="e2e8f-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e2e8f-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="e2e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e8f-103">Sanal ağ ağ geçidinden varsayılan siteyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="e2e8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2e8f-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e8f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e8f-106">**Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet 'i, Zorlamalı tünel varsayılan sitesini sanal ağ ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="e2e8f-107">Zorlamalı tünel, Azure sanal makinelerden şirket içi ağınıza Internet 'e bağlı trafik yönlendirmenize yol sunar; Bu, göndermeden önce trafiği incelemenizi ve denetlemenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="e2e8f-108">Zorlamalı tünel, sanal özel ağ (VPN) tüneli kullanılarak yürütülür; Bu tünel, varsayılan bir site gerektirir, tüm Azure Internet 'e bağlı trafiğin yönlendirileceği yerel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="e2e8f-109">**Remove-AzVirtualNetworkGatewayDefaultSite** ağ geçidine atanmış olan varsayılan siteyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="e2e8f-110">Bunu yaparsanız, Zorlamalı tünel için kullanmadan önce yeni bir varsayılan site atamak için Set-AzVirtualNetworkGatewayDefaultSite kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="e2e8f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2e8f-111">EXAMPLES</span></span>

### <span data-ttu-id="e2e8f-112">Örnek 1: sanal ağ geçidine atanmış olan varsayılan siteyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="e2e8f-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="e2e8f-113">Bu örnekte, şu anda ContosoVirtualGateway adındaki sanal ağ ağ geçidine atanmış olan varsayılan site kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="e2e8f-114">İlk komut ağ geçidine nesne başvurusu oluşturmak için **Get-AzVirtualNetworkGateway** kullanır; Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="e2e8f-115">İkinci komut, bu ağ geçidine atanmış olan varsayılan siteyi kaldırmak için **Remove-AzVirtualNetworkGatewayDefaultSite** kullanır.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="e2e8f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2e8f-116">PARAMETERS</span></span>

### <span data-ttu-id="e2e8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e8f-117">-DefaultProfile</span></span>
<span data-ttu-id="e2e8f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2e8f-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2e8f-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="e2e8f-120">Kaldırılacak varsayılan siteyi içeren sanal ağ ağ geçidinin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="e2e8f-121">Sanal ağ geçidi için Get-AzVirtualNetworkGateway kullanarak ve ağ geçidinin adını belirterek bir nesne başvurusu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e8f-122">CommonParameters</span></span>
<span data-ttu-id="e2e8f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e8f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e8f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e8f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2e8f-125">INPUTS</span></span>

### <span data-ttu-id="e2e8f-126">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2e8f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e2e8f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2e8f-127">OUTPUTS</span></span>

### <span data-ttu-id="e2e8f-128">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2e8f-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e2e8f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2e8f-129">NOTES</span></span>

## <span data-ttu-id="e2e8f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2e8f-130">RELATED LINKS</span></span>

[<span data-ttu-id="e2e8f-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2e8f-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e2e8f-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e2e8f-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)

