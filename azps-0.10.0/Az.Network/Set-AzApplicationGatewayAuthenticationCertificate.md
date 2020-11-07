---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936583"
---
# <span data-ttu-id="356cd-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="356cd-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="356cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="356cd-102">SYNOPSIS</span></span>
<span data-ttu-id="356cd-103">Uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="356cd-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="356cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="356cd-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="356cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="356cd-105">DESCRIPTION</span></span>
<span data-ttu-id="356cd-106">**Set-AzApplicationGatewayAuthenticationCertificate** cmdlet 'i, bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="356cd-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="356cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="356cd-107">EXAMPLES</span></span>

### <span data-ttu-id="356cd-108">2</span><span class="sxs-lookup"><span data-stu-id="356cd-108">1:</span></span>
```

```

## <span data-ttu-id="356cd-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="356cd-109">PARAMETERS</span></span>

### <span data-ttu-id="356cd-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356cd-110">-ApplicationGateway</span></span>
<span data-ttu-id="356cd-111">Bu cmdlet 'in kimlik doğrulama sertifikasını güncelleştirdiği uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="356cd-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="356cd-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="356cd-112">-CertificateFile</span></span>
<span data-ttu-id="356cd-113">Bu cmdlet 'in sertifikayı güncelleştirdiği kimlik doğrulama sertifikası dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="356cd-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="356cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356cd-114">-DefaultProfile</span></span>
<span data-ttu-id="356cd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="356cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="356cd-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="356cd-116">-Name</span></span>
<span data-ttu-id="356cd-117">Bu cmdlet 'in güncelleştirdiği kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="356cd-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="356cd-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="356cd-118">-Confirm</span></span>
<span data-ttu-id="356cd-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="356cd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356cd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356cd-120">-WhatIf</span></span>
<span data-ttu-id="356cd-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="356cd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="356cd-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="356cd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356cd-123">CommonParameters</span></span>
<span data-ttu-id="356cd-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="356cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356cd-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="356cd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356cd-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="356cd-126">INPUTS</span></span>

### <span data-ttu-id="356cd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="356cd-127">System.String</span></span>

## <span data-ttu-id="356cd-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="356cd-128">OUTPUTS</span></span>

### <span data-ttu-id="356cd-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356cd-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="356cd-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="356cd-130">NOTES</span></span>
* <span data-ttu-id="356cd-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="356cd-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="356cd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="356cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="356cd-133">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="356cd-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="356cd-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="356cd-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="356cd-135">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="356cd-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="356cd-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="356cd-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


