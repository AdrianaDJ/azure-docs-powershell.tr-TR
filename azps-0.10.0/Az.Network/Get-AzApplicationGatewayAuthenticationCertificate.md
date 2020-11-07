---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935604"
---
# <span data-ttu-id="dd699-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dd699-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="dd699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd699-102">SYNOPSIS</span></span>
<span data-ttu-id="dd699-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="dd699-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="dd699-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd699-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd699-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd699-105">DESCRIPTION</span></span>
<span data-ttu-id="dd699-106">**Get-AzApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="dd699-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="dd699-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd699-107">EXAMPLES</span></span>

### <span data-ttu-id="dd699-108">2</span><span class="sxs-lookup"><span data-stu-id="dd699-108">1:</span></span>
```

```

## <span data-ttu-id="dd699-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd699-109">PARAMETERS</span></span>

### <span data-ttu-id="dd699-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd699-110">-ApplicationGateway</span></span>
<span data-ttu-id="dd699-111">Bu cmdlet 'in kimlik doğrulama sertifikası aldığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd699-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="dd699-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd699-112">-DefaultProfile</span></span>
<span data-ttu-id="dd699-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd699-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd699-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd699-114">-Name</span></span>
<span data-ttu-id="dd699-115">Bu cmdlet 'in aldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd699-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd699-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd699-116">CommonParameters</span></span>
<span data-ttu-id="dd699-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd699-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd699-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd699-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd699-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd699-119">INPUTS</span></span>

### <span data-ttu-id="dd699-120">System. String</span><span class="sxs-lookup"><span data-stu-id="dd699-120">System.String</span></span>

## <span data-ttu-id="dd699-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd699-121">OUTPUTS</span></span>

### <span data-ttu-id="dd699-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dd699-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="dd699-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd699-123">NOTES</span></span>
* <span data-ttu-id="dd699-124">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="dd699-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dd699-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd699-125">RELATED LINKS</span></span>

[<span data-ttu-id="dd699-126">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dd699-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dd699-127">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dd699-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dd699-128">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dd699-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dd699-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dd699-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


