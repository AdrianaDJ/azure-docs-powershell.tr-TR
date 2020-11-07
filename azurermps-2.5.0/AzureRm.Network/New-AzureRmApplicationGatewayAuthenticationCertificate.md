---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939307"
---
# <span data-ttu-id="7dea0-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7dea0-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7dea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dea0-102">SYNOPSIS</span></span>
<span data-ttu-id="7dea0-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7dea0-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dea0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7dea0-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dea0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7dea0-105">DESCRIPTION</span></span>
<span data-ttu-id="7dea0-106">**New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure Application Gateway için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7dea0-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7dea0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7dea0-107">EXAMPLES</span></span>

### <span data-ttu-id="7dea0-108">2</span><span class="sxs-lookup"><span data-stu-id="7dea0-108">1:</span></span>
```

```

## <span data-ttu-id="7dea0-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7dea0-109">PARAMETERS</span></span>

### <span data-ttu-id="7dea0-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7dea0-110">-CertificateFile</span></span>
<span data-ttu-id="7dea0-111">Kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dea0-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="7dea0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dea0-112">-DefaultProfile</span></span>
<span data-ttu-id="7dea0-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7dea0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dea0-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="7dea0-114">-Name</span></span>
<span data-ttu-id="7dea0-115">Kimlik doğrulama sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dea0-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="7dea0-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="7dea0-116">-Confirm</span></span>
<span data-ttu-id="7dea0-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7dea0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dea0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dea0-118">-WhatIf</span></span>
<span data-ttu-id="7dea0-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7dea0-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dea0-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7dea0-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dea0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dea0-121">CommonParameters</span></span>
<span data-ttu-id="7dea0-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7dea0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dea0-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dea0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dea0-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7dea0-124">INPUTS</span></span>

### <span data-ttu-id="7dea0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7dea0-125">System.String</span></span>

## <span data-ttu-id="7dea0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7dea0-126">OUTPUTS</span></span>

### <span data-ttu-id="7dea0-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7dea0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7dea0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7dea0-128">NOTES</span></span>
* <span data-ttu-id="7dea0-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="7dea0-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7dea0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7dea0-130">RELATED LINKS</span></span>

[<span data-ttu-id="7dea0-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7dea0-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7dea0-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7dea0-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7dea0-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7dea0-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7dea0-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7dea0-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


