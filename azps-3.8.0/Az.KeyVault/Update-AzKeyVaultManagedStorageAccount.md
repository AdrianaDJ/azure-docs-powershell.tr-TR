---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: bb1bab4c80b3dff8bfdbede32b1775321cc2ebd5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096625"
---
# <span data-ttu-id="70eca-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70eca-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="70eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70eca-102">SYNOPSIS</span></span>
<span data-ttu-id="70eca-103">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="70eca-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="70eca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70eca-104">SYNTAX</span></span>

### <span data-ttu-id="70eca-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="70eca-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70eca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="70eca-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70eca-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="70eca-107">DESCRIPTION</span></span>
<span data-ttu-id="70eca-108">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="70eca-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="70eca-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70eca-109">EXAMPLES</span></span>

### <span data-ttu-id="70eca-110">Örnek 1: Anahtar Kasası yönetilen Azure depolama hesabında etkin anahtarı ' anahtar2 ' olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="70eca-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
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

<span data-ttu-id="70eca-111">Anahtar Kasası yönetilen Azure depolama hesabı etkin anahtarını ' anahtar2 ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="70eca-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="70eca-112">bu güncelleştirmeden sonra SAS belirteçlerini oluşturmak için ' anahtar2 ' kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="70eca-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="70eca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70eca-113">PARAMETERS</span></span>

### <span data-ttu-id="70eca-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70eca-114">-AccountName</span></span>
<span data-ttu-id="70eca-115">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="70eca-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="70eca-116">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70eca-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="70eca-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="70eca-117">-ActiveKeyName</span></span>
<span data-ttu-id="70eca-118">Etkin anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="70eca-118">Active key name.</span></span>
<span data-ttu-id="70eca-119">Belirtilmezse, yönetilen depolama hesabının etkin anahtar adının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="70eca-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="70eca-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="70eca-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="70eca-121">Otomatik yeniden üret tuşu.</span><span class="sxs-lookup"><span data-stu-id="70eca-121">Auto regenerate key.</span></span>
<span data-ttu-id="70eca-122">Belirtilmemişse, yönetilen depolama hesabının otomatik yeniden üret anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="70eca-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="70eca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70eca-123">-DefaultProfile</span></span>
<span data-ttu-id="70eca-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="70eca-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70eca-125">-Enable</span><span class="sxs-lookup"><span data-stu-id="70eca-125">-Enable</span></span>
<span data-ttu-id="70eca-126">Varsa, değer doğru ise SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını sunar.</span><span class="sxs-lookup"><span data-stu-id="70eca-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="70eca-127">Değer yanlışsa, SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="70eca-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="70eca-128">Belirtilmezse, depolama hesabının etkin/devre dışı durumundaki mevcut değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="70eca-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="70eca-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70eca-129">-InputObject</span></span>
<span data-ttu-id="70eca-130">ManagedStorageAccount nesnesi.</span><span class="sxs-lookup"><span data-stu-id="70eca-130">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="70eca-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="70eca-131">-PassThru</span></span>
<span data-ttu-id="70eca-132">Cmdlet, varsayılan olarak nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="70eca-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="70eca-133">Bu anahtar belirtilmişse, yönetilen depolama hesabı nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="70eca-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="70eca-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="70eca-134">-RegenerationPeriod</span></span>
<span data-ttu-id="70eca-135">Yeniden oluşturma dönemi.</span><span class="sxs-lookup"><span data-stu-id="70eca-135">Regeneration period.</span></span> <span data-ttu-id="70eca-136">Otomatik yeniden üret anahtarı etkinleştirilirse, bu değer, yönetilen depolama hesabının etkin olmayan anahtar otomatik olarak yeniden üretilmesinden sonraki ve etkin anahtar haline gelir.</span><span class="sxs-lookup"><span data-stu-id="70eca-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="70eca-137">Belirtilmezse, yönetilen depolama hesabı anahtarının varolan anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="70eca-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="70eca-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="70eca-138">-Tag</span></span>
<span data-ttu-id="70eca-139">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="70eca-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="70eca-140">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="70eca-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="70eca-141">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70eca-141">-VaultName</span></span>
<span data-ttu-id="70eca-142">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="70eca-142">Vault name.</span></span>
<span data-ttu-id="70eca-143">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70eca-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="70eca-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="70eca-144">-Confirm</span></span>
<span data-ttu-id="70eca-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70eca-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70eca-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70eca-146">-WhatIf</span></span>
<span data-ttu-id="70eca-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70eca-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70eca-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70eca-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70eca-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70eca-149">CommonParameters</span></span>
<span data-ttu-id="70eca-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70eca-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70eca-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="70eca-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70eca-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70eca-152">INPUTS</span></span>

### <span data-ttu-id="70eca-153">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="70eca-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="70eca-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70eca-154">OUTPUTS</span></span>

### <span data-ttu-id="70eca-155">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70eca-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="70eca-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70eca-156">NOTES</span></span>

## <span data-ttu-id="70eca-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70eca-157">RELATED LINKS</span></span>

[<span data-ttu-id="70eca-158">Az. Keykasa</span><span class="sxs-lookup"><span data-stu-id="70eca-158">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
