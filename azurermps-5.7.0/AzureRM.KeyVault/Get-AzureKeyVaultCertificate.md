---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588909"
---
# <span data-ttu-id="72e79-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72e79-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="72e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72e79-102">SYNOPSIS</span></span>
<span data-ttu-id="72e79-103">Anahtar kasasından sertifika alır.</span><span class="sxs-lookup"><span data-stu-id="72e79-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72e79-104">SYNTAX</span></span>

### <span data-ttu-id="72e79-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72e79-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e79-106">Sertifika ve Rusça sürüm</span><span class="sxs-lookup"><span data-stu-id="72e79-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e79-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="72e79-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e79-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="72e79-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e79-109">Bycertificatenadeniz Vseçversioninputobject</span><span class="sxs-lookup"><span data-stu-id="72e79-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e79-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="72e79-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e79-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="72e79-111">DESCRIPTION</span></span>
<span data-ttu-id="72e79-112">**Get-AzureKeyVaultCertificate** cmdlet 'ı, Azure Anahtar Kasası 'ndaki anahtar kasasından belirtilen sertifikayı veya sertifika sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="72e79-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="72e79-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72e79-113">EXAMPLES</span></span>

### <span data-ttu-id="72e79-114">Örnek 1: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="72e79-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="72e79-115">Bu komut, ContosoKV01 adındaki anahtar kasasına TestCert01 adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="72e79-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="72e79-116">Örnek 2: Bu anahtar kasası için silinmiş ancak temizlenmiş tüm sertifikaları edinin.</span><span class="sxs-lookup"><span data-stu-id="72e79-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="72e79-117">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinen ancak temizlenmemayan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="72e79-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="72e79-118">Örnek 3: silinen, ancak bu Anahtar Kasası için temizlenmiş olan sertifikayı alma.</span><span class="sxs-lookup"><span data-stu-id="72e79-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="72e79-119">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmeden önce ' MyCert ' adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="72e79-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="72e79-120">Bu komut, silme tarihi ve bu silinmiş sertifikanın zamanlanmış temizleme tarihi gibi meta verileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="72e79-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="72e79-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72e79-121">PARAMETERS</span></span>

### <span data-ttu-id="72e79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e79-122">-DefaultProfile</span></span>
<span data-ttu-id="72e79-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72e79-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e79-124">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="72e79-124">-IncludeVersions</span></span>
<span data-ttu-id="72e79-125">Bu işlemin sertifikanın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72e79-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e79-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72e79-126">-InputObject</span></span>
<span data-ttu-id="72e79-127">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="72e79-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72e79-128">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="72e79-128">-InRemovedState</span></span>
<span data-ttu-id="72e79-129">Çıkışta önceden silinmiş sertifikaların eklenip eklenmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="72e79-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e79-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="72e79-130">-Name</span></span>
<span data-ttu-id="72e79-131">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72e79-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e79-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72e79-132">-VaultName</span></span>
<span data-ttu-id="72e79-133">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72e79-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e79-134">-Version</span><span class="sxs-lookup"><span data-stu-id="72e79-134">-Version</span></span>
<span data-ttu-id="72e79-135">Sertifikanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="72e79-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e79-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e79-136">CommonParameters</span></span>
<span data-ttu-id="72e79-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72e79-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e79-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e79-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e79-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72e79-139">INPUTS</span></span>

### <span data-ttu-id="72e79-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="72e79-140">None</span></span>
<span data-ttu-id="72e79-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="72e79-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72e79-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72e79-142">OUTPUTS</span></span>

### <span data-ttu-id="72e79-143">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem]</span><span class="sxs-lookup"><span data-stu-id="72e79-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="72e79-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72e79-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="72e79-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72e79-145">NOTES</span></span>

## <span data-ttu-id="72e79-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72e79-146">RELATED LINKS</span></span>

[<span data-ttu-id="72e79-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72e79-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="72e79-148">İçeri aktarma-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72e79-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="72e79-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72e79-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="72e79-150">Geri al-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="72e79-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
