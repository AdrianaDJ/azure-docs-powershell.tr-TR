---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bb37c72368832ee4bbccb6e4c10a227e72ba127f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760217"
---
# <span data-ttu-id="fa48e-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fa48e-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="fa48e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa48e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa48e-103">Uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa48e-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="fa48e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa48e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa48e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa48e-105">DESCRIPTION</span></span>
<span data-ttu-id="fa48e-106">**Remove-Azapplicationgatewayfrontenvseçport** cmdlet 'i, bir Azure uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa48e-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="fa48e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa48e-107">EXAMPLES</span></span>

### <span data-ttu-id="fa48e-108">Örnek: uygulama ağ geçidinden ön uç bağlantı noktasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fa48e-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="fa48e-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve ağ geçidini $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fa48e-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="fa48e-110">İkinci komut FrontEndPort02 adındaki bağlantı noktasını uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa48e-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="fa48e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa48e-111">PARAMETERS</span></span>

### <span data-ttu-id="fa48e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa48e-112">-ApplicationGateway</span></span>
<span data-ttu-id="fa48e-113">Ön uç bağlantı noktasının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa48e-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="fa48e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa48e-114">-DefaultProfile</span></span>
<span data-ttu-id="fa48e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa48e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa48e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa48e-116">-Name</span></span>
<span data-ttu-id="fa48e-117">Kaldırılacak ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa48e-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="fa48e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa48e-118">CommonParameters</span></span>
<span data-ttu-id="fa48e-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa48e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa48e-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa48e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa48e-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa48e-121">INPUTS</span></span>

### <span data-ttu-id="fa48e-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa48e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fa48e-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa48e-123">OUTPUTS</span></span>

### <span data-ttu-id="fa48e-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa48e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fa48e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa48e-125">NOTES</span></span>

## <span data-ttu-id="fa48e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa48e-126">RELATED LINKS</span></span>

[<span data-ttu-id="fa48e-127">Add-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="fa48e-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fa48e-128">Get-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="fa48e-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fa48e-129">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="fa48e-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fa48e-130">Set-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="fa48e-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


