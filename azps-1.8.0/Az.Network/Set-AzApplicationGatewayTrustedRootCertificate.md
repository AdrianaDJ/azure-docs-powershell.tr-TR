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
ms.locfileid: "93760032"
---
# <span data-ttu-id="03f5c-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="03f5c-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="03f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="03f5c-103">Uygulama ağ geçidi 'nin güvenilen kök sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="03f5c-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="03f5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03f5c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03f5c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="03f5c-106">**Set-AzApplicationGatewayTrustedRootCertificate** cmdlet 'i, bir uygulama ağ geçidinin varolan güvenilen kök sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="03f5c-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="03f5c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03f5c-107">EXAMPLES</span></span>

### <span data-ttu-id="03f5c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="03f5c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="03f5c-109">Yukarıdaki örnek senaryolar, kök sertifika alındığında varolan bir güvenilen kök sertifikanın nasıl güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="03f5c-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="03f5c-110">İlk komut bir uygulama ağ geçidi alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="03f5c-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="03f5c-111">İkinci komut, varolan güvenilen kök sertifikayı yeni bir kök sertifikayla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="03f5c-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="03f5c-112">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="03f5c-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="03f5c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03f5c-113">PARAMETERS</span></span>

### <span data-ttu-id="03f5c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03f5c-114">-ApplicationGateway</span></span>
<span data-ttu-id="03f5c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03f5c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="03f5c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="03f5c-116">-CertificateFile</span></span>
<span data-ttu-id="03f5c-117">Sertifika CER dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="03f5c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="03f5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f5c-118">-DefaultProfile</span></span>
<span data-ttu-id="03f5c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03f5c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03f5c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="03f5c-120">-Name</span></span>
<span data-ttu-id="03f5c-121">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="03f5c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="03f5c-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="03f5c-122">-Confirm</span></span>
<span data-ttu-id="03f5c-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03f5c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03f5c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03f5c-124">-WhatIf</span></span>
<span data-ttu-id="03f5c-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03f5c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03f5c-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03f5c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03f5c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f5c-127">CommonParameters</span></span>
<span data-ttu-id="03f5c-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03f5c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f5c-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03f5c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f5c-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03f5c-130">INPUTS</span></span>

### <span data-ttu-id="03f5c-131">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03f5c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="03f5c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03f5c-132">OUTPUTS</span></span>

### <span data-ttu-id="03f5c-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03f5c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="03f5c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03f5c-134">NOTES</span></span>

## <span data-ttu-id="03f5c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03f5c-135">RELATED LINKS</span></span>

[<span data-ttu-id="03f5c-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="03f5c-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="03f5c-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="03f5c-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="03f5c-138">Yeni-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="03f5c-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="03f5c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="03f5c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
