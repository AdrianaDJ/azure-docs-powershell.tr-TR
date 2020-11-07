---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e94ca1bbed8e37643b301e5a5cb2ca3acc78d264
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917935"
---
# <span data-ttu-id="e0c26-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e0c26-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e0c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c26-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c26-103">Uygulama ağ geçidi 'nin güvenilen kök sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e0c26-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="e0c26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0c26-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0c26-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0c26-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c26-106">**Set-AzApplicationGatewayTrustedRootCertificate** cmdlet 'i, bir uygulama ağ geçidinin varolan güvenilen kök sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e0c26-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="e0c26-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0c26-107">EXAMPLES</span></span>

### <span data-ttu-id="e0c26-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0c26-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e0c26-109">Yukarıdaki örnek senaryolar, kök sertifika alındığında varolan bir güvenilen kök sertifikanın nasıl güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0c26-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="e0c26-110">İlk komut bir uygulama ağ geçidi alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e0c26-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="e0c26-111">İkinci komut, varolan güvenilen kök sertifikayı yeni bir kök sertifikayla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e0c26-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="e0c26-112">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e0c26-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e0c26-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0c26-113">PARAMETERS</span></span>

### <span data-ttu-id="e0c26-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0c26-114">-ApplicationGateway</span></span>
<span data-ttu-id="e0c26-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0c26-115">The applicationGateway</span></span>

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

### <span data-ttu-id="e0c26-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e0c26-116">-CertificateFile</span></span>
<span data-ttu-id="e0c26-117">Sertifika CER dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="e0c26-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="e0c26-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c26-118">-DefaultProfile</span></span>
<span data-ttu-id="e0c26-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0c26-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c26-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0c26-120">-Name</span></span>
<span data-ttu-id="e0c26-121">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="e0c26-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e0c26-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0c26-122">-Confirm</span></span>
<span data-ttu-id="e0c26-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0c26-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c26-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c26-124">-WhatIf</span></span>
<span data-ttu-id="e0c26-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0c26-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0c26-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0c26-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0c26-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c26-127">CommonParameters</span></span>
<span data-ttu-id="e0c26-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0c26-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c26-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0c26-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c26-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0c26-130">INPUTS</span></span>

### <span data-ttu-id="e0c26-131">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0c26-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0c26-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0c26-132">OUTPUTS</span></span>

### <span data-ttu-id="e0c26-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0c26-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0c26-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0c26-134">NOTES</span></span>

## <span data-ttu-id="e0c26-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0c26-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0c26-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e0c26-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e0c26-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e0c26-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e0c26-138">Yeni-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e0c26-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e0c26-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e0c26-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
