---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935414"
---
# <span data-ttu-id="12f42-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12f42-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="12f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12f42-102">SYNOPSIS</span></span>
<span data-ttu-id="12f42-103">Bir Azure Application Gateway için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12f42-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="12f42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12f42-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12f42-105">DESCRIPTION</span></span>
<span data-ttu-id="12f42-106">**Yeni-AzApplicationGatewaySslCertificate** cmdlet 'ı bir Azure uygulama ağ GEÇIDI için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12f42-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="12f42-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12f42-107">EXAMPLES</span></span>

### <span data-ttu-id="12f42-108">Örnek 1: Azure Application Gateway için SSL sertifikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="12f42-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="12f42-109">Bu komut, Cert01 adlı bir SSL sertifikası oluşturur ve sonucu $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="12f42-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="12f42-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12f42-110">PARAMETERS</span></span>

### <span data-ttu-id="12f42-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="12f42-111">-CertificateFile</span></span>
<span data-ttu-id="12f42-112">Bu cmdlet 'in oluşturduğu SSL sertifikasının. pfx dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="12f42-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="12f42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f42-113">-DefaultProfile</span></span>
<span data-ttu-id="12f42-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12f42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12f42-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="12f42-115">-Name</span></span>
<span data-ttu-id="12f42-116">Bu cmdlet 'in oluşturduğu SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12f42-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="12f42-117">-Parola</span><span class="sxs-lookup"><span data-stu-id="12f42-117">-Password</span></span>
<span data-ttu-id="12f42-118">Bu cmdlet 'in oluşturduğu SSL parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12f42-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="12f42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f42-119">CommonParameters</span></span>
<span data-ttu-id="12f42-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12f42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f42-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f42-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f42-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12f42-122">INPUTS</span></span>

### <span data-ttu-id="12f42-123">System. String</span><span class="sxs-lookup"><span data-stu-id="12f42-123">System.String</span></span>

## <span data-ttu-id="12f42-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12f42-124">OUTPUTS</span></span>

### <span data-ttu-id="12f42-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12f42-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="12f42-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12f42-126">NOTES</span></span>

## <span data-ttu-id="12f42-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12f42-127">RELATED LINKS</span></span>

[<span data-ttu-id="12f42-128">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12f42-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="12f42-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12f42-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="12f42-130">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12f42-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="12f42-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12f42-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


