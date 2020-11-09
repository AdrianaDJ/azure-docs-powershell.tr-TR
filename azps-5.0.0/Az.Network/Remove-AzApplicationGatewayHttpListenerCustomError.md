---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325282"
---
# <span data-ttu-id="bc25e-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bc25e-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="bc25e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc25e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc25e-103">Uygulama ağ geçidi 'nin http dinleyicisinde özel bir hatayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc25e-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="bc25e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc25e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc25e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc25e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc25e-106">**Remove-AzApplicationGatewayCustomError** cmdlet 'i, uygulama ağ geçidinin http dinleyicisinde özel bir hatayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc25e-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="bc25e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc25e-107">EXAMPLES</span></span>

### <span data-ttu-id="bc25e-108">Örnek 1: http dinleyicisinin özel hatasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="bc25e-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="bc25e-109">Bu komut http dinleyici $listener 502 özel hatasını kaldırır ve güncelleştirilmiş dinleyiciyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="bc25e-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="bc25e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc25e-110">PARAMETERS</span></span>

### <span data-ttu-id="bc25e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc25e-111">-DefaultProfile</span></span>
<span data-ttu-id="bc25e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc25e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc25e-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="bc25e-113">-HttpListener</span></span>
<span data-ttu-id="bc25e-114">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="bc25e-114">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc25e-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bc25e-115">-StatusCode</span></span>
<span data-ttu-id="bc25e-116">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="bc25e-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bc25e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc25e-117">CommonParameters</span></span>
<span data-ttu-id="bc25e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc25e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc25e-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc25e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc25e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc25e-120">INPUTS</span></span>

### <span data-ttu-id="bc25e-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bc25e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bc25e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc25e-122">OUTPUTS</span></span>

### <span data-ttu-id="bc25e-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bc25e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bc25e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc25e-124">NOTES</span></span>

## <span data-ttu-id="bc25e-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc25e-125">RELATED LINKS</span></span>

[<span data-ttu-id="bc25e-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bc25e-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="bc25e-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bc25e-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="bc25e-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bc25e-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
