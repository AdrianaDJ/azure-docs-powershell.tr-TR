---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bec9d197d039ea3934607ee291bdd6511ae6f4a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592090"
---
# <span data-ttu-id="4573b-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4573b-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4573b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4573b-102">SYNOPSIS</span></span>
<span data-ttu-id="4573b-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="4573b-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4573b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4573b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4573b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4573b-105">DESCRIPTION</span></span>
<span data-ttu-id="4573b-106">**Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure Application Gateway için kimlik doğrulama sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="4573b-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4573b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4573b-107">EXAMPLES</span></span>

## <span data-ttu-id="4573b-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4573b-108">PARAMETERS</span></span>

### <span data-ttu-id="4573b-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4573b-109">-ApplicationGateway</span></span>
<span data-ttu-id="4573b-110">Bu cmdlet 'in kimlik doğrulama sertifikası aldığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4573b-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="4573b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4573b-111">-DefaultProfile</span></span>
<span data-ttu-id="4573b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4573b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4573b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4573b-113">-Name</span></span>
<span data-ttu-id="4573b-114">Bu cmdlet 'in aldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4573b-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4573b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4573b-115">CommonParameters</span></span>
<span data-ttu-id="4573b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4573b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4573b-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4573b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4573b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4573b-118">INPUTS</span></span>

### <span data-ttu-id="4573b-119">System. String</span><span class="sxs-lookup"><span data-stu-id="4573b-119">System.String</span></span>

## <span data-ttu-id="4573b-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4573b-120">OUTPUTS</span></span>

### <span data-ttu-id="4573b-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4573b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4573b-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4573b-122">NOTES</span></span>
* <span data-ttu-id="4573b-123">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="4573b-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4573b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4573b-124">RELATED LINKS</span></span>

[<span data-ttu-id="4573b-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4573b-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4573b-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4573b-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4573b-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4573b-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4573b-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4573b-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)

