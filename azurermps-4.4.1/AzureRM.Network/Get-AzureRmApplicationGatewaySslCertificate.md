---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: da831810461e763acc51319ea4d6662c45a1c3ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589978"
---
# <span data-ttu-id="80dc9-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80dc9-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="80dc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="80dc9-103">Uygulama ağ geçidi için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="80dc9-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80dc9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80dc9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80dc9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80dc9-105">DESCRIPTION</span></span>
<span data-ttu-id="80dc9-106">**Get-AzureRmApplicationGatewaySslCertificate** cmdlet 'i bir uygulama ağ GEÇIDI için SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="80dc9-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="80dc9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80dc9-107">EXAMPLES</span></span>

### <span data-ttu-id="80dc9-108">Örnek 1: belirli bir SSL sertifikası edinme</span><span class="sxs-lookup"><span data-stu-id="80dc9-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="80dc9-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="80dc9-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="80dc9-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Cert01 adlı SSL sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="80dc9-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="80dc9-111">Komut, sertifikayı $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="80dc9-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="80dc9-112">Örnek 2: SSL sertifikalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="80dc9-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="80dc9-113">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="80dc9-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="80dc9-114">Bu ikinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden SSL sertifikalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="80dc9-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="80dc9-115">Bu komut, sonuçları $Certs adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="80dc9-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="80dc9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80dc9-116">PARAMETERS</span></span>

### <span data-ttu-id="80dc9-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80dc9-117">-ApplicationGateway</span></span>
<span data-ttu-id="80dc9-118">SSL sertifikasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="80dc9-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="80dc9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="80dc9-119">-Name</span></span>
<span data-ttu-id="80dc9-120">Bu cmdlet 'in aldığı SSL sertifikası havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80dc9-120">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="80dc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80dc9-121">-DefaultProfile</span></span>
<span data-ttu-id="80dc9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80dc9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80dc9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dc9-123">CommonParameters</span></span>
<span data-ttu-id="80dc9-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80dc9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80dc9-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80dc9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dc9-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80dc9-126">INPUTS</span></span>

### <span data-ttu-id="80dc9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="80dc9-127">System.String</span></span>

## <span data-ttu-id="80dc9-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80dc9-128">OUTPUTS</span></span>

### <span data-ttu-id="80dc9-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80dc9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="80dc9-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80dc9-130">NOTES</span></span>

## <span data-ttu-id="80dc9-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80dc9-131">RELATED LINKS</span></span>

[<span data-ttu-id="80dc9-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80dc9-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="80dc9-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80dc9-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="80dc9-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80dc9-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="80dc9-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80dc9-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


