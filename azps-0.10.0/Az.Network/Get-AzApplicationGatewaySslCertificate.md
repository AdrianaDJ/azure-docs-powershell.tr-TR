---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 62c73fe60e147ca34083851db50c3830198dd60e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935581"
---
# <span data-ttu-id="92683-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92683-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="92683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92683-102">SYNOPSIS</span></span>
<span data-ttu-id="92683-103">Uygulama ağ geçidi için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="92683-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="92683-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92683-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92683-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92683-105">DESCRIPTION</span></span>
<span data-ttu-id="92683-106">**Get-AzApplicationGatewaySslCertificate** cmdlet 'i, bir uygulama ağ GEÇIDI için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="92683-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="92683-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92683-107">EXAMPLES</span></span>

### <span data-ttu-id="92683-108">Örnek 1: belirli bir SSL sertifikası edinme</span><span class="sxs-lookup"><span data-stu-id="92683-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="92683-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="92683-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="92683-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Cert01 adlı SSL sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="92683-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="92683-111">Komut, sertifikayı $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="92683-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="92683-112">Örnek 2: SSL sertifikalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="92683-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="92683-113">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="92683-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="92683-114">Bu ikinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden SSL sertifikalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="92683-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="92683-115">Bu komut, sonuçları $Certs adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="92683-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="92683-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92683-116">PARAMETERS</span></span>

### <span data-ttu-id="92683-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92683-117">-ApplicationGateway</span></span>
<span data-ttu-id="92683-118">SSL sertifikasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92683-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="92683-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92683-119">-DefaultProfile</span></span>
<span data-ttu-id="92683-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92683-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92683-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="92683-121">-Name</span></span>
<span data-ttu-id="92683-122">Bu cmdlet 'in aldığı SSL sertifikası havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92683-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92683-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92683-123">CommonParameters</span></span>
<span data-ttu-id="92683-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92683-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92683-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92683-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92683-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92683-126">INPUTS</span></span>

### <span data-ttu-id="92683-127">System. String</span><span class="sxs-lookup"><span data-stu-id="92683-127">System.String</span></span>

## <span data-ttu-id="92683-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92683-128">OUTPUTS</span></span>

### <span data-ttu-id="92683-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92683-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="92683-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92683-130">NOTES</span></span>

## <span data-ttu-id="92683-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92683-131">RELATED LINKS</span></span>

[<span data-ttu-id="92683-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92683-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="92683-133">Yeni-Azapplicationgatewaysslsertifikası</span><span class="sxs-lookup"><span data-stu-id="92683-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="92683-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92683-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="92683-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92683-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


