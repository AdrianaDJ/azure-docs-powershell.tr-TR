---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105736"
---
# <span data-ttu-id="f0a1b-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f0a1b-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f0a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a1b-103">Uygulama ağ geçidine SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="f0a1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0a1b-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f0a1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a1b-106">**Add-AzureApplicationGatewaySslCertificate** cmdlet 'ı bir Azure uygulama ağ geçidine güvenli yuva KATMANı (SSL) sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="f0a1b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="f0a1b-108">Örnek 1: SSL sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="f0a1b-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="f0a1b-109">Bu komut, ApplicationGateway08 adındaki uygulama ağ geçidine SslCertificate13 adlı bir SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="f0a1b-110">Komut, sertifika dosyasının yolunu ve sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="f0a1b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0a1b-111">PARAMETERS</span></span>

### <span data-ttu-id="f0a1b-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f0a1b-112">-CertificateFile</span></span>
<span data-ttu-id="f0a1b-113">SSL sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="f0a1b-114">Bu cmdlet, sertifikayı bu parametrenin belirttiği dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0a1b-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="f0a1b-115">-CertificateName</span></span>
<span data-ttu-id="f0a1b-116">SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="f0a1b-117">Bu cmdlet, bu parametrenin belirttiği sertifikayı ekler.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0a1b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0a1b-118">-Name</span></span>
<span data-ttu-id="f0a1b-119">Bu cmdlet 'in SSL sertifikası eklediği uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="f0a1b-120">-Parola</span><span class="sxs-lookup"><span data-stu-id="f0a1b-120">-Password</span></span>
<span data-ttu-id="f0a1b-121">Bu cmdlet 'in eklediği SSL sertifikasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f0a1b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="f0a1b-122">-Profile</span></span>
<span data-ttu-id="f0a1b-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0a1b-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0a1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a1b-125">CommonParameters</span></span>
<span data-ttu-id="f0a1b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a1b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a1b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a1b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0a1b-128">INPUTS</span></span>

### <span data-ttu-id="f0a1b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f0a1b-129">System.String</span></span>

## <span data-ttu-id="f0a1b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0a1b-130">OUTPUTS</span></span>

### <span data-ttu-id="f0a1b-131">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0a1b-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="f0a1b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0a1b-132">NOTES</span></span>

## <span data-ttu-id="f0a1b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0a1b-133">RELATED LINKS</span></span>

[<span data-ttu-id="f0a1b-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f0a1b-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f0a1b-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f0a1b-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
