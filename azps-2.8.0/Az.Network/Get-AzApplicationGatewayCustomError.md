---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: fbf10b3cfc323a25a7d7a63dc047a4b24141c5d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932062"
---
# <span data-ttu-id="9e9e0-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9e9e0-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9e9e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9e0-103">Uygulama ağ geçidinden özel hataları alır.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="9e9e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e9e0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e9e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e9e0-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9e0-106">**Get-AzApplicationGatewayCustomError** cmdlet 'i uygulama ağ geçidinden özel hataları alıyor.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="9e9e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e9e0-107">EXAMPLES</span></span>

### <span data-ttu-id="9e9e0-108">Örnek 1: uygulama ağ geçidinde özel hata alır</span><span class="sxs-lookup"><span data-stu-id="9e9e0-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="9e9e0-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="9e9e0-110">Örnek 2: uygulama ağ geçidinde tüm özel hataların listesini alır</span><span class="sxs-lookup"><span data-stu-id="9e9e0-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="9e9e0-111">Bu komut, uygulama ağ geçidi $appgw tüm özel hataların listesini alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="9e9e0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e9e0-112">PARAMETERS</span></span>

### <span data-ttu-id="9e9e0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e9e0-113">-ApplicationGateway</span></span>
<span data-ttu-id="9e9e0-114">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="9e9e0-114">The Application Gateway</span></span>

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

### <span data-ttu-id="9e9e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9e0-115">-DefaultProfile</span></span>
<span data-ttu-id="9e9e0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e9e0-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9e9e0-117">-StatusCode</span></span>
<span data-ttu-id="9e9e0-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9e9e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9e0-119">CommonParameters</span></span>
<span data-ttu-id="9e9e0-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9e0-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9e9e0-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9e0-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e9e0-122">INPUTS</span></span>

### <span data-ttu-id="9e9e0-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e9e0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e9e0-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e9e0-124">OUTPUTS</span></span>

### <span data-ttu-id="9e9e0-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9e9e0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9e9e0-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e9e0-126">NOTES</span></span>

## <span data-ttu-id="9e9e0-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e9e0-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e9e0-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9e9e0-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9e9e0-129">Yeni-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9e9e0-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9e9e0-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9e9e0-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9e9e0-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9e9e0-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
