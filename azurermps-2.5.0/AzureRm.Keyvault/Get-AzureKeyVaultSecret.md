---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 522268cb215a393ef54209b7606c8556d2566fd7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939726"
---
# <span data-ttu-id="71f93-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71f93-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="71f93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71f93-102">SYNOPSIS</span></span>
<span data-ttu-id="71f93-103">Anahtar kasasındaki gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71f93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71f93-104">SYNTAX</span></span>

### <span data-ttu-id="71f93-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="71f93-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f93-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="71f93-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f93-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="71f93-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f93-108">Bydeletedgizlilikler</span><span class="sxs-lookup"><span data-stu-id="71f93-108">ByDeletedSecrets</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71f93-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="71f93-109">DESCRIPTION</span></span>
<span data-ttu-id="71f93-110">**Get-AzureKeyVaultSecret** cmdlet 'i anahtar kasasındaki gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-110">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="71f93-111">Bu cmdlet, bir anahtar kasasındaki belirli bir gizliliği veya tüm gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="71f93-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71f93-112">EXAMPLES</span></span>

### <span data-ttu-id="71f93-113">Örnek 1: anahtar kasasındaki tüm gizliliklerin tüm geçerli sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="71f93-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="71f93-114">Bu komut, contoso adlı anahtar kasasındaki tüm gizliliklerin geçerli sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="71f93-115">Örnek 2: belirli bir gizliliğin tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="71f93-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="71f93-116">Bu komut, contoso adlı anahtar kasasındaki gizli adındaki gizli adı tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="71f93-117">Örnek 3: belirli bir parolanın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="71f93-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="71f93-118">Bu komut, contoso adlı anahtar kasasındaki gizli adlı parolanın geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="71f93-119">Örnek 4: belirli bir gizli sürümü alma</span><span class="sxs-lookup"><span data-stu-id="71f93-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="71f93-120">Bu komut, contoso adlı anahtar kasasındaki gizli adlı gizli bir sürümü alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="71f93-121">Örnek 5: belirli bir parolanın geçerli sürümünün düz metin değerini alma</span><span class="sxs-lookup"><span data-stu-id="71f93-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="71f93-122">Bu komutlar, gizli adlı gizli adı olan geçerli sürümü alır ve bu gizliliğin düz metin değerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="71f93-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="71f93-123">Örnek 6: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm gizlilikleri alın.</span><span class="sxs-lookup"><span data-stu-id="71f93-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="71f93-124">Bu komut, contoso adlı tuş kasasına daha önce silinen ancak temizlenmediğim tüm gizlilikleri alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="71f93-125">Örnek 7: silinen, ancak bu Anahtar Kasası için temizlenmedi gizli gizli kaldırmaları alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="71f93-126">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmemişti gizli bir gizli kod dizesi alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="71f93-127">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş gizliliğin zamanlanmış temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="71f93-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="71f93-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71f93-128">PARAMETERS</span></span>

### <span data-ttu-id="71f93-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f93-129">-DefaultProfile</span></span>
<span data-ttu-id="71f93-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="71f93-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71f93-131">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="71f93-131">-IncludeVersions</span></span>
<span data-ttu-id="71f93-132">Bu cmdlet 'in tüm gizli sürümleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="71f93-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="71f93-133">Bir parolanın geçerli sürümü listedeki ilk sürümdür.</span><span class="sxs-lookup"><span data-stu-id="71f93-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="71f93-134">Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="71f93-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="71f93-135">*Includeversions* parametresini belirtmezseniz, bu cmdlet parolanın belirtilen *adla* geçerli gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="71f93-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71f93-136">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="71f93-136">-InRemovedState</span></span>
<span data-ttu-id="71f93-137">Çıktıda önceden silinen gizliliklerin gösterilip gösterilmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="71f93-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71f93-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="71f93-138">-Name</span></span>
<span data-ttu-id="71f93-139">Alınacak parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71f93-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71f93-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="71f93-140">-VaultName</span></span>
<span data-ttu-id="71f93-141">Gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71f93-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="71f93-142">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71f93-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="71f93-143">-Version</span><span class="sxs-lookup"><span data-stu-id="71f93-143">-Version</span></span>
<span data-ttu-id="71f93-144">Gizli sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="71f93-144">Specifies the secret version.</span></span>
<span data-ttu-id="71f93-145">Bu cmdlet, Anahtar Kasası adına, şu anda seçili ortama, gizli adına ve gizli sürüme göre gizli bir FQDN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71f93-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71f93-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f93-146">CommonParameters</span></span>
<span data-ttu-id="71f93-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71f93-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f93-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71f93-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f93-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71f93-149">INPUTS</span></span>

### <span data-ttu-id="71f93-150">Dizisi</span><span class="sxs-lookup"><span data-stu-id="71f93-150">String</span></span>

## <span data-ttu-id="71f93-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71f93-151">OUTPUTS</span></span>

### <span data-ttu-id="71f93-152">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Secretidentityıtem>, Microsoft. Azure. Commands. keykasa. modeller. Secret, liste<Microsoft. Azure. Commands. Keykasa. modeller>.</span><span class="sxs-lookup"><span data-stu-id="71f93-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="71f93-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71f93-153">NOTES</span></span>

## <span data-ttu-id="71f93-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71f93-154">RELATED LINKS</span></span>

[<span data-ttu-id="71f93-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71f93-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="71f93-156">Geri al-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="71f93-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="71f93-157">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71f93-157">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)
