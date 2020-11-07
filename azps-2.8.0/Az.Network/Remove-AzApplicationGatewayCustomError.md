---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c92c3c6b66e1b1208c7a0425b27a7e966bf6689
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918135"
---
# <span data-ttu-id="9d5e0-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d5e0-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9d5e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5e0-103">Uygulama ağ geçidinden özel bir hatayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9d5e0-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="9d5e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d5e0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d5e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d5e0-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5e0-106">**Remove-AzApplicationGatewayCustomError** cmdlet 'i uygulama ağ geçidinden özel bir hatayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9d5e0-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="9d5e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d5e0-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5e0-108">Örnek 1: özel hatayı uygulama ağ geçidinden kaldırır</span><span class="sxs-lookup"><span data-stu-id="9d5e0-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="9d5e0-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını kaldırır ve güncelleştirilmiş ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9d5e0-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="9d5e0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d5e0-110">PARAMETERS</span></span>

### <span data-ttu-id="9d5e0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d5e0-111">-ApplicationGateway</span></span>
<span data-ttu-id="9d5e0-112">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="9d5e0-112">The Application Gateway</span></span>

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

### <span data-ttu-id="9d5e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5e0-113">-DefaultProfile</span></span>
<span data-ttu-id="9d5e0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d5e0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d5e0-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9d5e0-115">-StatusCode</span></span>
<span data-ttu-id="9d5e0-116">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="9d5e0-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9d5e0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5e0-117">CommonParameters</span></span>
<span data-ttu-id="9d5e0-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d5e0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5e0-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5e0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5e0-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d5e0-120">INPUTS</span></span>

### <span data-ttu-id="9d5e0-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d5e0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d5e0-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d5e0-122">OUTPUTS</span></span>

### <span data-ttu-id="9d5e0-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d5e0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9d5e0-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d5e0-124">NOTES</span></span>

## <span data-ttu-id="9d5e0-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d5e0-125">RELATED LINKS</span></span>

[<span data-ttu-id="9d5e0-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d5e0-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9d5e0-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d5e0-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9d5e0-128">Yeni-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d5e0-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9d5e0-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9d5e0-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
