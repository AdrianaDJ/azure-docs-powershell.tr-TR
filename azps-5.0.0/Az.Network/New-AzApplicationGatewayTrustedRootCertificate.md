---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324676"
---
# <span data-ttu-id="7334e-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7334e-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7334e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7334e-102">SYNOPSIS</span></span>
<span data-ttu-id="7334e-103">Uygulama ağ geçidi için güvenilen kök sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7334e-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="7334e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7334e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7334e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7334e-105">DESCRIPTION</span></span>
<span data-ttu-id="7334e-106">**Yeni-AzApplicationGatewayTrustedRootCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi Için güvenilen kök sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7334e-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7334e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7334e-107">EXAMPLES</span></span>

### <span data-ttu-id="7334e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7334e-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="7334e-109">Bu komut, "TRC1" listesi adlı bir güvenilen kök sertifika oluşturur ve sonucu $trc adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7334e-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="7334e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7334e-110">PARAMETERS</span></span>

### <span data-ttu-id="7334e-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7334e-111">-CertificateFile</span></span>
<span data-ttu-id="7334e-112">Sertifika CER dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="7334e-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="7334e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7334e-113">-DefaultProfile</span></span>
<span data-ttu-id="7334e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7334e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7334e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7334e-115">-Name</span></span>
<span data-ttu-id="7334e-116">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="7334e-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="7334e-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="7334e-117">-Confirm</span></span>
<span data-ttu-id="7334e-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7334e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7334e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7334e-119">-WhatIf</span></span>
<span data-ttu-id="7334e-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7334e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7334e-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7334e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7334e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7334e-122">CommonParameters</span></span>
<span data-ttu-id="7334e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7334e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7334e-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7334e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7334e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7334e-125">INPUTS</span></span>

### <span data-ttu-id="7334e-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7334e-126">None</span></span>

## <span data-ttu-id="7334e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7334e-127">OUTPUTS</span></span>

### <span data-ttu-id="7334e-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7334e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7334e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7334e-129">NOTES</span></span>

## <span data-ttu-id="7334e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7334e-130">RELATED LINKS</span></span>

[<span data-ttu-id="7334e-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7334e-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7334e-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7334e-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7334e-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7334e-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7334e-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7334e-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
