---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 317fd5bf8306416ad4cbef3d1fb64d56d556ed1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590440"
---
# <span data-ttu-id="f6283-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6283-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f6283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6283-102">SYNOPSIS</span></span>
<span data-ttu-id="f6283-103">Uygulama ağ geçidine kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="f6283-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6283-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6283-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6283-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6283-105">DESCRIPTION</span></span>
<span data-ttu-id="f6283-106">**Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure Application Gateway 'e kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="f6283-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="f6283-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6283-107">EXAMPLES</span></span>

## <span data-ttu-id="f6283-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6283-108">PARAMETERS</span></span>

### <span data-ttu-id="f6283-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6283-109">-ApplicationGateway</span></span>
<span data-ttu-id="f6283-110">Bu cmdlet 'in kimlik doğrulama sertifikası eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="f6283-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f6283-111">-CertificateFile</span></span>
<span data-ttu-id="f6283-112">Bu cmdlet 'in eklediği kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f6283-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6283-113">-DefaultProfile</span></span>
<span data-ttu-id="f6283-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6283-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6283-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6283-115">-Name</span></span>
<span data-ttu-id="f6283-116">Bu cmdlet 'in uygulama ağ geçidine eklediği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="f6283-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6283-117">-Confirm</span></span>
<span data-ttu-id="f6283-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6283-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6283-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6283-119">-WhatIf</span></span>
<span data-ttu-id="f6283-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6283-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6283-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6283-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6283-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6283-122">CommonParameters</span></span>
<span data-ttu-id="f6283-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6283-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6283-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6283-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6283-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6283-125">INPUTS</span></span>

### <span data-ttu-id="f6283-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f6283-126">System.String</span></span>

## <span data-ttu-id="f6283-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6283-127">OUTPUTS</span></span>

### <span data-ttu-id="f6283-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6283-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6283-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6283-129">NOTES</span></span>
* <span data-ttu-id="f6283-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="f6283-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f6283-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6283-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6283-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6283-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f6283-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6283-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f6283-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6283-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f6283-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6283-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


