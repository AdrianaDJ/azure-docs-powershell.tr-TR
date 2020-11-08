---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109533"
---
# <span data-ttu-id="90d4b-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="90d4b-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="90d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="90d4b-103">Uygulama ağ geçidine kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="90d4b-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="90d4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90d4b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d4b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="90d4b-106">**Add-AzApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidine kimlik doğrulama sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="90d4b-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="90d4b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90d4b-107">EXAMPLES</span></span>

### <span data-ttu-id="90d4b-108">Örnek 1: uygulama ağ geçidine kimlik doğrulama sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="90d4b-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="90d4b-109">İlk komut appGwName adlı bir uygulama ağ geçidini alır ve bunu $appgw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="90d4b-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="90d4b-110">İkinci komut cert01 adlı kimlik doğrulama sertifikasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="90d4b-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="90d4b-111">Üçüncü komut, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="90d4b-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="90d4b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90d4b-112">PARAMETERS</span></span>

### <span data-ttu-id="90d4b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90d4b-113">-ApplicationGateway</span></span>
<span data-ttu-id="90d4b-114">Bu cmdlet 'in kimlik doğrulama sertifikası eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90d4b-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="90d4b-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="90d4b-115">-CertificateFile</span></span>
<span data-ttu-id="90d4b-116">Bu cmdlet 'in eklediği kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="90d4b-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d4b-117">-DefaultProfile</span></span>
<span data-ttu-id="90d4b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90d4b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90d4b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="90d4b-119">-Name</span></span>
<span data-ttu-id="90d4b-120">Bu cmdlet 'in uygulama ağ geçidine eklediği sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90d4b-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d4b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="90d4b-121">-Confirm</span></span>
<span data-ttu-id="90d4b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90d4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d4b-123">-WhatIf</span></span>
<span data-ttu-id="90d4b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d4b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90d4b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90d4b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d4b-126">CommonParameters</span></span>
<span data-ttu-id="90d4b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90d4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d4b-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d4b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d4b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90d4b-129">INPUTS</span></span>

### <span data-ttu-id="90d4b-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90d4b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90d4b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90d4b-131">OUTPUTS</span></span>

### <span data-ttu-id="90d4b-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90d4b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90d4b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90d4b-133">NOTES</span></span>
* <span data-ttu-id="90d4b-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="90d4b-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="90d4b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90d4b-135">RELATED LINKS</span></span>

[<span data-ttu-id="90d4b-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="90d4b-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="90d4b-137">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="90d4b-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="90d4b-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="90d4b-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="90d4b-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="90d4b-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


