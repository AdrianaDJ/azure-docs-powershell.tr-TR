---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 5935706c341fac5f0b26d3e4965f226342c3dfc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751684"
---
# <span data-ttu-id="e26a7-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e26a7-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e26a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e26a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e26a7-103">Anahtar kasasından sertifika alır.</span><span class="sxs-lookup"><span data-stu-id="e26a7-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="e26a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e26a7-104">SYNTAX</span></span>

### <span data-ttu-id="e26a7-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e26a7-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-106">Sertifika ve Rusça sürüm</span><span class="sxs-lookup"><span data-stu-id="e26a7-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="e26a7-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="e26a7-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-109">Bycertificatenadeniz Vseçversioninputobject</span><span class="sxs-lookup"><span data-stu-id="e26a7-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="e26a7-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-111">Binameresourceıd</span><span class="sxs-lookup"><span data-stu-id="e26a7-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-112">Vites Avenadeniz Vseçversionresourceıd</span><span class="sxs-lookup"><span data-stu-id="e26a7-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26a7-113">Bycertificateallversionsresourceıd</span><span class="sxs-lookup"><span data-stu-id="e26a7-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e26a7-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="e26a7-114">DESCRIPTION</span></span>
<span data-ttu-id="e26a7-115">**Get-Azanahtarvaultcertificate** cmdlet 'ı, Azure Anahtar Kasası 'ndaki anahtar kasasından belirtilen sertifikayı veya sertifika sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e26a7-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e26a7-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e26a7-116">EXAMPLES</span></span>

### <span data-ttu-id="e26a7-117">Örnek 1: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="e26a7-117">Example 1: Get a certificate</span></span>
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

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="e26a7-118">Bu komut, ContosoKV01 adındaki anahtar kasasına TestCert01 adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="e26a7-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="e26a7-119">Örnek 2: Bu anahtar kasası için silinmiş ancak temizlenmiş tüm sertifikaları edinin.</span><span class="sxs-lookup"><span data-stu-id="e26a7-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="e26a7-120">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinen ancak temizlenmemayan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="e26a7-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e26a7-121">Örnek 3: silinen, ancak bu Anahtar Kasası için temizlenmiş olan sertifikayı alma.</span><span class="sxs-lookup"><span data-stu-id="e26a7-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="e26a7-122">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmeden önce ' MyCert ' adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="e26a7-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e26a7-123">Bu komut, silme tarihi ve bu silinmiş sertifikanın zamanlanmış temizleme tarihi gibi meta verileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e26a7-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="e26a7-124">Örnek 4: filtreleme kullanarak sertifikaları listeleme</span><span class="sxs-lookup"><span data-stu-id="e26a7-124">Example 4: List certificates using filtering</span></span>
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

## <span data-ttu-id="e26a7-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e26a7-125">PARAMETERS</span></span>

### <span data-ttu-id="e26a7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26a7-126">-DefaultProfile</span></span>
<span data-ttu-id="e26a7-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e26a7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e26a7-128">-Inclubaðlý olarak</span><span class="sxs-lookup"><span data-stu-id="e26a7-128">-IncludePending</span></span>
<span data-ttu-id="e26a7-129">Beklemedeki sertifikaların çıktıya eklenip eklenmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="e26a7-129">Specifies whether to include pending certificates in the output</span></span>

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

### <span data-ttu-id="e26a7-130">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="e26a7-130">-IncludeVersions</span></span>
<span data-ttu-id="e26a7-131">Bu işlemin sertifikanın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e26a7-131">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="e26a7-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e26a7-132">-InputObject</span></span>
<span data-ttu-id="e26a7-133">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e26a7-133">KeyVault object.</span></span>

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

### <span data-ttu-id="e26a7-134">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="e26a7-134">-InRemovedState</span></span>
<span data-ttu-id="e26a7-135">Çıkışta önceden silinmiş sertifikaların eklenip eklenmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="e26a7-135">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="e26a7-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="e26a7-136">-Name</span></span>
<span data-ttu-id="e26a7-137">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e26a7-137">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e26a7-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e26a7-138">-ResourceId</span></span>
<span data-ttu-id="e26a7-139">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e26a7-139">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="e26a7-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e26a7-140">-VaultName</span></span>
<span data-ttu-id="e26a7-141">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e26a7-141">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="e26a7-142">-Version</span><span class="sxs-lookup"><span data-stu-id="e26a7-142">-Version</span></span>
<span data-ttu-id="e26a7-143">Sertifikanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e26a7-143">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="e26a7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26a7-144">CommonParameters</span></span>
<span data-ttu-id="e26a7-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e26a7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26a7-146">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e26a7-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26a7-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e26a7-147">INPUTS</span></span>

### <span data-ttu-id="e26a7-148">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="e26a7-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e26a7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e26a7-149">System.String</span></span>

## <span data-ttu-id="e26a7-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e26a7-150">OUTPUTS</span></span>

### <span data-ttu-id="e26a7-151">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="e26a7-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="e26a7-152">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e26a7-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="e26a7-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e26a7-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="e26a7-154">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="e26a7-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="e26a7-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e26a7-155">NOTES</span></span>

## <span data-ttu-id="e26a7-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e26a7-156">RELATED LINKS</span></span>

[<span data-ttu-id="e26a7-157">Add-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="e26a7-157">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="e26a7-158">Import-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="e26a7-158">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="e26a7-159">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e26a7-159">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="e26a7-160">Geri al-Azanahtarvaultsecretcertificate</span><span class="sxs-lookup"><span data-stu-id="e26a7-160">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
