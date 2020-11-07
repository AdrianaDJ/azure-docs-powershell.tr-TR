---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7dddb6a5b38414d658cc405820327c0d6df43a6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760728"
---
# <span data-ttu-id="9dd94-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9dd94-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9dd94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd94-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd94-103">Uygulama ağ geçidine SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="9dd94-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9dd94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9dd94-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9dd94-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd94-106">**Add-AzApplicationGatewaySslCertificate** cmdlet 'i bir uygulama ağ geçidine SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="9dd94-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9dd94-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9dd94-107">EXAMPLES</span></span>

### <span data-ttu-id="9dd94-108">Örnek 1: PFX 'i uygulama ağ geçidine kullanarak SSL sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9dd94-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9dd94-109">Bu komut ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve ardından Cert01 adlı bir SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="9dd94-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="9dd94-110">Örnek 2: bir uygulama ağ geçidine Anahtar Kasası gizliliğini (sürüm-Less secretId) kullanarak SSL sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9dd94-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9dd94-111">Parolayı, `Add-AzApplicationGatewaySslCertificate` ad Içeren uygulama ağ geçidine eklemek için parolayı alın ve buna başvuru yapın `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="9dd94-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="9dd94-112">Not: burada sürüm-daha seyrek secretId sağlandığına göre, uygulama ağ geçidi sertifikayı anahtar kasası ile düzenli aralıklarla eşitler.</span><span class="sxs-lookup"><span data-stu-id="9dd94-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="9dd94-113">Örnek 3: Anahtar Kasası gizliliğini (sürümlü secretId) uygulama ağ geçidine kullanarak SSL sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9dd94-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9dd94-114">Parolayı, `Add-AzApplicationGatewaySslCertificate` ad Içeren uygulama ağ geçidine eklemek için parolayı alın ve buna başvuru yapın `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="9dd94-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="9dd94-115">Not: uygulama ağ geçidi 'nin sertifikayı anahtar kasası ile eşitlediği durumlarda, lütfen sürüm-daha seyrek secretId sağlayın.</span><span class="sxs-lookup"><span data-stu-id="9dd94-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="9dd94-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9dd94-116">PARAMETERS</span></span>

### <span data-ttu-id="9dd94-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dd94-117">-ApplicationGateway</span></span>
<span data-ttu-id="9dd94-118">Bu cmdlet 'in SSL sertifikası eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dd94-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="9dd94-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9dd94-119">-CertificateFile</span></span>
<span data-ttu-id="9dd94-120">Bu cmdlet 'in eklediği SSL sertifikasının. pfx dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dd94-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9dd94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd94-121">-DefaultProfile</span></span>
<span data-ttu-id="9dd94-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9dd94-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dd94-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="9dd94-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="9dd94-124">Anahtar Kasası parolasının SecretId (URI).</span><span class="sxs-lookup"><span data-stu-id="9dd94-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="9dd94-125">Belirli bir gizli sürümünün kullanılması gerekiyorsa bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="9dd94-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="9dd94-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9dd94-126">-Name</span></span>
<span data-ttu-id="9dd94-127">Bu cmdlet 'in eklediği SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dd94-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9dd94-128">-Parola</span><span class="sxs-lookup"><span data-stu-id="9dd94-128">-Password</span></span>
<span data-ttu-id="9dd94-129">Bu cmdlet 'in eklediği SSL sertifikasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dd94-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9dd94-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd94-130">CommonParameters</span></span>
<span data-ttu-id="9dd94-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9dd94-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd94-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd94-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd94-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9dd94-133">INPUTS</span></span>

### <span data-ttu-id="9dd94-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dd94-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9dd94-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9dd94-135">OUTPUTS</span></span>

### <span data-ttu-id="9dd94-136">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dd94-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9dd94-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9dd94-137">NOTES</span></span>

## <span data-ttu-id="9dd94-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9dd94-138">RELATED LINKS</span></span>

[<span data-ttu-id="9dd94-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9dd94-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9dd94-140">Yeni-Azapplicationgatewaysslsertifikası</span><span class="sxs-lookup"><span data-stu-id="9dd94-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9dd94-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9dd94-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9dd94-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9dd94-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


