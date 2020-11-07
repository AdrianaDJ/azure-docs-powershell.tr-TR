---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940103"
---
# <span data-ttu-id="8d8af-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d8af-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8d8af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d8af-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8af-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="8d8af-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d8af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d8af-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d8af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d8af-105">DESCRIPTION</span></span>
<span data-ttu-id="8d8af-106">**Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure Application Gateway için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="8d8af-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8d8af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d8af-107">EXAMPLES</span></span>

### <span data-ttu-id="8d8af-108">2</span><span class="sxs-lookup"><span data-stu-id="8d8af-108">1:</span></span>
```

```

## <span data-ttu-id="8d8af-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d8af-109">PARAMETERS</span></span>

### <span data-ttu-id="8d8af-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d8af-110">-ApplicationGateway</span></span>
<span data-ttu-id="8d8af-111">Bu cmdlet 'in kimlik doğrulama sertifikası aldığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d8af-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="8d8af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8af-112">-DefaultProfile</span></span>
<span data-ttu-id="8d8af-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d8af-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d8af-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d8af-114">-Name</span></span>
<span data-ttu-id="8d8af-115">Bu cmdlet 'in aldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d8af-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8d8af-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8af-116">CommonParameters</span></span>
<span data-ttu-id="8d8af-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d8af-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8af-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d8af-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8af-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d8af-119">INPUTS</span></span>

### <span data-ttu-id="8d8af-120">System. String</span><span class="sxs-lookup"><span data-stu-id="8d8af-120">System.String</span></span>

## <span data-ttu-id="8d8af-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d8af-121">OUTPUTS</span></span>

### <span data-ttu-id="8d8af-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d8af-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8d8af-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d8af-123">NOTES</span></span>
* <span data-ttu-id="8d8af-124">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="8d8af-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8d8af-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d8af-125">RELATED LINKS</span></span>

[<span data-ttu-id="8d8af-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d8af-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d8af-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d8af-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d8af-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d8af-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d8af-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d8af-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


