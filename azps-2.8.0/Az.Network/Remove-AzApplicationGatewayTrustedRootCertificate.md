---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 9ef0629a56787229a995744235980eeb744ede08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918104"
---
# <span data-ttu-id="ee988-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ee988-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="ee988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee988-102">SYNOPSIS</span></span>
<span data-ttu-id="ee988-103">Uygulama ağ geçidinden güvenilir kök sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee988-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="ee988-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee988-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee988-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee988-105">DESCRIPTION</span></span>
<span data-ttu-id="ee988-106">**Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet 'i, varolan bir uygulama ağ geçidinden güvenilen kök sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee988-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="ee988-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee988-107">EXAMPLES</span></span>

### <span data-ttu-id="ee988-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee988-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="ee988-109">İlk komut bir uygulama ağ geçidi alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ee988-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="ee988-110">İkinci komut, $gw depolanan uygulama ağ geçidinden myRootCA adlı güvenilen kök sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee988-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="ee988-111">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ee988-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="ee988-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee988-112">PARAMETERS</span></span>

### <span data-ttu-id="ee988-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee988-113">-ApplicationGateway</span></span>
<span data-ttu-id="ee988-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee988-114">The applicationGateway</span></span>

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

### <span data-ttu-id="ee988-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee988-115">-DefaultProfile</span></span>
<span data-ttu-id="ee988-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee988-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee988-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee988-117">-Name</span></span>
<span data-ttu-id="ee988-118">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="ee988-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="ee988-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee988-119">-Confirm</span></span>
<span data-ttu-id="ee988-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee988-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee988-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee988-121">-WhatIf</span></span>
<span data-ttu-id="ee988-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee988-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee988-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee988-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee988-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee988-124">CommonParameters</span></span>
<span data-ttu-id="ee988-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee988-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee988-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee988-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee988-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee988-127">INPUTS</span></span>

### <span data-ttu-id="ee988-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee988-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ee988-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee988-129">OUTPUTS</span></span>

### <span data-ttu-id="ee988-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee988-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ee988-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee988-131">NOTES</span></span>

## <span data-ttu-id="ee988-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee988-132">RELATED LINKS</span></span>

[<span data-ttu-id="ee988-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ee988-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="ee988-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ee988-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="ee988-135">Yeni-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ee988-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="ee988-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ee988-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
