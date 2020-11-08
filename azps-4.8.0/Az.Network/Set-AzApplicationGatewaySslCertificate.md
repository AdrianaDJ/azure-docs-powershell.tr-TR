---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108843"
---
# <span data-ttu-id="19655-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="19655-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="19655-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19655-102">SYNOPSIS</span></span>
<span data-ttu-id="19655-103">Uygulama ağ geçidi için SSL sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19655-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="19655-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19655-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19655-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19655-105">DESCRIPTION</span></span>
<span data-ttu-id="19655-106">**Set-AzApplicationGatewaySslCertificate** cmdlet 'i, bir uygulama ağ GEÇIDI için SSL sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19655-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="19655-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19655-107">EXAMPLES</span></span>

### <span data-ttu-id="19655-108">Örnek 1: uygulama ağ geçidinde mevcut SSL sertifikasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="19655-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="19655-109">ApplicationGateway01 adlı uygulama ağ geçidi için varolan SSL sertifikasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="19655-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="19655-110">Örnek 2: uygulama ağ geçidinde Anahtar Kasası gizliliğini (sürüm-Less secretId) kullanarak var olan SSL sertifikasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="19655-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="19655-111">Parolayı edinin ve kullanarak var olan SSL sertifikasını güncelleyin `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="19655-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="19655-112">Örnek 3: uygulama ağ geçidinde Keykasa gizliliğini kullanarak var olan SSL sertifikasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="19655-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="19655-113">Parolayı edinin ve kullanarak var olan SSL sertifikasını güncelleyin `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="19655-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="19655-114">Not: uygulama ağ geçidi 'nin sertifikayı anahtar kasası ile eşitlediği durumlarda, lütfen sürüm-daha seyrek secretId sağlayın.</span><span class="sxs-lookup"><span data-stu-id="19655-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="19655-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19655-115">PARAMETERS</span></span>

### <span data-ttu-id="19655-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19655-116">-ApplicationGateway</span></span>
<span data-ttu-id="19655-117">Güvenli Yuva Katmanı (SSL) sertifikasının ilişkili olduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19655-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19655-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="19655-118">-CertificateFile</span></span>
<span data-ttu-id="19655-119">SSL sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="19655-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="19655-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19655-120">-DefaultProfile</span></span>
<span data-ttu-id="19655-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19655-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19655-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="19655-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="19655-123">Anahtar Kasası parolasının SecretId (URI).</span><span class="sxs-lookup"><span data-stu-id="19655-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="19655-124">Belirli bir gizli sürümünün kullanılması gerekiyorsa bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="19655-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="19655-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="19655-125">-Name</span></span>
<span data-ttu-id="19655-126">SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19655-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="19655-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="19655-127">-Password</span></span>
<span data-ttu-id="19655-128">SSL sertifikasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19655-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="19655-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19655-129">CommonParameters</span></span>
<span data-ttu-id="19655-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19655-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19655-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19655-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19655-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19655-132">INPUTS</span></span>

### <span data-ttu-id="19655-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19655-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19655-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19655-134">OUTPUTS</span></span>

### <span data-ttu-id="19655-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19655-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19655-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19655-136">NOTES</span></span>

## <span data-ttu-id="19655-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19655-137">RELATED LINKS</span></span>

[<span data-ttu-id="19655-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="19655-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="19655-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="19655-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="19655-140">Yeni-Azapplicationgatewaysslsertifikası</span><span class="sxs-lookup"><span data-stu-id="19655-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="19655-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="19655-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


