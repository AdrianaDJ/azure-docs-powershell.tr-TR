---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274881"
---
# <span data-ttu-id="bf1b4-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf1b4-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bf1b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1b4-103">Uygulama ağ geçidi için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="bf1b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf1b4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf1b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf1b4-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1b4-106">**Yeni-AzApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="bf1b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf1b4-107">EXAMPLES</span></span>

### <span data-ttu-id="bf1b4-108">Örnek 1: kimlik doğrulama sertifikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="bf1b4-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="bf1b4-109">İlk komut cert01 adlı kimlik doğrulama sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="bf1b4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf1b4-110">PARAMETERS</span></span>

### <span data-ttu-id="bf1b4-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bf1b4-111">-CertificateFile</span></span>
<span data-ttu-id="bf1b4-112">Kimlik doğrulama sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="bf1b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1b4-113">-DefaultProfile</span></span>
<span data-ttu-id="bf1b4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf1b4-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf1b4-115">-Name</span></span>
<span data-ttu-id="bf1b4-116">Kimlik doğrulama sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="bf1b4-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf1b4-117">-Confirm</span></span>
<span data-ttu-id="bf1b4-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf1b4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf1b4-119">-WhatIf</span></span>
<span data-ttu-id="bf1b4-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf1b4-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf1b4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1b4-122">CommonParameters</span></span>
<span data-ttu-id="bf1b4-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf1b4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1b4-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf1b4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1b4-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf1b4-125">INPUTS</span></span>

### <span data-ttu-id="bf1b4-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bf1b4-126">None</span></span>

## <span data-ttu-id="bf1b4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf1b4-127">OUTPUTS</span></span>

### <span data-ttu-id="bf1b4-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf1b4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bf1b4-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf1b4-129">NOTES</span></span>
* <span data-ttu-id="bf1b4-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="bf1b4-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bf1b4-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf1b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="bf1b4-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf1b4-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bf1b4-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf1b4-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bf1b4-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf1b4-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bf1b4-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf1b4-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


