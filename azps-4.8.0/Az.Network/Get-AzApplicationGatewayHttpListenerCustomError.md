---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267989"
---
# <span data-ttu-id="1654f-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1654f-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="1654f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1654f-102">SYNOPSIS</span></span>
<span data-ttu-id="1654f-103">Uygulama ağ geçidi 'nin http dinleyicisinde özel hataları alır.</span><span class="sxs-lookup"><span data-stu-id="1654f-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1654f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1654f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1654f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1654f-105">DESCRIPTION</span></span>
<span data-ttu-id="1654f-106">**Get-AzApplicationGatewayCustomError** cmdlet 'i, bir uygulama ağ geçidinin http dinleyicisinde özel hatalar alıyor.</span><span class="sxs-lookup"><span data-stu-id="1654f-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1654f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1654f-107">EXAMPLES</span></span>

### <span data-ttu-id="1654f-108">Örnek 1: http dinleyicisinde özel hata alır</span><span class="sxs-lookup"><span data-stu-id="1654f-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="1654f-109">Bu komut HTTP dinleyicisinin $listener 502 http dinleyicisi özel hatasını alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="1654f-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="1654f-110">Örnek 2: http dinleyicisinde tüm özel hataların listesini alır</span><span class="sxs-lookup"><span data-stu-id="1654f-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="1654f-111">Bu komut, http dinleyici $listener tüm özel hataların listesini alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="1654f-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="1654f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1654f-112">PARAMETERS</span></span>

### <span data-ttu-id="1654f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1654f-113">-DefaultProfile</span></span>
<span data-ttu-id="1654f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1654f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1654f-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="1654f-115">-HttpListener</span></span>
<span data-ttu-id="1654f-116">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="1654f-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="1654f-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1654f-117">-StatusCode</span></span>
<span data-ttu-id="1654f-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="1654f-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1654f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1654f-119">CommonParameters</span></span>
<span data-ttu-id="1654f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1654f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1654f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1654f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1654f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1654f-122">INPUTS</span></span>

### <span data-ttu-id="1654f-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1654f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1654f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1654f-124">OUTPUTS</span></span>

### <span data-ttu-id="1654f-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1654f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1654f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1654f-126">NOTES</span></span>

## <span data-ttu-id="1654f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1654f-127">RELATED LINKS</span></span>

[<span data-ttu-id="1654f-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1654f-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1654f-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1654f-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1654f-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1654f-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
