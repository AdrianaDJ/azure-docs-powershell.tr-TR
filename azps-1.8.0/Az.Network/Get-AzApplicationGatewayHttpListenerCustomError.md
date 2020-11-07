---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 58cef33d6e7c05167376fe81a7c3b1e3f464f407
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760646"
---
# <span data-ttu-id="56aa3-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="56aa3-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="56aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="56aa3-103">Uygulama ağ geçidi 'nin http dinleyicisinde özel hataları alır.</span><span class="sxs-lookup"><span data-stu-id="56aa3-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="56aa3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56aa3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56aa3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="56aa3-106">**Get-AzApplicationGatewayCustomError** cmdlet 'i, bir uygulama ağ geçidinin http dinleyicisinde özel hatalar alıyor.</span><span class="sxs-lookup"><span data-stu-id="56aa3-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="56aa3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="56aa3-108">Örnek 1: http dinleyicisinde özel hata alır</span><span class="sxs-lookup"><span data-stu-id="56aa3-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="56aa3-109">Bu komut HTTP dinleyicisinin $listener 502 http dinleyicisi özel hatasını alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="56aa3-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="56aa3-110">Örnek 2: http dinleyicisinde tüm özel hataların listesini alır</span><span class="sxs-lookup"><span data-stu-id="56aa3-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="56aa3-111">Bu komut, http dinleyici $listener tüm özel hataların listesini alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="56aa3-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="56aa3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56aa3-112">PARAMETERS</span></span>

### <span data-ttu-id="56aa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56aa3-113">-DefaultProfile</span></span>
<span data-ttu-id="56aa3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56aa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56aa3-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="56aa3-115">-HttpListener</span></span>
<span data-ttu-id="56aa3-116">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="56aa3-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="56aa3-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="56aa3-117">-StatusCode</span></span>
<span data-ttu-id="56aa3-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="56aa3-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="56aa3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56aa3-119">CommonParameters</span></span>
<span data-ttu-id="56aa3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56aa3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56aa3-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="56aa3-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56aa3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56aa3-122">INPUTS</span></span>

### <span data-ttu-id="56aa3-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="56aa3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="56aa3-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56aa3-124">OUTPUTS</span></span>

### <span data-ttu-id="56aa3-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="56aa3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="56aa3-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56aa3-126">NOTES</span></span>

## <span data-ttu-id="56aa3-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56aa3-127">RELATED LINKS</span></span>

[<span data-ttu-id="56aa3-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="56aa3-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="56aa3-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="56aa3-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="56aa3-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="56aa3-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
