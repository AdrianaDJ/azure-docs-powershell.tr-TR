---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 013010e0b679c69a6fa5c6d8341879b95bd55692
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594057"
---
# <span data-ttu-id="dcc57-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dcc57-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="dcc57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc57-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc57-103">Uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dcc57-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcc57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcc57-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcc57-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcc57-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc57-106">**Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dcc57-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="dcc57-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcc57-107">EXAMPLES</span></span>

## <span data-ttu-id="dcc57-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcc57-108">PARAMETERS</span></span>

### <span data-ttu-id="dcc57-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcc57-109">-ApplicationGateway</span></span>
<span data-ttu-id="dcc57-110">Bu cmdlet 'in bir kimlik doğrulama sertifikasını kaldırdığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcc57-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="dcc57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc57-111">-DefaultProfile</span></span>
<span data-ttu-id="dcc57-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcc57-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcc57-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcc57-113">-Name</span></span>
<span data-ttu-id="dcc57-114">Bu cmdlet 'in kaldırıldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcc57-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dcc57-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="dcc57-115">-Confirm</span></span>
<span data-ttu-id="dcc57-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dcc57-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcc57-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc57-117">-WhatIf</span></span>
<span data-ttu-id="dcc57-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcc57-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc57-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dcc57-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcc57-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc57-120">CommonParameters</span></span>
<span data-ttu-id="dcc57-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcc57-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc57-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc57-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc57-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcc57-123">INPUTS</span></span>

### <span data-ttu-id="dcc57-124">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc57-124">System.String</span></span>

## <span data-ttu-id="dcc57-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcc57-125">OUTPUTS</span></span>

### <span data-ttu-id="dcc57-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcc57-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dcc57-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcc57-127">NOTES</span></span>
* <span data-ttu-id="dcc57-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="dcc57-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dcc57-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcc57-129">RELATED LINKS</span></span>

[<span data-ttu-id="dcc57-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dcc57-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dcc57-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dcc57-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dcc57-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dcc57-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dcc57-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dcc57-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


