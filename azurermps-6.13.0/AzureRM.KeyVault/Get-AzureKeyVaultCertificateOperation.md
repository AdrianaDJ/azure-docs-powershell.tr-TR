---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: bc5b7b47c5567867a857ab32fe34c287e896ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593250"
---
# <span data-ttu-id="1a0aa-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1a0aa-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1a0aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0aa-103">Bir sertifika işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a0aa-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a0aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a0aa-104">SYNTAX</span></span>

### <span data-ttu-id="1a0aa-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a0aa-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a0aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a0aa-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a0aa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a0aa-107">DESCRIPTION</span></span>
<span data-ttu-id="1a0aa-108">**Get-AzureKeyVaultCertificateOperation** cmdlet 'i, sertifika işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a0aa-108">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="1a0aa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a0aa-109">EXAMPLES</span></span>

### <span data-ttu-id="1a0aa-110">Örnek 1: sertifika işleminin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="1a0aa-110">Example 1: Get the status of a certificate operation</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateOperation -VaultName "contosoKV01" -Name "TestCert01"

Id                        : https://contosoKV01.vault.azure.net/certificates/TestCert01/pending
Status                    : inProgress
StatusDetails             : Pending certificate created. Certificate request is in progress. This may take some time
                            based on the issuer provider. Please check again later.
RequestId                 : 32a63e80568442a2892dafb9f7cf366t
Target                    :
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="1a0aa-111">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifika işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a0aa-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="1a0aa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a0aa-112">PARAMETERS</span></span>

### <span data-ttu-id="1a0aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0aa-113">-DefaultProfile</span></span>
<span data-ttu-id="1a0aa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1a0aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a0aa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a0aa-115">-InputObject</span></span>
<span data-ttu-id="1a0aa-116">Sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1a0aa-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0aa-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a0aa-117">-Name</span></span>
<span data-ttu-id="1a0aa-118">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a0aa-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0aa-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1a0aa-119">-VaultName</span></span>
<span data-ttu-id="1a0aa-120">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a0aa-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0aa-121">CommonParameters</span></span>
<span data-ttu-id="1a0aa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a0aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0aa-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a0aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0aa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a0aa-124">INPUTS</span></span>

### <span data-ttu-id="1a0aa-125">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="1a0aa-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="1a0aa-126">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a0aa-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1a0aa-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a0aa-127">OUTPUTS</span></span>

### <span data-ttu-id="1a0aa-128">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1a0aa-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1a0aa-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a0aa-129">NOTES</span></span>

## <span data-ttu-id="1a0aa-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a0aa-130">RELATED LINKS</span></span>

[<span data-ttu-id="1a0aa-131">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1a0aa-131">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="1a0aa-132">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1a0aa-132">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

