---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592491"
---
# <span data-ttu-id="b3831-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3831-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="b3831-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3831-102">SYNOPSIS</span></span>
<span data-ttu-id="b3831-103">Önemli kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3831-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3831-104">SYNTAX</span></span>

### <span data-ttu-id="b3831-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3831-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3831-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="b3831-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3831-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="b3831-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3831-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="b3831-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3831-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="b3831-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3831-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="b3831-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3831-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3831-111">DESCRIPTION</span></span>
<span data-ttu-id="b3831-112">**Get-AzureKeyVaultKey** cmdlet 'ı Azure Key kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="b3831-113">Bu cmdlet, belirli bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** veya Anahtar Kasası veya sürüme göre tüm **anahtar paketi** nesnelerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="b3831-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3831-114">EXAMPLES</span></span>

### <span data-ttu-id="b3831-115">Örnek 1: anahtar kasasındaki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="b3831-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="b3831-116">Bu komut, contoso adlı anahtar kasasındaki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="b3831-117">Örnek 2: anahtarın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="b3831-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="b3831-118">Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="b3831-119">Örnek 3: anahtarın tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="b3831-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="b3831-120">Bu komut, contoso adındaki anahtar vaultile ıpfx adındaki anahtarın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="b3831-121">Örnek 4: anahtarın belirli bir sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="b3831-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="b3831-122">Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın belirli bir sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="b3831-123">Bu komutu çalıştırdıktan sonra, $Key nesnesinde gezinerek anahtarın çeşitli özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3831-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="b3831-124">Örnek 5: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm anahtarları edinin.</span><span class="sxs-lookup"><span data-stu-id="b3831-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="b3831-125">Bu komut, contoso adlı tuş kasasına önceden silinen ancak temizlenmemayan tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="b3831-126">Örnek 6: silinen, ancak bu Anahtar Kasası için temizlenmiş olan anahtar ıpfx 'i alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="b3831-127">Bu komut, contoso adlı Anahtar Kasası 'nda, daha önce silinmiş ancak temizlenmemişti olan anahtar.</span><span class="sxs-lookup"><span data-stu-id="b3831-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="b3831-128">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş anahtarın zamanlanan Temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3831-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="b3831-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3831-129">PARAMETERS</span></span>

### <span data-ttu-id="b3831-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3831-130">-DefaultProfile</span></span>
<span data-ttu-id="b3831-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3831-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3831-132">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="b3831-132">-IncludeVersions</span></span>
<span data-ttu-id="b3831-133">Bu cmdlet 'in bir anahtarın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3831-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="b3831-134">Anahtarın geçerli sürümü listedeki ilk sürümdür.</span><span class="sxs-lookup"><span data-stu-id="b3831-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="b3831-135">Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b3831-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="b3831-136">*Includeversions* parametresini belirtmezseniz, bu cmdlet anahtarın belirtilen *ada* sahip geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="b3831-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3831-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3831-137">-InputObject</span></span>
<span data-ttu-id="b3831-138">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b3831-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3831-139">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="b3831-139">-InRemovedState</span></span>
<span data-ttu-id="b3831-140">Çıktıda önceden silinen anahtarların gösterilip gösterilmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="b3831-140">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="b3831-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3831-141">-Name</span></span>
<span data-ttu-id="b3831-142">Alınacak anahtar paketi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3831-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3831-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b3831-143">-VaultName</span></span>
<span data-ttu-id="b3831-144">Bu cmdlet 'in anahtarları aldığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3831-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="b3831-145">Bu cmdlet, bu parametrenin belirttiği adı ve seçtiğiniz ortamı belirten bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3831-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3831-146">-Version</span><span class="sxs-lookup"><span data-stu-id="b3831-146">-Version</span></span>
<span data-ttu-id="b3831-147">Anahtar sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3831-147">Specifies the key version.</span></span>
<span data-ttu-id="b3831-148">Bu cmdlet, Anahtar Kasası adına, şu anda seçtiğiniz ortama, anahtar adına ve anahtar sürümüne bağlı olarak bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3831-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3831-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3831-149">CommonParameters</span></span>
<span data-ttu-id="b3831-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3831-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3831-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3831-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3831-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3831-152">INPUTS</span></span>

### <span data-ttu-id="b3831-153">Dizisi</span><span class="sxs-lookup"><span data-stu-id="b3831-153">String</span></span>

## <span data-ttu-id="b3831-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3831-154">OUTPUTS</span></span>

### <span data-ttu-id="b3831-155">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem>, Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey, liste<Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultkeyıdentityıtem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3831-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="b3831-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3831-156">NOTES</span></span>

## <span data-ttu-id="b3831-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3831-157">RELATED LINKS</span></span>

[<span data-ttu-id="b3831-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3831-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="b3831-159">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3831-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="b3831-160">Geri al-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="b3831-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="b3831-161">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="b3831-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

