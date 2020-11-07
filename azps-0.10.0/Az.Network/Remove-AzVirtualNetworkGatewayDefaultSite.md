---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: bfd90797ff60c42927b23424e3c100efd16a6d24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936601"
---
# <span data-ttu-id="b9db1-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b9db1-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="b9db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9db1-102">SYNOPSIS</span></span>
<span data-ttu-id="b9db1-103">Sanal ağ ağ geçidinden varsayılan siteyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b9db1-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="b9db1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9db1-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9db1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9db1-105">DESCRIPTION</span></span>
<span data-ttu-id="b9db1-106">**Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet 'i, Zorlamalı tünel varsayılan sitesini sanal ağ ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b9db1-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="b9db1-107">Zorlamalı tünel, Azure sanal makinelerden şirket içi ağınıza Internet 'e bağlı trafik yönlendirmenize yol sunar; Bu, göndermeden önce trafiği incelemenizi ve denetlemenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="b9db1-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="b9db1-108">Zorlamalı tünel, sanal özel ağ (VPN) tüneli kullanılarak yürütülür; Bu tünel, varsayılan bir site gerektirir, tüm Azure Internet 'e bağlı trafiğin yönlendirileceği yerel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="b9db1-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="b9db1-109">**Remove-AzVirtualNetworkGatewayDefaultSite** ağ geçidine atanmış olan varsayılan siteyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b9db1-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="b9db1-110">Bunu yaparsanız, Zorlamalı tünel için kullanmadan önce yeni bir varsayılan site atamak için Set-AzVirtualNetworkGatewayDefaultSite kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b9db1-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="b9db1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9db1-111">EXAMPLES</span></span>

### <span data-ttu-id="b9db1-112">Örnek 1: sanal ağ geçidine atanmış olan varsayılan siteyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="b9db1-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="b9db1-113">Bu örnekte, şu anda ContosoVirtualGateway adındaki sanal ağ ağ geçidine atanmış olan varsayılan site kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="b9db1-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="b9db1-114">İlk komut ağ geçidine nesne başvurusu oluşturmak için **Get-AzVirtualNetworkGateway** kullanır; Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="b9db1-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="b9db1-115">İkinci komut, bu ağ geçidine atanmış olan varsayılan siteyi kaldırmak için **Remove-AzVirtualNetworkGatewayDefaultSite** kullanır.</span><span class="sxs-lookup"><span data-stu-id="b9db1-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="b9db1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9db1-116">PARAMETERS</span></span>

### <span data-ttu-id="b9db1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9db1-117">-DefaultProfile</span></span>
<span data-ttu-id="b9db1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9db1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9db1-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9db1-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b9db1-120">Kaldırılacak varsayılan siteyi içeren sanal ağ ağ geçidinin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9db1-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="b9db1-121">Sanal ağ geçidi için Get-AzVirtualNetworkGateway kullanarak ve ağ geçidinin adını belirterek bir nesne başvurusu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9db1-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9db1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9db1-122">CommonParameters</span></span>
<span data-ttu-id="b9db1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9db1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9db1-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9db1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9db1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9db1-125">INPUTS</span></span>

###  
<span data-ttu-id="b9db1-126">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="b9db1-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b9db1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9db1-127">OUTPUTS</span></span>

###  
<span data-ttu-id="b9db1-128">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b9db1-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b9db1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9db1-129">NOTES</span></span>

## <span data-ttu-id="b9db1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9db1-130">RELATED LINKS</span></span>

[<span data-ttu-id="b9db1-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9db1-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b9db1-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b9db1-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


