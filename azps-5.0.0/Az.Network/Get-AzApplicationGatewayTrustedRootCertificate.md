---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279976"
---
# <span data-ttu-id="265f4-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="265f4-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="265f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="265f4-102">SYNOPSIS</span></span>
<span data-ttu-id="265f4-103">Uygulama ağ geçidinden belirli bir adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="265f4-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="265f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="265f4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="265f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="265f4-105">DESCRIPTION</span></span>
<span data-ttu-id="265f4-106">**Get-AzApplicationGatewayTrustedRootCertificate** cmdlet 'ı uygulama ağ geçidinden belirli bir adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="265f4-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="265f4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="265f4-107">EXAMPLES</span></span>

### <span data-ttu-id="265f4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="265f4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="265f4-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="265f4-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="265f4-110">İkinci komut, uygulama ağ geçidinden belirtilen adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="265f4-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="265f4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="265f4-111">PARAMETERS</span></span>

### <span data-ttu-id="265f4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="265f4-112">-ApplicationGateway</span></span>
<span data-ttu-id="265f4-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="265f4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="265f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265f4-114">-DefaultProfile</span></span>
<span data-ttu-id="265f4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="265f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="265f4-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="265f4-116">-Name</span></span>
<span data-ttu-id="265f4-117">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="265f4-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="265f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265f4-118">CommonParameters</span></span>
<span data-ttu-id="265f4-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="265f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265f4-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="265f4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265f4-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="265f4-121">INPUTS</span></span>

### <span data-ttu-id="265f4-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="265f4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="265f4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="265f4-123">OUTPUTS</span></span>

### <span data-ttu-id="265f4-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="265f4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="265f4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="265f4-125">NOTES</span></span>

## <span data-ttu-id="265f4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="265f4-126">RELATED LINKS</span></span>

[<span data-ttu-id="265f4-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="265f4-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="265f4-128">Yeni-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="265f4-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="265f4-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="265f4-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="265f4-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="265f4-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
