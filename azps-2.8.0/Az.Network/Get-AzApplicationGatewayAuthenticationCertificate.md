---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1743ed0427fdc0dd952c9b86d51c13c3ed855620
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931816"
---
# <span data-ttu-id="d7330-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7330-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d7330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7330-102">SYNOPSIS</span></span>
<span data-ttu-id="d7330-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="d7330-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="d7330-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7330-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7330-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7330-105">DESCRIPTION</span></span>
<span data-ttu-id="d7330-106">**Get-AzApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="d7330-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d7330-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7330-107">EXAMPLES</span></span>

### <span data-ttu-id="d7330-108">Örnek 1: belirtilen kimlik doğrulama sertifikasını alma</span><span class="sxs-lookup"><span data-stu-id="d7330-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="d7330-109">İlk komut appGwName adlı uygulama ağ geçidini alır ve $appgw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d7330-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="d7330-110">İkinci komut pool01 adındaki kimlik doğrulama sertifikasını alır ve $pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d7330-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="d7330-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7330-111">PARAMETERS</span></span>

### <span data-ttu-id="d7330-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7330-112">-ApplicationGateway</span></span>
<span data-ttu-id="d7330-113">Bu cmdlet 'in kimlik doğrulama sertifikası aldığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7330-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="d7330-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7330-114">-DefaultProfile</span></span>
<span data-ttu-id="d7330-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7330-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7330-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7330-116">-Name</span></span>
<span data-ttu-id="d7330-117">Bu cmdlet 'in aldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7330-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d7330-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7330-118">CommonParameters</span></span>
<span data-ttu-id="d7330-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7330-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7330-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7330-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7330-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7330-121">INPUTS</span></span>

### <span data-ttu-id="d7330-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7330-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7330-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7330-123">OUTPUTS</span></span>

### <span data-ttu-id="d7330-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7330-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d7330-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7330-125">NOTES</span></span>
* <span data-ttu-id="d7330-126">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="d7330-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d7330-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7330-127">RELATED LINKS</span></span>

[<span data-ttu-id="d7330-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7330-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d7330-129">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7330-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d7330-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7330-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d7330-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7330-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


