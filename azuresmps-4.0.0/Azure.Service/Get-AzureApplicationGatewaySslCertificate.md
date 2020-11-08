---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105664"
---
# <span data-ttu-id="2147a-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2147a-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2147a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2147a-102">SYNOPSIS</span></span>
<span data-ttu-id="2147a-103">Uygulama ağ geçidi sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="2147a-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="2147a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2147a-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2147a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2147a-105">DESCRIPTION</span></span>
<span data-ttu-id="2147a-106">**Get-AzureApplicationGatewaySslCertificate** cmdlet 'ı bir Azure Application Gateway Için güvenli yuva KATMANı (SSL) sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="2147a-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="2147a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2147a-107">EXAMPLES</span></span>

### <span data-ttu-id="2147a-108">Örnek 1: SSL sertifikası alın</span><span class="sxs-lookup"><span data-stu-id="2147a-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="2147a-109">Bu komut, ApplicationGateway08 adındaki uygulama ağ geçidinde SslCertificate13 adlı bir SSL sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="2147a-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="2147a-110">Örnek 2: tüm SSL sertifikalarını edinin</span><span class="sxs-lookup"><span data-stu-id="2147a-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="2147a-111">Bu komut, ApplicationGateway08 adındaki uygulama ağ geçidinde tüm SSL sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="2147a-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="2147a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2147a-112">PARAMETERS</span></span>

### <span data-ttu-id="2147a-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2147a-113">-CertificateName</span></span>
<span data-ttu-id="2147a-114">SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2147a-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="2147a-115">Bu cmdlet, bu parametrenin belirttiği sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="2147a-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2147a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2147a-116">-Name</span></span>
<span data-ttu-id="2147a-117">Bu cmdlet 'in SSL sertifikası aldığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2147a-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2147a-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="2147a-118">-Profile</span></span>
<span data-ttu-id="2147a-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2147a-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2147a-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2147a-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2147a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2147a-121">CommonParameters</span></span>
<span data-ttu-id="2147a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2147a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2147a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2147a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2147a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2147a-124">INPUTS</span></span>

### <span data-ttu-id="2147a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2147a-125">System.String</span></span>

## <span data-ttu-id="2147a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2147a-126">OUTPUTS</span></span>

### <span data-ttu-id="2147a-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, liste<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="2147a-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="2147a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2147a-128">NOTES</span></span>

## <span data-ttu-id="2147a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2147a-129">RELATED LINKS</span></span>

[<span data-ttu-id="2147a-130">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2147a-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2147a-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2147a-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
