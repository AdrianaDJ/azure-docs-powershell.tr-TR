---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 6e2dceadf11323eb1798435df426c063f4d58858
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940091"
---
# <span data-ttu-id="c737d-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c737d-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c737d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c737d-102">SYNOPSIS</span></span>
<span data-ttu-id="c737d-103">Uygulama ağ geçidi için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="c737d-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c737d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c737d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c737d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c737d-105">DESCRIPTION</span></span>
<span data-ttu-id="c737d-106">**Get-AzureRmApplicationGatewaySslCertificate** cmdlet 'i bir uygulama ağ GEÇIDI için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="c737d-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="c737d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c737d-107">EXAMPLES</span></span>

### <span data-ttu-id="c737d-108">Örnek 1: belirli bir SSL sertifikası edinme</span><span class="sxs-lookup"><span data-stu-id="c737d-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="c737d-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c737d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c737d-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Cert01 adlı SSL sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="c737d-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="c737d-111">Komut, sertifikayı $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c737d-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="c737d-112">Örnek 2: SSL sertifikalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="c737d-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="c737d-113">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c737d-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c737d-114">Bu ikinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden SSL sertifikalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c737d-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="c737d-115">Bu komut, sonuçları $Certs adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c737d-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="c737d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c737d-116">PARAMETERS</span></span>

### <span data-ttu-id="c737d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c737d-117">-ApplicationGateway</span></span>
<span data-ttu-id="c737d-118">SSL sertifikasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c737d-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="c737d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c737d-119">-DefaultProfile</span></span>
<span data-ttu-id="c737d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c737d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c737d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c737d-121">-Name</span></span>
<span data-ttu-id="c737d-122">Bu cmdlet 'in aldığı SSL sertifikası havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c737d-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c737d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c737d-123">CommonParameters</span></span>
<span data-ttu-id="c737d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c737d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c737d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c737d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c737d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c737d-126">INPUTS</span></span>

### <span data-ttu-id="c737d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c737d-127">System.String</span></span>

## <span data-ttu-id="c737d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c737d-128">OUTPUTS</span></span>

### <span data-ttu-id="c737d-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c737d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c737d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c737d-130">NOTES</span></span>

## <span data-ttu-id="c737d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c737d-131">RELATED LINKS</span></span>

[<span data-ttu-id="c737d-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c737d-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c737d-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c737d-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c737d-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c737d-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c737d-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c737d-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


