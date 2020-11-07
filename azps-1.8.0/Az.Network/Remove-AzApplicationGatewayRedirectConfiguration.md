---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760205"
---
# <span data-ttu-id="daaaf-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daaaf-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="daaaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="daaaf-103">Varolan bir uygulama ağ geçidinden yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="daaaf-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="daaaf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="daaaf-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daaaf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="daaaf-105">DESCRIPTION</span></span>
<span data-ttu-id="daaaf-106">**Remove-AzApplicationGatewayRedirectConfiguration** cmdlet 'i, varolan uygulama ağ geçidinden yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="daaaf-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="daaaf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="daaaf-107">EXAMPLES</span></span>

### <span data-ttu-id="daaaf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="daaaf-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="daaaf-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="daaaf-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="daaaf-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Redirect01 adlı yeniden yönlendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="daaaf-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="daaaf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="daaaf-111">PARAMETERS</span></span>

### <span data-ttu-id="daaaf-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daaaf-112">-ApplicationGateway</span></span>
<span data-ttu-id="daaaf-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daaaf-113">The applicationGateway</span></span>

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

### <span data-ttu-id="daaaf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daaaf-114">-DefaultProfile</span></span>
<span data-ttu-id="daaaf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="daaaf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daaaf-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="daaaf-116">-Name</span></span>
<span data-ttu-id="daaaf-117">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="daaaf-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="daaaf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daaaf-118">CommonParameters</span></span>
<span data-ttu-id="daaaf-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="daaaf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daaaf-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daaaf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daaaf-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="daaaf-121">INPUTS</span></span>

### <span data-ttu-id="daaaf-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daaaf-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daaaf-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="daaaf-123">OUTPUTS</span></span>

### <span data-ttu-id="daaaf-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daaaf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daaaf-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="daaaf-125">NOTES</span></span>

## <span data-ttu-id="daaaf-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="daaaf-126">RELATED LINKS</span></span>

[<span data-ttu-id="daaaf-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daaaf-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="daaaf-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daaaf-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="daaaf-129">Yeni-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daaaf-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="daaaf-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daaaf-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)