---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 38af48c1f7b5ae8eb4a3be0f5b2fea6fbe452f0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916271"
---
# <span data-ttu-id="87382-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87382-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="87382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87382-102">SYNOPSIS</span></span>
<span data-ttu-id="87382-103">Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87382-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="87382-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87382-104">SYNTAX</span></span>

### <span data-ttu-id="87382-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87382-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87382-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="87382-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87382-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="87382-107">DESCRIPTION</span></span>
<span data-ttu-id="87382-108">Bir Azure Depolama hesabını anahtar kasasına geri ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="87382-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="87382-109">Bu, Azure Depolama hesabını kaldırmaz ancak hesap anahtarlarını Azure Anahtar Kasası tarafından yönetilmeyecek şekilde kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87382-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="87382-110">Tüm ilişkili anahtar kasası yönetimli depolama SAS tanımları da kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="87382-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="87382-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87382-111">EXAMPLES</span></span>

### <span data-ttu-id="87382-112">Örnek 1: Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="87382-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="87382-113">' Mykasasına ' anahtar kasasından ' mystorageaccount ' adlı Azure Depolama hesabını disde</span><span class="sxs-lookup"><span data-stu-id="87382-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="87382-114">' Mystorageaccount ' hesabı kaldırılmayacak.</span><span class="sxs-lookup"><span data-stu-id="87382-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="87382-115">Bu hesapla ilişkili tüm Anahtar Kasası yönetilen depolama SAS tanımları kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="87382-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="87382-116">Örnek 2: Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını Kullanıcı onayı olmadan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="87382-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="87382-117">' Mykasasına ' anahtar kasasından ' mystorageaccount ' adlı Azure Depolama hesabını disde</span><span class="sxs-lookup"><span data-stu-id="87382-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="87382-118">' Mystorageaccount ' hesabı kaldırılmayacak.</span><span class="sxs-lookup"><span data-stu-id="87382-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="87382-119">Bu hesapla ilişkili tüm Anahtar Kasası yönetilen depolama SAS tanımları kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="87382-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="87382-120">Örnek 3: bir Anahtar Kasası yönetilen Azure Depolama hesabını ve yumuşak silme özellikli bir kasadan ilişkili tüm SAS tanımlarını kalıcı olarak silin (temizleyin).</span><span class="sxs-lookup"><span data-stu-id="87382-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="87382-121">Örnekte, bu kasa için yumuşak silmenin etkinleştirildiği varsayılır.</span><span class="sxs-lookup"><span data-stu-id="87382-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="87382-122">Kasadaki bir varlığın kasa özelliklerini veya RecoveryLevel özniteliğini inceleyerek durumun bu olup olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="87382-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="87382-123">Birinci cmdlet, ' mykasa ' anahtar kasasından ' mystorageaccount '</span><span class="sxs-lookup"><span data-stu-id="87382-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="87382-124">' Mystorageaccount ' hesabı kaldırılmayacak.</span><span class="sxs-lookup"><span data-stu-id="87382-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="87382-125">Bu hesapla ilişkili tüm Anahtar Kasası yönetilen depolama SAS tanımları kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="87382-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="87382-126">İkinci cmdlet, depolama hesabının silinmiş ancak kurtarılabilir durumunda olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="87382-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="87382-127">Bu duruma ulaşmak biraz zaman gerektirebilir, lütfen denemeden önce ~ 30s işlemine izin verin.</span><span class="sxs-lookup"><span data-stu-id="87382-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="87382-128">Üçüncü cmdlet depolama hesabını kalıcı olarak kaldırır-kurtarma artık mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="87382-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="87382-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87382-129">PARAMETERS</span></span>

### <span data-ttu-id="87382-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="87382-130">-AccountName</span></span>
<span data-ttu-id="87382-131">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="87382-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="87382-132">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87382-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87382-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87382-133">-DefaultProfile</span></span>
<span data-ttu-id="87382-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="87382-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87382-135">-Force</span><span class="sxs-lookup"><span data-stu-id="87382-135">-Force</span></span>
<span data-ttu-id="87382-136">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="87382-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="87382-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87382-137">-InputObject</span></span>
<span data-ttu-id="87382-138">ManagedStorageAccount nesnesi.</span><span class="sxs-lookup"><span data-stu-id="87382-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87382-139">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="87382-139">-InRemovedState</span></span>
<span data-ttu-id="87382-140">Önceden silinmiş yönetilen depolama hesabını kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="87382-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="87382-141">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="87382-141">-PassThru</span></span>
<span data-ttu-id="87382-142">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="87382-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="87382-143">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="87382-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="87382-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="87382-144">-VaultName</span></span>
<span data-ttu-id="87382-145">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="87382-145">Vault name.</span></span>
<span data-ttu-id="87382-146">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87382-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87382-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="87382-147">-Confirm</span></span>
<span data-ttu-id="87382-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87382-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87382-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87382-149">-WhatIf</span></span>
<span data-ttu-id="87382-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87382-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87382-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87382-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87382-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87382-152">CommonParameters</span></span>
<span data-ttu-id="87382-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87382-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87382-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87382-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87382-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87382-155">INPUTS</span></span>

### <span data-ttu-id="87382-156">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="87382-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="87382-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87382-157">OUTPUTS</span></span>

### <span data-ttu-id="87382-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87382-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="87382-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87382-159">NOTES</span></span>

## <span data-ttu-id="87382-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87382-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
