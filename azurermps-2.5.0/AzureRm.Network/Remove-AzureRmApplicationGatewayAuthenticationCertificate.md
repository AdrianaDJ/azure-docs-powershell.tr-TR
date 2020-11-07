---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939106"
---
# <span data-ttu-id="7570e-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7570e-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7570e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7570e-102">SYNOPSIS</span></span>
<span data-ttu-id="7570e-103">Uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7570e-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7570e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7570e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7570e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7570e-105">DESCRIPTION</span></span>
<span data-ttu-id="7570e-106">**Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidinden kimlik doğrulama sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7570e-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="7570e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7570e-107">EXAMPLES</span></span>

### <span data-ttu-id="7570e-108">2</span><span class="sxs-lookup"><span data-stu-id="7570e-108">1:</span></span>
```

```

## <span data-ttu-id="7570e-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7570e-109">PARAMETERS</span></span>

### <span data-ttu-id="7570e-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7570e-110">-ApplicationGateway</span></span>
<span data-ttu-id="7570e-111">Bu cmdlet 'in bir kimlik doğrulama sertifikasını kaldırdığı uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7570e-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="7570e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7570e-112">-DefaultProfile</span></span>
<span data-ttu-id="7570e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7570e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7570e-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="7570e-114">-Name</span></span>
<span data-ttu-id="7570e-115">Bu cmdlet 'in kaldırıldığı kimlik doğrulama sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7570e-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7570e-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="7570e-116">-Confirm</span></span>
<span data-ttu-id="7570e-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7570e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7570e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7570e-118">-WhatIf</span></span>
<span data-ttu-id="7570e-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7570e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7570e-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7570e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7570e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7570e-121">CommonParameters</span></span>
<span data-ttu-id="7570e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7570e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7570e-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7570e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7570e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7570e-124">INPUTS</span></span>

### <span data-ttu-id="7570e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7570e-125">System.String</span></span>

## <span data-ttu-id="7570e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7570e-126">OUTPUTS</span></span>

### <span data-ttu-id="7570e-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7570e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7570e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7570e-128">NOTES</span></span>
* <span data-ttu-id="7570e-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="7570e-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7570e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7570e-130">RELATED LINKS</span></span>

[<span data-ttu-id="7570e-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7570e-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7570e-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7570e-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7570e-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7570e-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7570e-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7570e-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


