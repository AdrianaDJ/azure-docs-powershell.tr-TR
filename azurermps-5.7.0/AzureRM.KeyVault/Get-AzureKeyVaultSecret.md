---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f2507d441dc04fd01217dde685deb667211f4034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594954"
---
# <span data-ttu-id="18021-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="18021-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="18021-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18021-102">SYNOPSIS</span></span>
<span data-ttu-id="18021-103">Anahtar kasasındaki gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="18021-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18021-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18021-104">SYNTAX</span></span>

### <span data-ttu-id="18021-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18021-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18021-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="18021-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18021-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="18021-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18021-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="18021-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18021-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="18021-109">ByInputObjectSecretName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18021-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="18021-110">ByInputObjectSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18021-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="18021-111">DESCRIPTION</span></span>
<span data-ttu-id="18021-112">**Get-AzureKeyVaultSecret** cmdlet 'i anahtar kasasındaki gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="18021-112">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="18021-113">Bu cmdlet, bir anahtar kasasındaki belirli bir gizliliği veya tüm gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="18021-113">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="18021-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18021-114">EXAMPLES</span></span>

### <span data-ttu-id="18021-115">Örnek 1: anahtar kasasındaki tüm gizliliklerin tüm geçerli sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="18021-115">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="18021-116">Bu komut, contoso adlı anahtar kasasındaki tüm gizliliklerin geçerli sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="18021-116">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="18021-117">Örnek 2: belirli bir gizliliğin tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="18021-117">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="18021-118">Bu komut, contoso adlı anahtar kasasındaki gizli adındaki gizli adı tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="18021-118">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="18021-119">Örnek 3: belirli bir parolanın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="18021-119">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="18021-120">Bu komut, contoso adlı anahtar kasasındaki gizli adlı parolanın geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="18021-120">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="18021-121">Örnek 4: belirli bir gizli sürümü alma</span><span class="sxs-lookup"><span data-stu-id="18021-121">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="18021-122">Bu komut, contoso adlı anahtar kasasındaki gizli adlı gizli bir sürümü alır.</span><span class="sxs-lookup"><span data-stu-id="18021-122">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="18021-123">Örnek 5: belirli bir parolanın geçerli sürümünün düz metin değerini alma</span><span class="sxs-lookup"><span data-stu-id="18021-123">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="18021-124">Bu komutlar, gizli adlı gizli adı olan geçerli sürümü alır ve bu gizliliğin düz metin değerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="18021-124">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="18021-125">Örnek 6: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm gizlilikleri alın.</span><span class="sxs-lookup"><span data-stu-id="18021-125">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="18021-126">Bu komut, contoso adlı tuş kasasına daha önce silinen ancak temizlenmediğim tüm gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="18021-126">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="18021-127">Örnek 7: silinen, ancak bu Anahtar Kasası için temizlenmedi gizli gizli kaldırmaları alır.</span><span class="sxs-lookup"><span data-stu-id="18021-127">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="18021-128">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmemişti gizli bir gizli kod dizesi alır.</span><span class="sxs-lookup"><span data-stu-id="18021-128">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="18021-129">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş gizliliğin zamanlanmış temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="18021-129">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="18021-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18021-130">PARAMETERS</span></span>

### <span data-ttu-id="18021-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18021-131">-DefaultProfile</span></span>
<span data-ttu-id="18021-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="18021-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18021-133">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="18021-133">-IncludeVersions</span></span>
<span data-ttu-id="18021-134">Bu cmdlet 'in tüm gizli sürümleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18021-134">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="18021-135">Bir parolanın geçerli sürümü listedeki ilk sürümdür.</span><span class="sxs-lookup"><span data-stu-id="18021-135">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="18021-136">Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="18021-136">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="18021-137">*Includeversions* parametresini belirtmezseniz, bu cmdlet parolanın belirtilen *adla* geçerli gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="18021-137">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18021-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18021-138">-InputObject</span></span>
<span data-ttu-id="18021-139">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="18021-139">KeyVault Object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18021-140">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="18021-140">-InRemovedState</span></span>
<span data-ttu-id="18021-141">Çıktıda önceden silinen gizliliklerin gösterilip gösterilmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="18021-141">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18021-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="18021-142">-Name</span></span>
<span data-ttu-id="18021-143">Alınacak parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18021-143">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18021-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="18021-144">-VaultName</span></span>
<span data-ttu-id="18021-145">Gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18021-145">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="18021-146">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18021-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18021-147">-Version</span><span class="sxs-lookup"><span data-stu-id="18021-147">-Version</span></span>
<span data-ttu-id="18021-148">Gizli sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18021-148">Specifies the secret version.</span></span>
<span data-ttu-id="18021-149">Bu cmdlet, Anahtar Kasası adına, şu anda seçili ortama, gizli adına ve gizli sürüme göre gizli bir FQDN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18021-149">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, ByInputObjectSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18021-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18021-150">CommonParameters</span></span>
<span data-ttu-id="18021-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18021-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18021-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18021-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18021-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18021-153">INPUTS</span></span>

### <span data-ttu-id="18021-154">Dizisi</span><span class="sxs-lookup"><span data-stu-id="18021-154">String</span></span>

## <span data-ttu-id="18021-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18021-155">OUTPUTS</span></span>

### <span data-ttu-id="18021-156">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem>, Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret, liste<Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultsecretidentityıtem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="18021-156">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="18021-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18021-157">NOTES</span></span>

## <span data-ttu-id="18021-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18021-158">RELATED LINKS</span></span>

[<span data-ttu-id="18021-159">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="18021-159">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="18021-160">Geri al-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="18021-160">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="18021-161">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="18021-161">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

