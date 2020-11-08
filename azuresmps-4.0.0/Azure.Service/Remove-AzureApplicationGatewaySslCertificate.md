---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106494"
---
# <span data-ttu-id="6986a-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6986a-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6986a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6986a-102">SYNOPSIS</span></span>
<span data-ttu-id="6986a-103">Uygulama ağ geçidinden SSL sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6986a-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="6986a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6986a-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6986a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6986a-105">DESCRIPTION</span></span>
<span data-ttu-id="6986a-106">**Remove-AzureApplicationGatewaySslCertificate** cmdlet 'i, bir uygulama ağ geçidinden güvenli yuva KATMANı (SSL) sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6986a-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="6986a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6986a-107">EXAMPLES</span></span>

### <span data-ttu-id="6986a-108">Örnek 1: SSL sertifikasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6986a-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="6986a-109">Bu komut, SslCertificate13 adlı bir SSL sertifikasını ApplicationGateway08 adındaki uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6986a-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="6986a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6986a-110">PARAMETERS</span></span>

### <span data-ttu-id="6986a-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6986a-111">-CertificateName</span></span>
<span data-ttu-id="6986a-112">SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6986a-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="6986a-113">Bu cmdlet, bu parametrenin belirttiği sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6986a-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="6986a-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="6986a-114">-Name</span></span>
<span data-ttu-id="6986a-115">Bu cmdlet 'in SSL sertifikasını kaldırdığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6986a-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="6986a-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="6986a-116">-Profile</span></span>
<span data-ttu-id="6986a-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6986a-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6986a-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6986a-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6986a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6986a-119">CommonParameters</span></span>
<span data-ttu-id="6986a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6986a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6986a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6986a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6986a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6986a-122">INPUTS</span></span>

### <span data-ttu-id="6986a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6986a-123">System.String</span></span>

## <span data-ttu-id="6986a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6986a-124">OUTPUTS</span></span>

### <span data-ttu-id="6986a-125">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6986a-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="6986a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6986a-126">NOTES</span></span>

## <span data-ttu-id="6986a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6986a-127">RELATED LINKS</span></span>

[<span data-ttu-id="6986a-128">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6986a-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6986a-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6986a-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
