---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: ead8884b3594edc6377fc4c646c01e51dbe13439
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940049"
---
# <span data-ttu-id="9afb6-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9afb6-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="9afb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9afb6-102">SYNOPSIS</span></span>
<span data-ttu-id="9afb6-103">Uygulama ağ geçidinden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9afb6-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9afb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9afb6-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9afb6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9afb6-105">DESCRIPTION</span></span>
<span data-ttu-id="9afb6-106">**Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet 'ı bir Azure uygulama ağ geçidinden ön uç IP 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9afb6-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="9afb6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9afb6-107">EXAMPLES</span></span>

### <span data-ttu-id="9afb6-108">Örnek 1: ön uç IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="9afb6-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="9afb6-109">İlk komut ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9afb6-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9afb6-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden FrontEndIP02 adlı ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9afb6-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9afb6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9afb6-111">PARAMETERS</span></span>

### <span data-ttu-id="9afb6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9afb6-112">-ApplicationGateway</span></span>
<span data-ttu-id="9afb6-113">Ön uç IP yapılandırmasının kaldırılacağı bir uygulama ağ geçidi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9afb6-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9afb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afb6-114">-DefaultProfile</span></span>
<span data-ttu-id="9afb6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9afb6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9afb6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9afb6-116">-Name</span></span>
<span data-ttu-id="9afb6-117">Kaldırılacak ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9afb6-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="9afb6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afb6-118">CommonParameters</span></span>
<span data-ttu-id="9afb6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9afb6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afb6-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9afb6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afb6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9afb6-121">INPUTS</span></span>

### <span data-ttu-id="9afb6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9afb6-122">System.String</span></span>

## <span data-ttu-id="9afb6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9afb6-123">OUTPUTS</span></span>

### <span data-ttu-id="9afb6-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9afb6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9afb6-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9afb6-125">NOTES</span></span>

## <span data-ttu-id="9afb6-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9afb6-126">RELATED LINKS</span></span>

[<span data-ttu-id="9afb6-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9afb6-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9afb6-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9afb6-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9afb6-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9afb6-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9afb6-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9afb6-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


