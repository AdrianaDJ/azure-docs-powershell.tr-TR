---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2d1ac2c3e5705a4214e211bf7db9af89d432a393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764981"
---
# <span data-ttu-id="f6b6d-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f6b6d-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="f6b6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b6d-103">Uygulama ağ geçidinden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6b6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6b6d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6b6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6b6d-105">DESCRIPTION</span></span>
<span data-ttu-id="f6b6d-106">**Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet 'ı bir Azure uygulama ağ geçidinden ön uç IP 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="f6b6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6b6d-107">EXAMPLES</span></span>

### <span data-ttu-id="f6b6d-108">Örnek 1: ön uç IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f6b6d-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="f6b6d-109">İlk komut ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f6b6d-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden FrontEndIP02 adlı ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f6b6d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6b6d-111">PARAMETERS</span></span>

### <span data-ttu-id="f6b6d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6b6d-112">-ApplicationGateway</span></span>
<span data-ttu-id="f6b6d-113">Ön uç IP yapılandırmasının kaldırılacağı bir uygulama ağ geçidi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f6b6d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b6d-114">-DefaultProfile</span></span>
<span data-ttu-id="f6b6d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6b6d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6b6d-116">-Name</span></span>
<span data-ttu-id="f6b6d-117">Kaldırılacak ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="f6b6d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b6d-118">CommonParameters</span></span>
<span data-ttu-id="f6b6d-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6b6d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b6d-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b6d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b6d-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6b6d-121">INPUTS</span></span>

### <span data-ttu-id="f6b6d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f6b6d-122">System.String</span></span>

## <span data-ttu-id="f6b6d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6b6d-123">OUTPUTS</span></span>

### <span data-ttu-id="f6b6d-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6b6d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6b6d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6b6d-125">NOTES</span></span>

## <span data-ttu-id="f6b6d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6b6d-126">RELATED LINKS</span></span>

[<span data-ttu-id="f6b6d-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f6b6d-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f6b6d-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f6b6d-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f6b6d-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f6b6d-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f6b6d-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f6b6d-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


