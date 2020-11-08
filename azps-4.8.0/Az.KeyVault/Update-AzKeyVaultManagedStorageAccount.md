---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 72d23725f537df4f3e2244e799437394496bf434
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267180"
---
# <span data-ttu-id="77017-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="77017-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="77017-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77017-102">SYNOPSIS</span></span>
<span data-ttu-id="77017-103">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="77017-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="77017-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77017-104">SYNTAX</span></span>

### <span data-ttu-id="77017-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="77017-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77017-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="77017-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77017-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="77017-107">DESCRIPTION</span></span>
<span data-ttu-id="77017-108">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="77017-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="77017-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77017-109">EXAMPLES</span></span>

### <span data-ttu-id="77017-110">Örnek 1: Anahtar Kasası yönetilen Azure depolama hesabında etkin anahtarı ' anahtar2 ' olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="77017-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="77017-111">Anahtar Kasası yönetilen Azure depolama hesabı etkin anahtarını ' anahtar2 ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="77017-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="77017-112">bu güncelleştirmeden sonra SAS belirteçlerini oluşturmak için ' anahtar2 ' kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="77017-112">'key2' will be used to generate SAS tokens after this update.</span></span>

### <span data-ttu-id="77017-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="77017-113">Example 2</span></span>

<span data-ttu-id="77017-114">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="77017-114">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="77017-115">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="77017-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultManagedStorageAccount -AccountName 'mystorageaccount' -AutoRegenerateKey $false -RegenerationPeriod $regenerationPeriod -VaultName 'myvault'
```

## <span data-ttu-id="77017-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77017-116">PARAMETERS</span></span>

### <span data-ttu-id="77017-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77017-117">-AccountName</span></span>
<span data-ttu-id="77017-118">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="77017-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="77017-119">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77017-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="77017-120">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="77017-120">-ActiveKeyName</span></span>
<span data-ttu-id="77017-121">Etkin anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="77017-121">Active key name.</span></span>
<span data-ttu-id="77017-122">Belirtilmezse, yönetilen depolama hesabının etkin anahtar adının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="77017-122">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77017-123">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="77017-123">-AutoRegenerateKey</span></span>
<span data-ttu-id="77017-124">Otomatik yeniden üret tuşu.</span><span class="sxs-lookup"><span data-stu-id="77017-124">Auto regenerate key.</span></span>
<span data-ttu-id="77017-125">Belirtilmemişse, yönetilen depolama hesabının otomatik yeniden üret anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="77017-125">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77017-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77017-126">-DefaultProfile</span></span>
<span data-ttu-id="77017-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="77017-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77017-128">-Enable</span><span class="sxs-lookup"><span data-stu-id="77017-128">-Enable</span></span>
<span data-ttu-id="77017-129">Varsa, değer doğru ise SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını sunar.</span><span class="sxs-lookup"><span data-stu-id="77017-129">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="77017-130">Değer yanlışsa, SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="77017-130">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="77017-131">Belirtilmezse, depolama hesabının etkin/devre dışı durumundaki mevcut değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="77017-131">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77017-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77017-132">-InputObject</span></span>
<span data-ttu-id="77017-133">ManagedStorageAccount nesnesi.</span><span class="sxs-lookup"><span data-stu-id="77017-133">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="77017-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="77017-134">-PassThru</span></span>
<span data-ttu-id="77017-135">Cmdlet, varsayılan olarak nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="77017-135">Cmdlet does not return object by default.</span></span> <span data-ttu-id="77017-136">Bu anahtar belirtilmişse, yönetilen depolama hesabı nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="77017-136">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="77017-137">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="77017-137">-RegenerationPeriod</span></span>
<span data-ttu-id="77017-138">Yeniden oluşturma dönemi.</span><span class="sxs-lookup"><span data-stu-id="77017-138">Regeneration period.</span></span> <span data-ttu-id="77017-139">Otomatik yeniden üret anahtarı etkinleştirilirse, bu değer, yönetilen depolama hesabının etkin olmayan anahtar otomatik olarak yeniden üretilmesinden sonraki ve etkin anahtar haline gelir.</span><span class="sxs-lookup"><span data-stu-id="77017-139">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="77017-140">Belirtilmezse, yönetilen depolama hesabı anahtarının varolan anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="77017-140">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77017-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="77017-141">-Tag</span></span>
<span data-ttu-id="77017-142">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="77017-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="77017-143">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="77017-143">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77017-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="77017-144">-VaultName</span></span>
<span data-ttu-id="77017-145">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="77017-145">Vault name.</span></span>
<span data-ttu-id="77017-146">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77017-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="77017-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="77017-147">-Confirm</span></span>
<span data-ttu-id="77017-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="77017-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77017-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77017-149">-WhatIf</span></span>
<span data-ttu-id="77017-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="77017-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77017-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="77017-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77017-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77017-152">CommonParameters</span></span>
<span data-ttu-id="77017-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77017-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77017-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="77017-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77017-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77017-155">INPUTS</span></span>

### <span data-ttu-id="77017-156">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="77017-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="77017-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77017-157">OUTPUTS</span></span>

### <span data-ttu-id="77017-158">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="77017-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="77017-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77017-159">NOTES</span></span>

## <span data-ttu-id="77017-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77017-160">RELATED LINKS</span></span>

[<span data-ttu-id="77017-161">Az. Keykasa</span><span class="sxs-lookup"><span data-stu-id="77017-161">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
