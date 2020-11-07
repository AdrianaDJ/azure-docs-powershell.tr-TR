---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935668"
---
# <span data-ttu-id="bcd0a-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bcd0a-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bcd0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcd0a-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd0a-103">Uygulama ağ geçidine kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="bcd0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcd0a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcd0a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcd0a-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd0a-106">**Add-AzApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidine kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="bcd0a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcd0a-107">EXAMPLES</span></span>

### <span data-ttu-id="bcd0a-108">2</span><span class="sxs-lookup"><span data-stu-id="bcd0a-108">1:</span></span>
```

```

## <span data-ttu-id="bcd0a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcd0a-109">PARAMETERS</span></span>

### <span data-ttu-id="bcd0a-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcd0a-110">-ApplicationGateway</span></span>
<span data-ttu-id="bcd0a-111">Bu cmdlet 'in kimlik doğrulama sertifikası eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="bcd0a-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bcd0a-112">-CertificateFile</span></span>
<span data-ttu-id="bcd0a-113">Bu cmdlet 'in eklediği kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="bcd0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd0a-114">-DefaultProfile</span></span>
<span data-ttu-id="bcd0a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd0a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="bcd0a-116">-Name</span></span>
<span data-ttu-id="bcd0a-117">Bu cmdlet 'in uygulama ağ geçidine eklediği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="bcd0a-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="bcd0a-118">-Confirm</span></span>
<span data-ttu-id="bcd0a-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcd0a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd0a-120">-WhatIf</span></span>
<span data-ttu-id="bcd0a-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcd0a-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcd0a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd0a-123">CommonParameters</span></span>
<span data-ttu-id="bcd0a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcd0a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd0a-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd0a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd0a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcd0a-126">INPUTS</span></span>

### <span data-ttu-id="bcd0a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bcd0a-127">System.String</span></span>

## <span data-ttu-id="bcd0a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcd0a-128">OUTPUTS</span></span>

### <span data-ttu-id="bcd0a-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcd0a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bcd0a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcd0a-130">NOTES</span></span>
* <span data-ttu-id="bcd0a-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="bcd0a-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bcd0a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcd0a-132">RELATED LINKS</span></span>

[<span data-ttu-id="bcd0a-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bcd0a-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bcd0a-134">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bcd0a-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bcd0a-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bcd0a-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bcd0a-136">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bcd0a-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


