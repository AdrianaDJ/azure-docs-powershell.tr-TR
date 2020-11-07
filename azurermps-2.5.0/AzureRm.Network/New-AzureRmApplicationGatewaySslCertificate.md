---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938940"
---
# <span data-ttu-id="cfd04-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfd04-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cfd04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfd04-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd04-103">Bir Azure Application Gateway için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfd04-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfd04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfd04-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfd04-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfd04-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd04-106">**New-AzureRmApplicationGatewaySslCertificate** cmdlet 'ı bir Azure Application Gateway için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfd04-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cfd04-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfd04-107">EXAMPLES</span></span>

### <span data-ttu-id="cfd04-108">Örnek 1: Azure Application Gateway için SSL sertifikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cfd04-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="cfd04-109">Bu komut, Cert01 adlı bir SSL sertifikası oluşturur ve sonucu $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="cfd04-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="cfd04-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfd04-110">PARAMETERS</span></span>

### <span data-ttu-id="cfd04-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cfd04-111">-CertificateFile</span></span>
<span data-ttu-id="cfd04-112">Bu cmdlet 'in oluşturduğu SSL sertifikasının. pfx dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfd04-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd04-113">-DefaultProfile</span></span>
<span data-ttu-id="cfd04-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cfd04-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfd04-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cfd04-115">-Name</span></span>
<span data-ttu-id="cfd04-116">Bu cmdlet 'in oluşturduğu SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfd04-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd04-117">-Parola</span><span class="sxs-lookup"><span data-stu-id="cfd04-117">-Password</span></span>
<span data-ttu-id="cfd04-118">Bu cmdlet 'in oluşturduğu SSL parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfd04-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd04-119">CommonParameters</span></span>
<span data-ttu-id="cfd04-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfd04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd04-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd04-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd04-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfd04-122">INPUTS</span></span>

### <span data-ttu-id="cfd04-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cfd04-123">System.String</span></span>

## <span data-ttu-id="cfd04-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfd04-124">OUTPUTS</span></span>

### <span data-ttu-id="cfd04-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfd04-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cfd04-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfd04-126">NOTES</span></span>

## <span data-ttu-id="cfd04-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfd04-127">RELATED LINKS</span></span>

[<span data-ttu-id="cfd04-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfd04-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cfd04-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfd04-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cfd04-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfd04-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cfd04-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfd04-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


