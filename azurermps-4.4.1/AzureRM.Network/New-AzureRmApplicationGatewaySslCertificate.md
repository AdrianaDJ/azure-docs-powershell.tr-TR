---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: ad318c776662ebaeab3192ca584aa2aad7f2e20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589970"
---
# <span data-ttu-id="580b9-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="580b9-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="580b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="580b9-102">SYNOPSIS</span></span>
<span data-ttu-id="580b9-103">Bir Azure Application Gateway için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="580b9-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="580b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="580b9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="580b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="580b9-105">DESCRIPTION</span></span>
<span data-ttu-id="580b9-106">**New-AzureRmApplicationGatewaySslCertificate** cmdlet 'ı bir Azure Application Gateway için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="580b9-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="580b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="580b9-107">EXAMPLES</span></span>

### <span data-ttu-id="580b9-108">Örnek 1: Azure Application Gateway için SSL sertifikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="580b9-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\>$Cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="580b9-109">Bu komut, Cert01 adlı bir SSL sertifikası oluşturur ve sonucu $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="580b9-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="580b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="580b9-110">PARAMETERS</span></span>

### <span data-ttu-id="580b9-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="580b9-111">-CertificateFile</span></span>
<span data-ttu-id="580b9-112">Bu cmdlet 'in oluşturduğu SSL sertifikasının. pfx dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="580b9-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="580b9-113">-Name</span></span>
<span data-ttu-id="580b9-114">Bu cmdlet 'in oluşturduğu SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="580b9-114">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-115">-Parola</span><span class="sxs-lookup"><span data-stu-id="580b9-115">-Password</span></span>
<span data-ttu-id="580b9-116">Bu cmdlet 'in oluşturduğu SSL parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="580b9-116">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580b9-117">-DefaultProfile</span></span>
<span data-ttu-id="580b9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="580b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="580b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580b9-119">CommonParameters</span></span>
<span data-ttu-id="580b9-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="580b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580b9-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580b9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580b9-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="580b9-122">INPUTS</span></span>

### <span data-ttu-id="580b9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="580b9-123">System.String</span></span>

## <span data-ttu-id="580b9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="580b9-124">OUTPUTS</span></span>

### <span data-ttu-id="580b9-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="580b9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="580b9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="580b9-126">NOTES</span></span>

## <span data-ttu-id="580b9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="580b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="580b9-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="580b9-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="580b9-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="580b9-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="580b9-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="580b9-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="580b9-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="580b9-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


