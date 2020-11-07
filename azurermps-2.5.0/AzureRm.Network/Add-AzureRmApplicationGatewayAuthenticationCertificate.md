---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939543"
---
# <span data-ttu-id="2eff3-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2eff3-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2eff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eff3-102">SYNOPSIS</span></span>
<span data-ttu-id="2eff3-103">Uygulama ağ geçidine kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="2eff3-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eff3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2eff3-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2eff3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2eff3-105">DESCRIPTION</span></span>
<span data-ttu-id="2eff3-106">**Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure Application Gateway 'e kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="2eff3-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="2eff3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2eff3-107">EXAMPLES</span></span>

### <span data-ttu-id="2eff3-108">2</span><span class="sxs-lookup"><span data-stu-id="2eff3-108">1:</span></span>
```

```

## <span data-ttu-id="2eff3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2eff3-109">PARAMETERS</span></span>

### <span data-ttu-id="2eff3-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2eff3-110">-ApplicationGateway</span></span>
<span data-ttu-id="2eff3-111">Bu cmdlet 'in kimlik doğrulama sertifikası eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2eff3-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="2eff3-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2eff3-112">-CertificateFile</span></span>
<span data-ttu-id="2eff3-113">Bu cmdlet 'in eklediği kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2eff3-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="2eff3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eff3-114">-DefaultProfile</span></span>
<span data-ttu-id="2eff3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2eff3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eff3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2eff3-116">-Name</span></span>
<span data-ttu-id="2eff3-117">Bu cmdlet 'in uygulama ağ geçidine eklediği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2eff3-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="2eff3-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="2eff3-118">-Confirm</span></span>
<span data-ttu-id="2eff3-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2eff3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eff3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eff3-120">-WhatIf</span></span>
<span data-ttu-id="2eff3-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2eff3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eff3-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2eff3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eff3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eff3-123">CommonParameters</span></span>
<span data-ttu-id="2eff3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2eff3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eff3-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eff3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eff3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2eff3-126">INPUTS</span></span>

### <span data-ttu-id="2eff3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2eff3-127">System.String</span></span>

## <span data-ttu-id="2eff3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2eff3-128">OUTPUTS</span></span>

### <span data-ttu-id="2eff3-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2eff3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2eff3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2eff3-130">NOTES</span></span>
* <span data-ttu-id="2eff3-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="2eff3-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2eff3-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2eff3-132">RELATED LINKS</span></span>

[<span data-ttu-id="2eff3-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2eff3-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2eff3-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2eff3-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2eff3-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2eff3-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2eff3-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2eff3-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


