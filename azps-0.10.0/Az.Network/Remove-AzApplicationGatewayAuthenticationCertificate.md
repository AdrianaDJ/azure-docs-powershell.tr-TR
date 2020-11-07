---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935339"
---
# <span data-ttu-id="7df17-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7df17-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7df17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7df17-102">SYNOPSIS</span></span>
<span data-ttu-id="7df17-103">Uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7df17-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="7df17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7df17-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7df17-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7df17-105">DESCRIPTION</span></span>
<span data-ttu-id="7df17-106">**Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet 'i, bir Azure uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7df17-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="7df17-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7df17-107">EXAMPLES</span></span>

### <span data-ttu-id="7df17-108">2</span><span class="sxs-lookup"><span data-stu-id="7df17-108">1:</span></span>
```

```

## <span data-ttu-id="7df17-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7df17-109">PARAMETERS</span></span>

### <span data-ttu-id="7df17-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7df17-110">-ApplicationGateway</span></span>
<span data-ttu-id="7df17-111">Bu cmdlet 'in bir kimlik doğrulama sertifikasını kaldırdığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7df17-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="7df17-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df17-112">-DefaultProfile</span></span>
<span data-ttu-id="7df17-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7df17-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7df17-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="7df17-114">-Name</span></span>
<span data-ttu-id="7df17-115">Bu cmdlet 'in kaldırıldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7df17-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7df17-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="7df17-116">-Confirm</span></span>
<span data-ttu-id="7df17-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7df17-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df17-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df17-118">-WhatIf</span></span>
<span data-ttu-id="7df17-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7df17-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df17-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7df17-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df17-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df17-121">CommonParameters</span></span>
<span data-ttu-id="7df17-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7df17-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df17-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df17-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df17-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7df17-124">INPUTS</span></span>

### <span data-ttu-id="7df17-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7df17-125">System.String</span></span>

## <span data-ttu-id="7df17-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7df17-126">OUTPUTS</span></span>

### <span data-ttu-id="7df17-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7df17-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7df17-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7df17-128">NOTES</span></span>
* <span data-ttu-id="7df17-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="7df17-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7df17-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7df17-130">RELATED LINKS</span></span>

[<span data-ttu-id="7df17-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7df17-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7df17-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7df17-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7df17-133">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7df17-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7df17-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7df17-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


