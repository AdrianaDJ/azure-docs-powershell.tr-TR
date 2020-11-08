---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: ede0598162fdecc760f33646c86171501ec46db4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280228"
---
# <span data-ttu-id="fef4a-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fef4a-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="fef4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef4a-102">SYNOPSIS</span></span>
<span data-ttu-id="fef4a-103">Anahtar kasasından sertifika alır.</span><span class="sxs-lookup"><span data-stu-id="fef4a-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="fef4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fef4a-104">SYNTAX</span></span>

### <span data-ttu-id="fef4a-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fef4a-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-106">Sertifika ve Rusça sürüm</span><span class="sxs-lookup"><span data-stu-id="fef4a-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="fef4a-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="fef4a-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-109">Bycertificatenadeniz Vseçversioninputobject</span><span class="sxs-lookup"><span data-stu-id="fef4a-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="fef4a-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-111">Binameresourceıd</span><span class="sxs-lookup"><span data-stu-id="fef4a-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-112">Vites Avenadeniz Vseçversionresourceıd</span><span class="sxs-lookup"><span data-stu-id="fef4a-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4a-113">Bycertificateallversionsresourceıd</span><span class="sxs-lookup"><span data-stu-id="fef4a-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef4a-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="fef4a-114">DESCRIPTION</span></span>
<span data-ttu-id="fef4a-115">**Get-Azanahtarvaultcertificate** cmdlet 'ı, Azure Anahtar Kasası 'ndaki anahtar kasasından belirtilen sertifikayı veya sertifika sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fef4a-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fef4a-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fef4a-116">EXAMPLES</span></span>

### <span data-ttu-id="fef4a-117">Örnek 1: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="fef4a-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="fef4a-118">Örnek 2: sertifika alma ve PFX olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="fef4a-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="fef4a-119">Bu komut, ContosoKV01 adındaki anahtar kasasına TestCert01 adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="fef4a-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="fef4a-120">Sertifikayı pfx dosyası olarak indirmek için, aşağıdaki komutu çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fef4a-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="fef4a-121">Bu komutlar SecretId öğesine erişir ve içeriği bir PFX dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fef4a-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name
$secretValueText = '';
$ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
try {
    $secretValueText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}
$secretByte = [Convert]::FromBase64String($secretValueText)
$x509Cert = new-object System.Security.Cryptography.X509Certificates.X509Certificate2
$x509Cert.Import($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="fef4a-122">Örnek 3: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm sertifikaları edinin.</span><span class="sxs-lookup"><span data-stu-id="fef4a-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="fef4a-123">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinen ancak temizlenmemayan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="fef4a-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="fef4a-124">Örnek 4: silinen, ancak bu Anahtar Kasası için temizlenmediğim sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="fef4a-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="fef4a-125">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmeden önce ' MyCert ' adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="fef4a-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="fef4a-126">Bu komut, silme tarihi ve bu silinmiş sertifikanın zamanlanmış temizleme tarihi gibi meta verileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fef4a-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="fef4a-127">Örnek 5: filtreleme kullanarak sertifikaları listeleme</span><span class="sxs-lookup"><span data-stu-id="fef4a-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="fef4a-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fef4a-128">PARAMETERS</span></span>

### <span data-ttu-id="fef4a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef4a-129">-DefaultProfile</span></span>
<span data-ttu-id="fef4a-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fef4a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fef4a-131">-Inclubaðlý olarak</span><span class="sxs-lookup"><span data-stu-id="fef4a-131">-IncludePending</span></span>
<span data-ttu-id="fef4a-132">Beklemedeki sertifikaların çıktıya eklenip eklenmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="fef4a-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-133">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="fef4a-133">-IncludeVersions</span></span>
<span data-ttu-id="fef4a-134">Bu işlemin sertifikanın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fef4a-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fef4a-135">-InputObject</span></span>
<span data-ttu-id="fef4a-136">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fef4a-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-137">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="fef4a-137">-InRemovedState</span></span>
<span data-ttu-id="fef4a-138">Çıkışta önceden silinmiş sertifikaların eklenip eklenmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="fef4a-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="fef4a-139">-Name</span></span>
<span data-ttu-id="fef4a-140">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef4a-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fef4a-141">-ResourceId</span></span>
<span data-ttu-id="fef4a-142">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fef4a-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fef4a-143">-VaultName</span></span>
<span data-ttu-id="fef4a-144">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef4a-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-145">-Version</span><span class="sxs-lookup"><span data-stu-id="fef4a-145">-Version</span></span>
<span data-ttu-id="fef4a-146">Sertifikanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef4a-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef4a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef4a-147">CommonParameters</span></span>
<span data-ttu-id="fef4a-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fef4a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef4a-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fef4a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef4a-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fef4a-150">INPUTS</span></span>

### <span data-ttu-id="fef4a-151">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="fef4a-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fef4a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="fef4a-152">System.String</span></span>

## <span data-ttu-id="fef4a-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fef4a-153">OUTPUTS</span></span>

### <span data-ttu-id="fef4a-154">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="fef4a-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="fef4a-155">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fef4a-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="fef4a-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fef4a-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="fef4a-157">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="fef4a-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="fef4a-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fef4a-158">NOTES</span></span>

## <span data-ttu-id="fef4a-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fef4a-159">RELATED LINKS</span></span>

[<span data-ttu-id="fef4a-160">Add-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="fef4a-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="fef4a-161">Import-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="fef4a-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="fef4a-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fef4a-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="fef4a-163">Geri al-Azanahtarvaultsecretcertificate</span><span class="sxs-lookup"><span data-stu-id="fef4a-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
