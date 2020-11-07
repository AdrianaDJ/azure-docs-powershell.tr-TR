---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a71ba6f6d9b45e0016589d5629f029998f33963f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765146"
---
# <span data-ttu-id="9bfa2-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9bfa2-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9bfa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bfa2-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfa2-103">Uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bfa2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bfa2-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bfa2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bfa2-105">DESCRIPTION</span></span>
<span data-ttu-id="9bfa2-106">**Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="9bfa2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bfa2-107">EXAMPLES</span></span>

## <span data-ttu-id="9bfa2-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bfa2-108">PARAMETERS</span></span>

### <span data-ttu-id="9bfa2-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bfa2-109">-ApplicationGateway</span></span>
<span data-ttu-id="9bfa2-110">Bu cmdlet 'in kimlik doğrulama sertifikasını güncelleştirdiği uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="9bfa2-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9bfa2-111">-CertificateFile</span></span>
<span data-ttu-id="9bfa2-112">Bu cmdlet 'in sertifikayı güncelleştirdiği kimlik doğrulama sertifikası dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="9bfa2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bfa2-113">-Name</span></span>
<span data-ttu-id="9bfa2-114">Bu cmdlet 'in güncelleştirdiği kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-114">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9bfa2-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="9bfa2-115">-Confirm</span></span>
<span data-ttu-id="9bfa2-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bfa2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bfa2-117">-WhatIf</span></span>
<span data-ttu-id="9bfa2-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bfa2-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bfa2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfa2-120">-DefaultProfile</span></span>
<span data-ttu-id="9bfa2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfa2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfa2-122">CommonParameters</span></span>
<span data-ttu-id="9bfa2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bfa2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfa2-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfa2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfa2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bfa2-125">INPUTS</span></span>

### <span data-ttu-id="9bfa2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9bfa2-126">System.String</span></span>

## <span data-ttu-id="9bfa2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bfa2-127">OUTPUTS</span></span>

### <span data-ttu-id="9bfa2-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bfa2-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9bfa2-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bfa2-129">NOTES</span></span>
* <span data-ttu-id="9bfa2-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="9bfa2-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9bfa2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bfa2-131">RELATED LINKS</span></span>

[<span data-ttu-id="9bfa2-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9bfa2-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9bfa2-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9bfa2-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9bfa2-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9bfa2-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9bfa2-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9bfa2-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


