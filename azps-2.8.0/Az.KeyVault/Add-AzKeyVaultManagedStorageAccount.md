---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 56883ecc1ca562ed4a259be9d1940683e652a280
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751700"
---
# <span data-ttu-id="d2480-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2480-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d2480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2480-102">SYNOPSIS</span></span>
<span data-ttu-id="d2480-103">Anahtarları anahtar kasası hizmeti tarafından yönetilecek şekilde belirtilen anahtar kasasına mevcut bir Azure depolama hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="d2480-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="d2480-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2480-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2480-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2480-105">DESCRIPTION</span></span>
<span data-ttu-id="d2480-106">Depolama hesabı anahtarlarının anahtar kasası ile yönetilebilmesi için anahtar kasası ile mevcut bir Azure Depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d2480-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="d2480-107">Depolama hesabı zaten var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d2480-107">The Storage Account must already exist.</span></span> <span data-ttu-id="d2480-108">Depolama tuşları hiçbir zaman arayan kişiye gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="d2480-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="d2480-109">Anahtar Kasası otomatik yeniden üretir ve etkin anahtarı yeniden oluşturma dönemine göre geçirir.</span><span class="sxs-lookup"><span data-stu-id="d2480-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="d2480-110">Bu özelliğe genel bakış için [Azure Key Kasası yönetimli depolama hesabı-PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="d2480-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="d2480-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2480-111">EXAMPLES</span></span>

### <span data-ttu-id="d2480-112">Örnek 1: anahtarlarını yönetmek için anahtar kasası ile Azure depolama hesabı ayarlama</span><span class="sxs-lookup"><span data-stu-id="d2480-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="d2480-113">Anahtarları Anahtar Kasası tarafından yönetilecek Anahtar Kasası olan bir depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d2480-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="d2480-114">Etkin anahtar kümesi: ' anahtar '.</span><span class="sxs-lookup"><span data-stu-id="d2480-114">The active key set is 'key1'.</span></span> <span data-ttu-id="d2480-115">Bu anahtar SAS belirteçlerini oluşturmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="d2480-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="d2480-116">Anahtar Kasası, bu komutun zamanından sonraki yeniden oluşturma döneminden sonra ' anahtar2 ' tuşunu yeniden oluşturacak ve etkin anahtar olarak ayarlaedecektir.</span><span class="sxs-lookup"><span data-stu-id="d2480-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="d2480-117">Bu otomatik yeniden oluşturma işlemi, 90 gün aralığı ile ' anahtar ' ve ' anahtar2 ' arasında devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="d2480-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="d2480-118">Örnek 2: anahtarlarını yönetmek için anahtar kasası ile klasik bir Azure depolama hesabı ayarlama</span><span class="sxs-lookup"><span data-stu-id="d2480-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="d2480-119">Anahtarlarının Anahtar Kasası tarafından yönetilmesi için Anahtar Kasası olan klasik depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d2480-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="d2480-120">Etkin anahtar kümesi: ' birincil '.</span><span class="sxs-lookup"><span data-stu-id="d2480-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="d2480-121">Bu anahtar SAS belirteçlerini oluşturmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="d2480-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="d2480-122">Anahtar Kasası, bu komutun zamanından sonraki yeniden oluşturma döneminden sonra ' Ikincil ' tuşunu yeniden oluşturacak ve etkin anahtar olarak ayarlaedecektir.</span><span class="sxs-lookup"><span data-stu-id="d2480-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="d2480-123">Bu otomatik yeniden oluşturma işlemi, %90 günlük bir boşluk ile ' birincil ' ve ' Ikincil ' arasında devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="d2480-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="d2480-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2480-124">PARAMETERS</span></span>

### <span data-ttu-id="d2480-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2480-125">-AccountName</span></span>
<span data-ttu-id="d2480-126">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="d2480-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="d2480-127">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2480-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-128">-Accountresourceıd</span><span class="sxs-lookup"><span data-stu-id="d2480-128">-AccountResourceId</span></span>
<span data-ttu-id="d2480-129">Depolama hesabının Azure kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d2480-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="d2480-130">-ActiveKeyName</span></span>
<span data-ttu-id="d2480-131">SAS belirteçlerini oluşturmak için kullanılması gereken depolama hesabı anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="d2480-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2480-132">-DefaultProfile</span></span>
<span data-ttu-id="d2480-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d2480-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2480-134">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="d2480-134">-Disable</span></span>
<span data-ttu-id="d2480-135">SAS belirteçlerinin oluşturulması için yönetilen depolama hesabı anahtarının kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d2480-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="d2480-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="d2480-137">Otomatik yeniden üret tuşu.</span><span class="sxs-lookup"><span data-stu-id="d2480-137">Auto regenerate key.</span></span> <span data-ttu-id="d2480-138">Doğruysa, yönetilen depolama hesabının etkin olmayan anahtarı otomatik olarak yeniden oluşturulur ve yeniden oluşturma döneminden sonra yeni etkin anahtar olur.</span><span class="sxs-lookup"><span data-stu-id="d2480-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="d2480-139">Yanlışsa, yönetilen depolama hesabı anahtarları otomatik olarak oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="d2480-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="d2480-140">-RegenerationPeriod</span></span>
<span data-ttu-id="d2480-141">Yeniden oluşturma dönemi.</span><span class="sxs-lookup"><span data-stu-id="d2480-141">Regeneration period.</span></span> <span data-ttu-id="d2480-142">Otomatik yeniden üret anahtarı etkinleştirilirse, bu değer, yönetilen depolama hesabının etkin olmayan anahtar otomatik olarak yeniden üretilmesinden sonraki ve yeni etkin anahtar haline gelir.</span><span class="sxs-lookup"><span data-stu-id="d2480-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d2480-143">-Tag</span></span>
<span data-ttu-id="d2480-144">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d2480-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d2480-145">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="d2480-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d2480-146">-VaultName</span></span>
<span data-ttu-id="d2480-147">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="d2480-147">Vault name.</span></span>
<span data-ttu-id="d2480-148">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2480-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2480-149">-Confirm</span></span>
<span data-ttu-id="d2480-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2480-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2480-151">-WhatIf</span></span>
<span data-ttu-id="d2480-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2480-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2480-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2480-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2480-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2480-154">CommonParameters</span></span>
<span data-ttu-id="d2480-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2480-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2480-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2480-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2480-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2480-157">INPUTS</span></span>

### <span data-ttu-id="d2480-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d2480-158">System.String</span></span>

### <span data-ttu-id="d2480-159">System. Nullable ' 1 [[System. TimeSpan, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="d2480-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d2480-160">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2480-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d2480-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2480-161">OUTPUTS</span></span>

### <span data-ttu-id="d2480-162">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2480-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d2480-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2480-163">NOTES</span></span>

## <span data-ttu-id="d2480-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2480-164">RELATED LINKS</span></span>

[<span data-ttu-id="d2480-165">Az. Keykasa</span><span class="sxs-lookup"><span data-stu-id="d2480-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
