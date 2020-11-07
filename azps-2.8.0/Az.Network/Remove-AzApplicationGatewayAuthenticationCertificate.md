---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 4bed76f6fa80e5f901d5deeba45940d16332fa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932316"
---
# <span data-ttu-id="c7d39-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7d39-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c7d39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d39-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d39-103">Uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7d39-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="c7d39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7d39-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7d39-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7d39-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d39-106">**Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet 'i, bir Azure uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7d39-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="c7d39-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7d39-107">EXAMPLES</span></span>

### <span data-ttu-id="c7d39-108">Örnek 1: uygulama ağ geçidinden kimlik doğrulama sertifikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="c7d39-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="c7d39-109">İlk komut appGwName adlı uygulama ağ geçidini alır ve sonucu $appgw değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="c7d39-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="c7d39-110">İkinci komut cert01 adındaki kimlik doğrulama sertifikasını uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7d39-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="c7d39-111">Üçüncü komut, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c7d39-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="c7d39-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7d39-112">PARAMETERS</span></span>

### <span data-ttu-id="c7d39-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7d39-113">-ApplicationGateway</span></span>
<span data-ttu-id="c7d39-114">Bu cmdlet 'in bir kimlik doğrulama sertifikasını kaldırdığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7d39-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="c7d39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d39-115">-DefaultProfile</span></span>
<span data-ttu-id="c7d39-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7d39-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d39-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7d39-117">-Name</span></span>
<span data-ttu-id="c7d39-118">Bu cmdlet 'in kaldırıldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7d39-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c7d39-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7d39-119">-Confirm</span></span>
<span data-ttu-id="c7d39-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7d39-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7d39-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7d39-121">-WhatIf</span></span>
<span data-ttu-id="c7d39-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7d39-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7d39-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7d39-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7d39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d39-124">CommonParameters</span></span>
<span data-ttu-id="c7d39-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7d39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d39-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d39-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d39-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7d39-127">INPUTS</span></span>

### <span data-ttu-id="c7d39-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7d39-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7d39-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7d39-129">OUTPUTS</span></span>

### <span data-ttu-id="c7d39-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7d39-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7d39-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7d39-131">NOTES</span></span>
* <span data-ttu-id="c7d39-132">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="c7d39-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c7d39-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7d39-133">RELATED LINKS</span></span>

[<span data-ttu-id="c7d39-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7d39-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7d39-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7d39-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7d39-136">Yeni-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7d39-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7d39-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7d39-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)

