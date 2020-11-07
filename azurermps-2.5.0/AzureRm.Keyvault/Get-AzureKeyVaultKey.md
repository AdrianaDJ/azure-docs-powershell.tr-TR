---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 5ebb9ca4a59f713ec81e5099cd3bbcc91084ac4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939556"
---
# <span data-ttu-id="e0a12-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e0a12-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="e0a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a12-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a12-103">Önemli kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0a12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0a12-104">SYNTAX</span></span>

### <span data-ttu-id="e0a12-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0a12-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0a12-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="e0a12-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0a12-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="e0a12-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0a12-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="e0a12-108">ByDeletedKey</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a12-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0a12-109">DESCRIPTION</span></span>
<span data-ttu-id="e0a12-110">**Get-AzureKeyVaultKey** cmdlet 'ı Azure Key kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-110">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="e0a12-111">Bu cmdlet, belirli bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** veya Anahtar Kasası veya sürüme göre tüm **anahtar paketi** nesnelerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="e0a12-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0a12-112">EXAMPLES</span></span>

### <span data-ttu-id="e0a12-113">Örnek 1: anahtar kasasındaki tüm anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="e0a12-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="e0a12-114">Bu komut, contoso adlı anahtar kasasındaki tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="e0a12-115">Örnek 2: anahtarın geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="e0a12-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="e0a12-116">Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="e0a12-117">Örnek 3: anahtarın tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="e0a12-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="e0a12-118">Bu komut, contoso adındaki anahtar vaultile ıpfx adındaki anahtarın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="e0a12-119">Örnek 4: anahtarın belirli bir sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="e0a12-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="e0a12-120">Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın belirli bir sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="e0a12-121">Bu komutu çalıştırdıktan sonra, $Key nesnesinde gezinerek anahtarın çeşitli özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0a12-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="e0a12-122">Örnek 5: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm anahtarları edinin.</span><span class="sxs-lookup"><span data-stu-id="e0a12-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="e0a12-123">Bu komut, contoso adlı tuş kasasına önceden silinen ancak temizlenmemayan tüm anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e0a12-124">Örnek 6: silinen, ancak bu Anahtar Kasası için temizlenmiş olan anahtar ıpfx 'i alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="e0a12-125">Bu komut, contoso adlı Anahtar Kasası 'nda, daha önce silinmiş ancak temizlenmemişti olan anahtar.</span><span class="sxs-lookup"><span data-stu-id="e0a12-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e0a12-126">Bu komut, silme tarihi gibi meta verileri ve bu silinmiş anahtarın zamanlanan Temizleme tarihini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e0a12-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="e0a12-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0a12-127">PARAMETERS</span></span>

### <span data-ttu-id="e0a12-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a12-128">-DefaultProfile</span></span>
<span data-ttu-id="e0a12-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e0a12-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0a12-130">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="e0a12-130">-IncludeVersions</span></span>
<span data-ttu-id="e0a12-131">Bu cmdlet 'in bir anahtarın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0a12-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="e0a12-132">Anahtarın geçerli sürümü listedeki ilk sürümdür.</span><span class="sxs-lookup"><span data-stu-id="e0a12-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="e0a12-133">Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e0a12-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="e0a12-134">*Includeversions* parametresini belirtmezseniz, bu cmdlet anahtarın belirtilen *ada* sahip geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e0a12-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a12-135">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="e0a12-135">-InRemovedState</span></span>
<span data-ttu-id="e0a12-136">Çıktıda önceden silinen anahtarların gösterilip gösterilmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="e0a12-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a12-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0a12-137">-Name</span></span>
<span data-ttu-id="e0a12-138">Alınacak anahtar paketi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0a12-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a12-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e0a12-139">-VaultName</span></span>
<span data-ttu-id="e0a12-140">Bu cmdlet 'in anahtarları aldığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0a12-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="e0a12-141">Bu cmdlet, bu parametrenin belirttiği adı ve seçtiğiniz ortamı belirten bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0a12-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="e0a12-142">-Version</span><span class="sxs-lookup"><span data-stu-id="e0a12-142">-Version</span></span>
<span data-ttu-id="e0a12-143">Anahtar sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0a12-143">Specifies the key version.</span></span>
<span data-ttu-id="e0a12-144">Bu cmdlet, Anahtar Kasası adına, şu anda seçtiğiniz ortama, anahtar adına ve anahtar sürümüne bağlı olarak bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0a12-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a12-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a12-145">CommonParameters</span></span>
<span data-ttu-id="e0a12-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0a12-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a12-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0a12-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a12-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0a12-148">INPUTS</span></span>

### <span data-ttu-id="e0a12-149">Dizisi</span><span class="sxs-lookup"><span data-stu-id="e0a12-149">String</span></span>

## <span data-ttu-id="e0a12-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0a12-150">OUTPUTS</span></span>

### <span data-ttu-id="e0a12-151">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Keyıdentityıtem>, Microsoft. Azure. Commands. keykasa. modeller., liste<Microsoft. Azure. Commands. keykasa. modeller>.</span><span class="sxs-lookup"><span data-stu-id="e0a12-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="e0a12-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0a12-152">NOTES</span></span>

## <span data-ttu-id="e0a12-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0a12-153">RELATED LINKS</span></span>

[<span data-ttu-id="e0a12-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e0a12-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="e0a12-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e0a12-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="e0a12-156">Geri al-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="e0a12-156">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="e0a12-157">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="e0a12-157">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

