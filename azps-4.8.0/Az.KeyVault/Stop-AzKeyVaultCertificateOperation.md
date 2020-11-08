---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e260b32e847705240d93451b32bef9ae31d7fa07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267185"
---
# <span data-ttu-id="a0725-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a0725-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a0725-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0725-102">SYNOPSIS</span></span>
<span data-ttu-id="a0725-103">Anahtar Kasası 'nda sertifika işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a0725-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="a0725-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0725-104">SYNTAX</span></span>

### <span data-ttu-id="a0725-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0725-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0725-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a0725-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0725-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0725-107">DESCRIPTION</span></span>
<span data-ttu-id="a0725-108">**Dur-Azanahtarvaultcertificateoperation** cmdlet 'ı Azure Anahtar Kasası hizmetinde sertifika işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a0725-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="a0725-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0725-109">EXAMPLES</span></span>

### <span data-ttu-id="a0725-110">Örnek 1: sertifika işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="a0725-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

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

<span data-ttu-id="a0725-111">Bu komut TestCert02 sertifika işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a0725-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="a0725-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0725-112">PARAMETERS</span></span>

### <span data-ttu-id="a0725-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0725-113">-DefaultProfile</span></span>
<span data-ttu-id="a0725-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0725-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0725-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0725-115">-Force</span></span>
<span data-ttu-id="a0725-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a0725-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0725-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0725-117">-InputObject</span></span>
<span data-ttu-id="a0725-118">İşlem nesnesi</span><span class="sxs-lookup"><span data-stu-id="a0725-118">Operation object</span></span>

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

### <span data-ttu-id="a0725-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0725-119">-Name</span></span>
<span data-ttu-id="a0725-120">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0725-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="a0725-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a0725-121">-VaultName</span></span>
<span data-ttu-id="a0725-122">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0725-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a0725-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0725-123">-Confirm</span></span>
<span data-ttu-id="a0725-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0725-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0725-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0725-125">-WhatIf</span></span>
<span data-ttu-id="a0725-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0725-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0725-127">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0725-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0725-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0725-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0725-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0725-129">CommonParameters</span></span>
<span data-ttu-id="a0725-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0725-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0725-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0725-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0725-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0725-132">INPUTS</span></span>

### <span data-ttu-id="a0725-133">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a0725-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a0725-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0725-134">OUTPUTS</span></span>

### <span data-ttu-id="a0725-135">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a0725-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a0725-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0725-136">NOTES</span></span>

## <span data-ttu-id="a0725-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0725-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0725-138">Get-Azanahtarvaultcertificateoperation</span><span class="sxs-lookup"><span data-stu-id="a0725-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="a0725-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a0725-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

