---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280005"
---
# <span data-ttu-id="fabe1-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fabe1-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="fabe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabe1-102">SYNOPSIS</span></span>
<span data-ttu-id="fabe1-103">Uygulama ağ geçidinin ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="fabe1-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="fabe1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fabe1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fabe1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fabe1-105">DESCRIPTION</span></span>
<span data-ttu-id="fabe1-106">**Get-Azapplicationgatewayfrontendıconfıg** cmdlet 'i, uygulama ağ geçidinin ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="fabe1-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="fabe1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fabe1-107">EXAMPLES</span></span>

### <span data-ttu-id="fabe1-108">Örnek 1: belirtilen ön uç IP yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="fabe1-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="fabe1-109">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, FrontEndIP01 adlı ön uç IP yapılandırmasını $AppGw ve $FrontEndIP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fabe1-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="fabe1-110">Örnek 2: ön uç IP yapılandırmalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="fabe1-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="fabe1-111">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw 'dan ön uç IP yapılandırmalarının bir listesini alır ve $FrontEndIPs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fabe1-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="fabe1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fabe1-112">PARAMETERS</span></span>

### <span data-ttu-id="fabe1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fabe1-113">-ApplicationGateway</span></span>
<span data-ttu-id="fabe1-114">Ön uç IP yapılandırmasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fabe1-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="fabe1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabe1-115">-DefaultProfile</span></span>
<span data-ttu-id="fabe1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fabe1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fabe1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="fabe1-117">-Name</span></span>
<span data-ttu-id="fabe1-118">Bu cmdlet 'in aldığı ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fabe1-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fabe1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabe1-119">CommonParameters</span></span>
<span data-ttu-id="fabe1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fabe1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabe1-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fabe1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabe1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fabe1-122">INPUTS</span></span>

### <span data-ttu-id="fabe1-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fabe1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fabe1-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fabe1-124">OUTPUTS</span></span>

### <span data-ttu-id="fabe1-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fabe1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="fabe1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fabe1-126">NOTES</span></span>

## <span data-ttu-id="fabe1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fabe1-127">RELATED LINKS</span></span>

[<span data-ttu-id="fabe1-128">Add-Azapplicationgatewayfrontendıconfıg yapılandırması</span><span class="sxs-lookup"><span data-stu-id="fabe1-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fabe1-129">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="fabe1-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fabe1-130">Remove-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="fabe1-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fabe1-131">Set-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="fabe1-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


