---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936673"
---
# <span data-ttu-id="7b8c7-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b8c7-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7b8c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8c7-103">Anahtarları anahtar kasası hizmeti tarafından yönetilecek şekilde belirtilen anahtar kasasına mevcut bir Azure depolama hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="7b8c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b8c7-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b8c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b8c7-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8c7-106">Depolama hesabı anahtarlarının anahtar kasası ile yönetilebilmesi için anahtar kasası ile mevcut bir Azure Depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="7b8c7-107">Depolama hesabı zaten var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-107">The Storage Account must already exist.</span></span> <span data-ttu-id="7b8c7-108">Depolama tuşları hiçbir zaman arayan kişiye gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="7b8c7-109">Anahtar Kasası otomatik yeniden üretir ve etkin anahtarı yeniden oluşturma dönemine göre geçirir.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="7b8c7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b8c7-110">EXAMPLES</span></span>

### <span data-ttu-id="7b8c7-111">Örnek 1: anahtarlarını yönetmek için anahtar kasası ile Azure depolama hesabı ayarlama</span><span class="sxs-lookup"><span data-stu-id="7b8c7-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="7b8c7-112">Anahtarları Anahtar Kasası tarafından yönetilecek Anahtar Kasası olan bir depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="7b8c7-113">Etkin anahtar kümesi: ' anahtar '.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-113">The active key set is 'key1'.</span></span> <span data-ttu-id="7b8c7-114">Bu anahtar SAS belirteçlerini oluşturmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="7b8c7-115">Anahtar Kasası, bu komutun zamanından sonraki yeniden oluşturma döneminden sonra ' anahtar2 ' tuşunu yeniden oluşturacak ve etkin anahtar olarak ayarlaedecektir.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="7b8c7-116">Bu otomatik yeniden oluşturma işlemi, 90 gün aralığı ile ' anahtar ' ve ' anahtar2 ' arasında devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="7b8c7-117">Örnek 2: anahtarlarını yönetmek için anahtar kasası ile klasik bir Azure depolama hesabı ayarlama</span><span class="sxs-lookup"><span data-stu-id="7b8c7-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="7b8c7-118">Anahtarlarının Anahtar Kasası tarafından yönetilmesi için Anahtar Kasası olan klasik depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="7b8c7-119">Etkin anahtar kümesi: ' birincil '.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="7b8c7-120">Bu anahtar SAS belirteçlerini oluşturmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="7b8c7-121">Anahtar Kasası, bu komutun zamanından sonraki yeniden oluşturma döneminden sonra ' Ikincil ' tuşunu yeniden oluşturacak ve etkin anahtar olarak ayarlaedecektir.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="7b8c7-122">Bu otomatik yeniden oluşturma işlemi, %90 günlük bir boşluk ile ' birincil ' ve ' Ikincil ' arasında devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="7b8c7-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b8c7-123">PARAMETERS</span></span>

### <span data-ttu-id="7b8c7-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7b8c7-124">-AccountName</span></span>
<span data-ttu-id="7b8c7-125">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="7b8c7-126">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-127">-Accountresourceıd</span><span class="sxs-lookup"><span data-stu-id="7b8c7-127">-AccountResourceId</span></span>
<span data-ttu-id="7b8c7-128">Depolama hesabının Azure kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="7b8c7-129">-ActiveKeyName</span></span>
<span data-ttu-id="7b8c7-130">SAS belirteçlerini oluşturmak için kullanılması gereken depolama hesabı anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8c7-131">-DefaultProfile</span></span>
<span data-ttu-id="7b8c7-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7b8c7-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-133">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="7b8c7-133">-Disable</span></span>
<span data-ttu-id="7b8c7-134">SAS belirteçlerinin oluşturulması için yönetilen depolama hesabı anahtarının kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="7b8c7-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="7b8c7-136">Otomatik yeniden üret tuşu.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-136">Auto regenerate key.</span></span> <span data-ttu-id="7b8c7-137">Doğruysa, yönetilen depolama hesabının etkin olmayan anahtarı otomatik olarak yeniden oluşturulur ve yeniden oluşturma döneminden sonra yeni etkin anahtar olur.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="7b8c7-138">Yanlışsa, yönetilen depolama hesabı anahtarları otomatik olarak oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="7b8c7-139">-RegenerationPeriod</span></span>
<span data-ttu-id="7b8c7-140">Yeniden oluşturma dönemi.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-140">Regeneration period.</span></span> <span data-ttu-id="7b8c7-141">Otomatik yeniden üret anahtarı etkinleştirilirse, bu değer, yönetilen depolama hesabının etkin olmayan anahtar otomatik olarak yeniden üretilmesinden sonraki ve yeni etkin anahtar haline gelir.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7b8c7-142">-Tag</span></span>
<span data-ttu-id="7b8c7-143">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b8c7-144">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7b8c7-144">For example:</span></span>

<span data-ttu-id="7b8c7-145">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="7b8c7-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7b8c7-146">-VaultName</span></span>
<span data-ttu-id="7b8c7-147">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-147">Vault name.</span></span>
<span data-ttu-id="7b8c7-148">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7b8c7-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b8c7-149">-Confirm</span></span>
<span data-ttu-id="7b8c7-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b8c7-151">-WhatIf</span></span>
<span data-ttu-id="7b8c7-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b8c7-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8c7-154">CommonParameters</span></span>
<span data-ttu-id="7b8c7-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8c7-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8c7-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8c7-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b8c7-157">INPUTS</span></span>

### <span data-ttu-id="7b8c7-158">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7b8c7-158">None</span></span>
<span data-ttu-id="7b8c7-159">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7b8c7-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b8c7-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b8c7-160">OUTPUTS</span></span>

### <span data-ttu-id="7b8c7-161">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b8c7-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="7b8c7-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b8c7-162">NOTES</span></span>

## <span data-ttu-id="7b8c7-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b8c7-163">RELATED LINKS</span></span>

[<span data-ttu-id="7b8c7-164">Az. Keykasa</span><span class="sxs-lookup"><span data-stu-id="7b8c7-164">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
