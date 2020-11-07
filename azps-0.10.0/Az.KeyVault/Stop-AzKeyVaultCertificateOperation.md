---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/stop-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e1a4efc9709b7168e5de46ea0e19e2059f15243c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936646"
---
# <span data-ttu-id="4d1cb-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="4d1cb-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="4d1cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1cb-103">Anahtar Kasası 'nda sertifika işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="4d1cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d1cb-104">SYNTAX</span></span>

```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d1cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d1cb-105">DESCRIPTION</span></span>
<span data-ttu-id="4d1cb-106">**Dur-Azanahtarvaultcertificateoperation** cmdlet 'ı Azure Anahtar Kasası hizmetinde sertifika işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-106">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="4d1cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d1cb-107">EXAMPLES</span></span>

### <span data-ttu-id="4d1cb-108">Örnek 1: sertifika işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="4d1cb-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="4d1cb-109">Bu komut TestCert02 sertifika işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="4d1cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d1cb-110">PARAMETERS</span></span>

### <span data-ttu-id="4d1cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1cb-111">-DefaultProfile</span></span>
<span data-ttu-id="4d1cb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4d1cb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d1cb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4d1cb-113">-Force</span></span>
<span data-ttu-id="4d1cb-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cb-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d1cb-115">-Name</span></span>
<span data-ttu-id="4d1cb-116">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="4d1cb-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4d1cb-117">-VaultName</span></span>
<span data-ttu-id="4d1cb-118">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4d1cb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d1cb-119">-Confirm</span></span>
<span data-ttu-id="4d1cb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1cb-121">-WhatIf</span></span>
<span data-ttu-id="4d1cb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1cb-123">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1cb-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1cb-125">CommonParameters</span></span>
<span data-ttu-id="4d1cb-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1cb-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1cb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1cb-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d1cb-128">INPUTS</span></span>

### <span data-ttu-id="4d1cb-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4d1cb-129">None</span></span>
<span data-ttu-id="4d1cb-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4d1cb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d1cb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d1cb-131">OUTPUTS</span></span>

### <span data-ttu-id="4d1cb-132">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="4d1cb-132">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="4d1cb-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d1cb-133">NOTES</span></span>

## <span data-ttu-id="4d1cb-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d1cb-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d1cb-135">Get-Azanahtarvaultcertificateoperation</span><span class="sxs-lookup"><span data-stu-id="4d1cb-135">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="4d1cb-136">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="4d1cb-136">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

