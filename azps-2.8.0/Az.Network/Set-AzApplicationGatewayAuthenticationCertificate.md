---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6e0194135b93898ea14998d92f8f23afd612f221
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917976"
---
# <span data-ttu-id="b7575-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7575-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b7575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7575-102">SYNOPSIS</span></span>
<span data-ttu-id="b7575-103">Uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7575-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b7575-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7575-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7575-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7575-105">DESCRIPTION</span></span>
<span data-ttu-id="b7575-106">**Set-AzApplicationGatewayAuthenticationCertificate** cmdlet 'i, bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7575-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b7575-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7575-107">EXAMPLES</span></span>

### <span data-ttu-id="b7575-108">Örnek 1: kimlik doğrulama sertifikasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b7575-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="b7575-109">İlk komut appGwName adlı uygulama ağ geçidini alır ve sonucu $appgw değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="b7575-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="b7575-110">İkinci komut, uygulama ağ geçidinde cert01 adındaki kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7575-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="b7575-111">Üçüncü komut, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b7575-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="b7575-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7575-112">PARAMETERS</span></span>

### <span data-ttu-id="b7575-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7575-113">-ApplicationGateway</span></span>
<span data-ttu-id="b7575-114">Bu cmdlet 'in kimlik doğrulama sertifikasını güncelleştirdiği uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7575-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="b7575-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b7575-115">-CertificateFile</span></span>
<span data-ttu-id="b7575-116">Bu cmdlet 'in sertifikayı güncelleştirdiği kimlik doğrulama sertifikası dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7575-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="b7575-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7575-117">-DefaultProfile</span></span>
<span data-ttu-id="b7575-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7575-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7575-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7575-119">-Name</span></span>
<span data-ttu-id="b7575-120">Bu cmdlet 'in güncelleştirdiği kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7575-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b7575-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7575-121">-Confirm</span></span>
<span data-ttu-id="b7575-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7575-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7575-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7575-123">-WhatIf</span></span>
<span data-ttu-id="b7575-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7575-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7575-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7575-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7575-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7575-126">CommonParameters</span></span>
<span data-ttu-id="b7575-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7575-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7575-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7575-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7575-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7575-129">INPUTS</span></span>

### <span data-ttu-id="b7575-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7575-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7575-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7575-131">OUTPUTS</span></span>

### <span data-ttu-id="b7575-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7575-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7575-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7575-133">NOTES</span></span>
* <span data-ttu-id="b7575-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="b7575-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b7575-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7575-135">RELATED LINKS</span></span>

[<span data-ttu-id="b7575-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7575-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b7575-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7575-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b7575-138">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7575-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b7575-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7575-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

