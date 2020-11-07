---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0749f964831962c946c5682db6c746da644cb0ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931913"
---
# <span data-ttu-id="219fa-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="219fa-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="219fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219fa-102">SYNOPSIS</span></span>
<span data-ttu-id="219fa-103">Bir Azure Application Gateway için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="219fa-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="219fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="219fa-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="219fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="219fa-105">DESCRIPTION</span></span>
<span data-ttu-id="219fa-106">**Yeni-AzApplicationGatewaySslCertificate** cmdlet 'ı bir Azure uygulama ağ GEÇIDI için SSL sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="219fa-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="219fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="219fa-107">EXAMPLES</span></span>

### <span data-ttu-id="219fa-108">Örnek 1: Azure Application Gateway için SSL sertifikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="219fa-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="219fa-109">Bu komut, Cert01 adlı bir SSL sertifikası oluşturur ve sonucu $Cert adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="219fa-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="219fa-110">Örnek 2: Keykasa gizliliğini (Version-Less secretId) kullanarak SSL sertifikası oluşturun ve uygulama ağ geçidine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="219fa-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="219fa-111">Parolayı alın ve kullanarak SSL sertifikası oluşturun `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="219fa-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="219fa-112">Not: burada sürüm-daha seyrek secretId sağlandığına göre, uygulama ağ geçidi sertifikayı anahtar kasası ile düzenli aralıklarla eşitler.</span><span class="sxs-lookup"><span data-stu-id="219fa-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="219fa-113">Örnek 3: Keykasa gizliliğini kullanarak SSL sertifikası oluşturun ve bir uygulama ağ geçidine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="219fa-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="219fa-114">Parolayı alın ve kullanarak SSL sertifikası oluşturun `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="219fa-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="219fa-115">Not: uygulama ağ geçidi 'nin sertifikayı anahtar kasası ile eşitlediği durumlarda, lütfen sürüm-daha seyrek secretId sağlayın.</span><span class="sxs-lookup"><span data-stu-id="219fa-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="219fa-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="219fa-116">PARAMETERS</span></span>

### <span data-ttu-id="219fa-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="219fa-117">-CertificateFile</span></span>
<span data-ttu-id="219fa-118">Bu cmdlet 'in oluşturduğu SSL sertifikasının. pfx dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="219fa-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219fa-119">-DefaultProfile</span></span>
<span data-ttu-id="219fa-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="219fa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="219fa-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="219fa-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="219fa-122">Anahtar Kasası parolasının SecretId (URI).</span><span class="sxs-lookup"><span data-stu-id="219fa-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="219fa-123">Belirli bir gizli sürümünün kullanılması gerekiyorsa bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="219fa-123">Use this option when a specific version of secret needs to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219fa-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="219fa-124">-Name</span></span>
<span data-ttu-id="219fa-125">Bu cmdlet 'in oluşturduğu SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="219fa-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="219fa-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="219fa-126">-Password</span></span>
<span data-ttu-id="219fa-127">Bu cmdlet 'in oluşturduğu SSL parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="219fa-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219fa-128">CommonParameters</span></span>
<span data-ttu-id="219fa-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="219fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219fa-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219fa-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="219fa-131">INPUTS</span></span>

### <span data-ttu-id="219fa-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="219fa-132">None</span></span>

## <span data-ttu-id="219fa-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="219fa-133">OUTPUTS</span></span>

### <span data-ttu-id="219fa-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="219fa-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="219fa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="219fa-135">NOTES</span></span>

## <span data-ttu-id="219fa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="219fa-136">RELATED LINKS</span></span>

[<span data-ttu-id="219fa-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="219fa-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="219fa-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="219fa-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="219fa-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="219fa-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="219fa-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="219fa-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


