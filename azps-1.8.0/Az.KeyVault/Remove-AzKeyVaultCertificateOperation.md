---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e225ed4a76d753cc48d1b5bdd748d91ca986d963
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916276"
---
# <span data-ttu-id="0ce7a-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0ce7a-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0ce7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce7a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce7a-103">Anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="0ce7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ce7a-104">SYNTAX</span></span>

### <span data-ttu-id="0ce7a-105">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="0ce7a-105">Default</span></span>
```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ce7a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0ce7a-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ce7a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ce7a-107">DESCRIPTION</span></span>
<span data-ttu-id="0ce7a-108">**Remove-AzKeyVaultCertificateOperation** cmdlet 'i anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-108">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="0ce7a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ce7a-109">EXAMPLES</span></span>

### <span data-ttu-id="0ce7a-110">Örnek 1: sertifika işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0ce7a-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

Id                        : https://contosokv01.vault.azure.net/certificates/testcert01/pending
Status                    : completed
StatusDetails             :
RequestId                 : f5dfd2ae486149a594dc98e800dceaaa
Target                    : https://contosokv01.vault.azure.net/certificates/testcert01
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
                            ==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="0ce7a-111">Bu komut, TestCert01 adındaki sertifika işlemini, onay istemeden ContosoKV01 anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="0ce7a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ce7a-112">PARAMETERS</span></span>

### <span data-ttu-id="0ce7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce7a-113">-DefaultProfile</span></span>
<span data-ttu-id="0ce7a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0ce7a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0ce7a-115">-Force</span></span>
<span data-ttu-id="0ce7a-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ce7a-117">-InputObject</span></span>
<span data-ttu-id="0ce7a-118">İşlem nesnesi</span><span class="sxs-lookup"><span data-stu-id="0ce7a-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ce7a-119">-Name</span></span>
<span data-ttu-id="0ce7a-120">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0ce7a-121">-PassThru</span></span>
<span data-ttu-id="0ce7a-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ce7a-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0ce7a-124">-VaultName</span></span>
<span data-ttu-id="0ce7a-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ce7a-126">-Confirm</span></span>
<span data-ttu-id="0ce7a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce7a-128">-WhatIf</span></span>
<span data-ttu-id="0ce7a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce7a-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce7a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce7a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce7a-132">CommonParameters</span></span>
<span data-ttu-id="0ce7a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce7a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce7a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce7a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ce7a-135">INPUTS</span></span>

### <span data-ttu-id="0ce7a-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0ce7a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0ce7a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ce7a-137">OUTPUTS</span></span>

### <span data-ttu-id="0ce7a-138">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0ce7a-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0ce7a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ce7a-139">NOTES</span></span>

## <span data-ttu-id="0ce7a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ce7a-140">RELATED LINKS</span></span>

[<span data-ttu-id="0ce7a-141">Get-Azanahtarvaultcertificateoperation</span><span class="sxs-lookup"><span data-stu-id="0ce7a-141">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="0ce7a-142">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0ce7a-142">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)
