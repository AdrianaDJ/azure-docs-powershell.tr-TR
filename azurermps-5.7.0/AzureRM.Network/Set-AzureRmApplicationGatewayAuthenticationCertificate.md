---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ebeff6e8c8542d487305ec7570a30c26689e6885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595090"
---
# <span data-ttu-id="a043f-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a043f-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="a043f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a043f-102">SYNOPSIS</span></span>
<span data-ttu-id="a043f-103">Uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a043f-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a043f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a043f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a043f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a043f-105">DESCRIPTION</span></span>
<span data-ttu-id="a043f-106">**Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a043f-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="a043f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a043f-107">EXAMPLES</span></span>

## <span data-ttu-id="a043f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a043f-108">PARAMETERS</span></span>

### <span data-ttu-id="a043f-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a043f-109">-ApplicationGateway</span></span>
<span data-ttu-id="a043f-110">Bu cmdlet 'in kimlik doğrulama sertifikasını güncelleştirdiği uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a043f-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="a043f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a043f-111">-CertificateFile</span></span>
<span data-ttu-id="a043f-112">Bu cmdlet 'in sertifikayı güncelleştirdiği kimlik doğrulama sertifikası dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a043f-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="a043f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a043f-113">-DefaultProfile</span></span>
<span data-ttu-id="a043f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a043f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a043f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a043f-115">-Name</span></span>
<span data-ttu-id="a043f-116">Bu cmdlet 'in güncelleştirdiği kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a043f-116">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a043f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="a043f-117">-Confirm</span></span>
<span data-ttu-id="a043f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a043f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a043f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a043f-119">-WhatIf</span></span>
<span data-ttu-id="a043f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a043f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a043f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a043f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a043f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a043f-122">CommonParameters</span></span>
<span data-ttu-id="a043f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a043f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a043f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a043f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a043f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a043f-125">INPUTS</span></span>

### <span data-ttu-id="a043f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a043f-126">System.String</span></span>

## <span data-ttu-id="a043f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a043f-127">OUTPUTS</span></span>

### <span data-ttu-id="a043f-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a043f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a043f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a043f-129">NOTES</span></span>
* <span data-ttu-id="a043f-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="a043f-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a043f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a043f-131">RELATED LINKS</span></span>

[<span data-ttu-id="a043f-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a043f-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a043f-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a043f-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a043f-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a043f-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a043f-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a043f-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


