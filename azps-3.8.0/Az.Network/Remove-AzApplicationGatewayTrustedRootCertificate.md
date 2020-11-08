---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095816"
---
# <span data-ttu-id="d86ec-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d86ec-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d86ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d86ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d86ec-103">Uygulama ağ geçidinden güvenilir kök sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d86ec-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="d86ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d86ec-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d86ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d86ec-105">DESCRIPTION</span></span>
<span data-ttu-id="d86ec-106">**Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet 'i, varolan bir uygulama ağ geçidinden güvenilen kök sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d86ec-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="d86ec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d86ec-107">EXAMPLES</span></span>

### <span data-ttu-id="d86ec-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d86ec-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d86ec-109">İlk komut bir uygulama ağ geçidi alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d86ec-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="d86ec-110">İkinci komut, $gw depolanan uygulama ağ geçidinden myRootCA adlı güvenilen kök sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d86ec-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="d86ec-111">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d86ec-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="d86ec-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d86ec-112">PARAMETERS</span></span>

### <span data-ttu-id="d86ec-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d86ec-113">-ApplicationGateway</span></span>
<span data-ttu-id="d86ec-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d86ec-114">The applicationGateway</span></span>

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

### <span data-ttu-id="d86ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86ec-115">-DefaultProfile</span></span>
<span data-ttu-id="d86ec-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d86ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d86ec-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d86ec-117">-Name</span></span>
<span data-ttu-id="d86ec-118">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="d86ec-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d86ec-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d86ec-119">-Confirm</span></span>
<span data-ttu-id="d86ec-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d86ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d86ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d86ec-121">-WhatIf</span></span>
<span data-ttu-id="d86ec-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d86ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d86ec-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d86ec-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d86ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86ec-124">CommonParameters</span></span>
<span data-ttu-id="d86ec-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d86ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86ec-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d86ec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86ec-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d86ec-127">INPUTS</span></span>

### <span data-ttu-id="d86ec-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d86ec-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d86ec-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d86ec-129">OUTPUTS</span></span>

### <span data-ttu-id="d86ec-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d86ec-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d86ec-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d86ec-131">NOTES</span></span>

## <span data-ttu-id="d86ec-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d86ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="d86ec-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d86ec-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d86ec-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d86ec-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d86ec-135">Yeni-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d86ec-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d86ec-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d86ec-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)