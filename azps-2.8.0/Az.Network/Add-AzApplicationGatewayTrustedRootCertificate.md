---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c8db96e9758e04a96f3f7b28c9fda9d8ac73a47e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932110"
---
# <span data-ttu-id="cea19-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cea19-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="cea19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea19-102">SYNOPSIS</span></span>
<span data-ttu-id="cea19-103">Uygulama ağ geçidine güvenilir kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cea19-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="cea19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cea19-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea19-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cea19-105">DESCRIPTION</span></span>
<span data-ttu-id="cea19-106">**Add-AzApplicationGatewayTrustedRootCertificate** cmdlet 'ı bir Azure uygulama ağ geçidine güvenilen kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cea19-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="cea19-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cea19-107">EXAMPLES</span></span>

### <span data-ttu-id="cea19-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cea19-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="cea19-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cea19-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="cea19-110">İkinci komut, kök sertifikanın giriş yolunu gösteren uygulama ağ geçidi 'ne yeni bir güvenilen kök sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="cea19-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="cea19-111">Üçüncü komut, arka uç sunucu sertifikasını doğrulamak için güvenilen kök sertifikası kullanarak yeni bir arka uç http ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cea19-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="cea19-112">Dördüncü komut, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cea19-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="cea19-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cea19-113">PARAMETERS</span></span>

### <span data-ttu-id="cea19-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cea19-114">-ApplicationGateway</span></span>
<span data-ttu-id="cea19-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cea19-115">The applicationGateway</span></span>

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

### <span data-ttu-id="cea19-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cea19-116">-CertificateFile</span></span>
<span data-ttu-id="cea19-117">Sertifika CER dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="cea19-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="cea19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea19-118">-DefaultProfile</span></span>
<span data-ttu-id="cea19-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cea19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cea19-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="cea19-120">-Name</span></span>
<span data-ttu-id="cea19-121">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="cea19-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="cea19-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="cea19-122">-Confirm</span></span>
<span data-ttu-id="cea19-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cea19-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea19-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea19-124">-WhatIf</span></span>
<span data-ttu-id="cea19-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cea19-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea19-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cea19-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea19-127">CommonParameters</span></span>
<span data-ttu-id="cea19-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cea19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea19-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea19-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea19-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cea19-130">INPUTS</span></span>

### <span data-ttu-id="cea19-131">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cea19-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cea19-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cea19-132">OUTPUTS</span></span>

### <span data-ttu-id="cea19-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cea19-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cea19-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cea19-134">NOTES</span></span>

## <span data-ttu-id="cea19-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cea19-135">RELATED LINKS</span></span>

[<span data-ttu-id="cea19-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cea19-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cea19-137">Yeni-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cea19-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cea19-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cea19-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cea19-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cea19-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)