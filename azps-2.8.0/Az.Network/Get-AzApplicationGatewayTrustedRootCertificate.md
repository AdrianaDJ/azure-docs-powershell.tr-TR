---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 1e617ef1283937116bd97c24a968f247fa7552de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932046"
---
# <span data-ttu-id="5ae76-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5ae76-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="5ae76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ae76-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae76-103">Uygulama ağ geçidinden belirli bir adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="5ae76-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="5ae76-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ae76-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ae76-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ae76-105">DESCRIPTION</span></span>
<span data-ttu-id="5ae76-106">**Get-AzApplicationGatewayTrustedRootCertificate** cmdlet 'ı uygulama ağ geçidinden belirli bir adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="5ae76-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="5ae76-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ae76-107">EXAMPLES</span></span>

### <span data-ttu-id="5ae76-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ae76-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="5ae76-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5ae76-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="5ae76-110">İkinci komut, uygulama ağ geçidinden belirtilen adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="5ae76-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="5ae76-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ae76-111">PARAMETERS</span></span>

### <span data-ttu-id="5ae76-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ae76-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ae76-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ae76-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5ae76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae76-114">-DefaultProfile</span></span>
<span data-ttu-id="5ae76-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ae76-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ae76-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ae76-116">-Name</span></span>
<span data-ttu-id="5ae76-117">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="5ae76-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="5ae76-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae76-118">CommonParameters</span></span>
<span data-ttu-id="5ae76-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ae76-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae76-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ae76-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae76-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ae76-121">INPUTS</span></span>

### <span data-ttu-id="5ae76-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ae76-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ae76-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ae76-123">OUTPUTS</span></span>

### <span data-ttu-id="5ae76-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5ae76-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="5ae76-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ae76-125">NOTES</span></span>

## <span data-ttu-id="5ae76-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ae76-126">RELATED LINKS</span></span>

[<span data-ttu-id="5ae76-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5ae76-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="5ae76-128">Yeni-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5ae76-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="5ae76-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5ae76-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="5ae76-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5ae76-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)