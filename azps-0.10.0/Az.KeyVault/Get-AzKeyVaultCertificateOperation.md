---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 432e6ce1562a7f341cc9e121e1012354c5c67a93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935797"
---
# <span data-ttu-id="7abb5-101">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7abb5-101">Get-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7abb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7abb5-102">SYNOPSIS</span></span>
<span data-ttu-id="7abb5-103">Bir sertifika işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7abb5-103">Gets the status of a certificate operation.</span></span>

## <span data-ttu-id="7abb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7abb5-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7abb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7abb5-105">DESCRIPTION</span></span>
<span data-ttu-id="7abb5-106">**Get-Azanahtarvaultcertificateoperation** cmdlet 'i, sertifika işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7abb5-106">The **Get-AzKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="7abb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7abb5-107">EXAMPLES</span></span>

### <span data-ttu-id="7abb5-108">Örnek 1: sertifika işleminin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="7abb5-108">Example 1: Get the status of a certificate operation</span></span>
```
PS C:\>Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="7abb5-109">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifika işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7abb5-109">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="7abb5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7abb5-110">PARAMETERS</span></span>

### <span data-ttu-id="7abb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abb5-111">-DefaultProfile</span></span>
<span data-ttu-id="7abb5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7abb5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7abb5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7abb5-113">-Name</span></span>
<span data-ttu-id="7abb5-114">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7abb5-114">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abb5-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7abb5-115">-VaultName</span></span>
<span data-ttu-id="7abb5-116">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7abb5-116">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abb5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abb5-117">CommonParameters</span></span>
<span data-ttu-id="7abb5-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7abb5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abb5-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abb5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abb5-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7abb5-120">INPUTS</span></span>

### <span data-ttu-id="7abb5-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7abb5-121">None</span></span>
<span data-ttu-id="7abb5-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7abb5-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7abb5-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7abb5-123">OUTPUTS</span></span>

### <span data-ttu-id="7abb5-124">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7abb5-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7abb5-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7abb5-125">NOTES</span></span>

## <span data-ttu-id="7abb5-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7abb5-126">RELATED LINKS</span></span>

[<span data-ttu-id="7abb5-127">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7abb5-127">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="7abb5-128">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7abb5-128">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

