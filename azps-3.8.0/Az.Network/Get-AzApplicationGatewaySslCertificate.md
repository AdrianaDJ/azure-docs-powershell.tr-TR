---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937822"
---
# <span data-ttu-id="b1da3-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b1da3-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b1da3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1da3-102">SYNOPSIS</span></span>
<span data-ttu-id="b1da3-103">Uygulama ağ geçidi için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="b1da3-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="b1da3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1da3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1da3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1da3-105">DESCRIPTION</span></span>
<span data-ttu-id="b1da3-106">**Get-AzApplicationGatewaySslCertificate** cmdlet 'i, bir uygulama ağ GEÇIDI için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="b1da3-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="b1da3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1da3-107">EXAMPLES</span></span>

### <span data-ttu-id="b1da3-108">Örnek 1: belirli bir SSL sertifikası edinme</span><span class="sxs-lookup"><span data-stu-id="b1da3-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b1da3-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b1da3-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b1da3-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Cert01 adlı SSL sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="b1da3-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b1da3-111">Komut, sertifikayı $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b1da3-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="b1da3-112">Örnek 2: SSL sertifikalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="b1da3-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="b1da3-113">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b1da3-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b1da3-114">Bu ikinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden SSL sertifikalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b1da3-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="b1da3-115">Bu komut, sonuçları $Certs adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b1da3-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="b1da3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1da3-116">PARAMETERS</span></span>

### <span data-ttu-id="b1da3-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1da3-117">-ApplicationGateway</span></span>
<span data-ttu-id="b1da3-118">SSL sertifikasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1da3-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="b1da3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1da3-119">-DefaultProfile</span></span>
<span data-ttu-id="b1da3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1da3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1da3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1da3-121">-Name</span></span>
<span data-ttu-id="b1da3-122">Bu cmdlet 'in aldığı SSL sertifikası havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1da3-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b1da3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1da3-123">CommonParameters</span></span>
<span data-ttu-id="b1da3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1da3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1da3-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b1da3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1da3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1da3-126">INPUTS</span></span>

### <span data-ttu-id="b1da3-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1da3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1da3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1da3-128">OUTPUTS</span></span>

### <span data-ttu-id="b1da3-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b1da3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b1da3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1da3-130">NOTES</span></span>

## <span data-ttu-id="b1da3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1da3-131">RELATED LINKS</span></span>

[<span data-ttu-id="b1da3-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b1da3-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b1da3-133">Yeni-Azapplicationgatewaysslsertifikası</span><span class="sxs-lookup"><span data-stu-id="b1da3-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b1da3-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b1da3-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b1da3-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b1da3-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


