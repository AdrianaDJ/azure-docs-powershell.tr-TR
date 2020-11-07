---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935446"
---
# <span data-ttu-id="15288-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="15288-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15288-102">SYNOPSIS</span></span>
<span data-ttu-id="15288-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15288-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="15288-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15288-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15288-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15288-105">DESCRIPTION</span></span>
<span data-ttu-id="15288-106">**Yeni-AzApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15288-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="15288-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15288-107">EXAMPLES</span></span>

### <span data-ttu-id="15288-108">2</span><span class="sxs-lookup"><span data-stu-id="15288-108">1:</span></span>
```

```

## <span data-ttu-id="15288-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15288-109">PARAMETERS</span></span>

### <span data-ttu-id="15288-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="15288-110">-CertificateFile</span></span>
<span data-ttu-id="15288-111">Kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15288-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="15288-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15288-112">-DefaultProfile</span></span>
<span data-ttu-id="15288-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15288-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15288-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="15288-114">-Name</span></span>
<span data-ttu-id="15288-115">Kimlik doğrulama sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="15288-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="15288-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="15288-116">-Confirm</span></span>
<span data-ttu-id="15288-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15288-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15288-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15288-118">-WhatIf</span></span>
<span data-ttu-id="15288-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15288-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15288-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15288-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15288-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15288-121">CommonParameters</span></span>
<span data-ttu-id="15288-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15288-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15288-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15288-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15288-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15288-124">INPUTS</span></span>

### <span data-ttu-id="15288-125">System. String</span><span class="sxs-lookup"><span data-stu-id="15288-125">System.String</span></span>

## <span data-ttu-id="15288-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15288-126">OUTPUTS</span></span>

### <span data-ttu-id="15288-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="15288-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15288-128">NOTES</span></span>
* <span data-ttu-id="15288-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="15288-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="15288-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15288-130">RELATED LINKS</span></span>

[<span data-ttu-id="15288-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="15288-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="15288-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="15288-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


