---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 51bb8ff46613080d3fa62a2b4953419348cb99bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592179"
---
# <span data-ttu-id="b4047-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4047-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b4047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4047-102">SYNOPSIS</span></span>
<span data-ttu-id="b4047-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4047-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4047-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4047-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4047-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4047-105">DESCRIPTION</span></span>
<span data-ttu-id="b4047-106">**New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure Application Gateway için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4047-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b4047-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4047-107">EXAMPLES</span></span>

## <span data-ttu-id="b4047-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4047-108">PARAMETERS</span></span>

### <span data-ttu-id="b4047-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b4047-109">-CertificateFile</span></span>
<span data-ttu-id="b4047-110">Kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4047-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="b4047-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4047-111">-Name</span></span>
<span data-ttu-id="b4047-112">Kimlik doğrulama sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4047-112">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="b4047-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4047-113">-Confirm</span></span>
<span data-ttu-id="b4047-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4047-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4047-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4047-115">-WhatIf</span></span>
<span data-ttu-id="b4047-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4047-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4047-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4047-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4047-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4047-118">-DefaultProfile</span></span>
<span data-ttu-id="b4047-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4047-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4047-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4047-120">CommonParameters</span></span>
<span data-ttu-id="b4047-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4047-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4047-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4047-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4047-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4047-123">INPUTS</span></span>

### <span data-ttu-id="b4047-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b4047-124">System.String</span></span>

## <span data-ttu-id="b4047-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4047-125">OUTPUTS</span></span>

### <span data-ttu-id="b4047-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4047-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b4047-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4047-127">NOTES</span></span>
* <span data-ttu-id="b4047-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="b4047-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b4047-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4047-129">RELATED LINKS</span></span>

[<span data-ttu-id="b4047-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4047-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b4047-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4047-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b4047-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4047-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b4047-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4047-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


