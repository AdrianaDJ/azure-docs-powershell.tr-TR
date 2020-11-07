---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940013"
---
# <span data-ttu-id="15b5d-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15b5d-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="15b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="15b5d-103">Uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="15b5d-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15b5d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15b5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="15b5d-106">**Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="15b5d-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="15b5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15b5d-107">EXAMPLES</span></span>

### <span data-ttu-id="15b5d-108">2</span><span class="sxs-lookup"><span data-stu-id="15b5d-108">1:</span></span>
```

```

## <span data-ttu-id="15b5d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15b5d-109">PARAMETERS</span></span>

### <span data-ttu-id="15b5d-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b5d-110">-ApplicationGateway</span></span>
<span data-ttu-id="15b5d-111">Bu cmdlet 'in kimlik doğrulama sertifikasını güncelleştirdiği uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15b5d-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="15b5d-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="15b5d-112">-CertificateFile</span></span>
<span data-ttu-id="15b5d-113">Bu cmdlet 'in sertifikayı güncelleştirdiği kimlik doğrulama sertifikası dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15b5d-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b5d-114">-DefaultProfile</span></span>
<span data-ttu-id="15b5d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15b5d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b5d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="15b5d-116">-Name</span></span>
<span data-ttu-id="15b5d-117">Bu cmdlet 'in güncelleştirdiği kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15b5d-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b5d-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="15b5d-118">-Confirm</span></span>
<span data-ttu-id="15b5d-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15b5d-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b5d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b5d-120">-WhatIf</span></span>
<span data-ttu-id="15b5d-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15b5d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b5d-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15b5d-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b5d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b5d-123">CommonParameters</span></span>
<span data-ttu-id="15b5d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15b5d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b5d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b5d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b5d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15b5d-126">INPUTS</span></span>

### <span data-ttu-id="15b5d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="15b5d-127">System.String</span></span>

## <span data-ttu-id="15b5d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15b5d-128">OUTPUTS</span></span>

### <span data-ttu-id="15b5d-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b5d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15b5d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15b5d-130">NOTES</span></span>
* <span data-ttu-id="15b5d-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="15b5d-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="15b5d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15b5d-132">RELATED LINKS</span></span>

[<span data-ttu-id="15b5d-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15b5d-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="15b5d-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15b5d-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="15b5d-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15b5d-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="15b5d-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15b5d-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


