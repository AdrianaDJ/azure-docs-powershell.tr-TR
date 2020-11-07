---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cf8d7453961796afb4b0aa94d549d80eb9279ab5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760052"
---
# <span data-ttu-id="f44ef-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f44ef-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f44ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f44ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f44ef-103">Uygulama ağ geçidinin http dinleyicisinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f44ef-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="f44ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f44ef-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f44ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f44ef-105">DESCRIPTION</span></span>
<span data-ttu-id="f44ef-106">**Set-AzApplicationGatewayCustomError** cmdlet 'i, uygulama ağ geçidinin http dinleyicisinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f44ef-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="f44ef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f44ef-107">EXAMPLES</span></span>

### <span data-ttu-id="f44ef-108">Örnek 1: http dinleyicisinde özel bir hatayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f44ef-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f44ef-109">Bu komut, http dinleyicisi $listener 502 özel hatasını güncelleştirir ve güncelleştirilmiş dinleyiciyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f44ef-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="f44ef-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f44ef-110">PARAMETERS</span></span>

### <span data-ttu-id="f44ef-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f44ef-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f44ef-112">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="f44ef-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f44ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44ef-113">-DefaultProfile</span></span>
<span data-ttu-id="f44ef-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f44ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f44ef-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f44ef-115">-HttpListener</span></span>
<span data-ttu-id="f44ef-116">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="f44ef-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f44ef-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f44ef-117">-StatusCode</span></span>
<span data-ttu-id="f44ef-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="f44ef-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f44ef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44ef-119">CommonParameters</span></span>
<span data-ttu-id="f44ef-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f44ef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44ef-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44ef-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44ef-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f44ef-122">INPUTS</span></span>

### <span data-ttu-id="f44ef-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f44ef-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f44ef-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f44ef-124">OUTPUTS</span></span>

### <span data-ttu-id="f44ef-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f44ef-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f44ef-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f44ef-126">NOTES</span></span>

## <span data-ttu-id="f44ef-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f44ef-127">RELATED LINKS</span></span>

[<span data-ttu-id="f44ef-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f44ef-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f44ef-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f44ef-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f44ef-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f44ef-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
