---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ea3d16ec55186017852df30f6ff745f79703f224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936641"
---
# <span data-ttu-id="e68b4-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e68b4-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e68b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e68b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e68b4-103">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e68b4-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e68b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e68b4-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e68b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e68b4-105">DESCRIPTION</span></span>
<span data-ttu-id="e68b4-106">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e68b4-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e68b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e68b4-107">EXAMPLES</span></span>

### <span data-ttu-id="e68b4-108">Örnek 1: Anahtar Kasası yönetilen Azure depolama hesabında etkin anahtarı ' anahtar2 ' olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e68b4-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="e68b4-109">Anahtar Kasası yönetilen Azure depolama hesabı etkin anahtarını ' anahtar2 ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e68b4-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="e68b4-110">bu güncelleştirmeden sonra SAS belirteçlerini oluşturmak için ' anahtar2 ' kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="e68b4-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="e68b4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e68b4-111">PARAMETERS</span></span>

### <span data-ttu-id="e68b4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e68b4-112">-AccountName</span></span>
<span data-ttu-id="e68b4-113">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="e68b4-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="e68b4-114">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e68b4-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="e68b4-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="e68b4-115">-ActiveKeyName</span></span>
<span data-ttu-id="e68b4-116">Etkin anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="e68b4-116">Active key name.</span></span>
<span data-ttu-id="e68b4-117">Belirtilmezse, yönetilen depolama hesabının etkin anahtar adının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="e68b4-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68b4-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="e68b4-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="e68b4-119">Otomatik yeniden üret tuşu.</span><span class="sxs-lookup"><span data-stu-id="e68b4-119">Auto regenerate key.</span></span>
<span data-ttu-id="e68b4-120">Belirtilmemişse, yönetilen depolama hesabının otomatik yeniden üret anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="e68b4-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68b4-121">-DefaultProfile</span></span>
<span data-ttu-id="e68b4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e68b4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e68b4-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="e68b4-123">-Enable</span></span>
<span data-ttu-id="e68b4-124">Varsa, değer doğru ise SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını sunar.</span><span class="sxs-lookup"><span data-stu-id="e68b4-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="e68b4-125">Değer yanlışsa, SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e68b4-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="e68b4-126">Belirtilmezse, depolama hesabının etkin/devre dışı durumundaki mevcut değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="e68b4-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68b4-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e68b4-127">-PassThru</span></span>
<span data-ttu-id="e68b4-128">Cmdlet, varsayılan olarak nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="e68b4-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="e68b4-129">Bu anahtar belirtilmişse, yönetilen depolama hesabı nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e68b4-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="e68b4-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="e68b4-130">-RegenerationPeriod</span></span>
<span data-ttu-id="e68b4-131">Yeniden oluşturma dönemi.</span><span class="sxs-lookup"><span data-stu-id="e68b4-131">Regeneration period.</span></span> <span data-ttu-id="e68b4-132">Otomatik yeniden üret anahtarı etkinleştirilirse, bu değer, yönetilen depolama hesabının etkin olmayan anahtar otomatik olarak yeniden üretilmesinden sonraki ve etkin anahtar haline gelir.</span><span class="sxs-lookup"><span data-stu-id="e68b4-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="e68b4-133">Belirtilmezse, yönetilen depolama hesabı anahtarının varolan anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="e68b4-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="e68b4-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e68b4-134">-Tag</span></span>
<span data-ttu-id="e68b4-135">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e68b4-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e68b4-136">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="e68b4-136">For example:</span></span>

<span data-ttu-id="e68b4-137">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e68b4-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e68b4-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e68b4-138">-VaultName</span></span>
<span data-ttu-id="e68b4-139">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="e68b4-139">Vault name.</span></span>
<span data-ttu-id="e68b4-140">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e68b4-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e68b4-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="e68b4-141">-Confirm</span></span>
<span data-ttu-id="e68b4-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e68b4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e68b4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e68b4-143">-WhatIf</span></span>
<span data-ttu-id="e68b4-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e68b4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e68b4-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e68b4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e68b4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68b4-146">CommonParameters</span></span>
<span data-ttu-id="e68b4-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e68b4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68b4-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e68b4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68b4-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e68b4-149">INPUTS</span></span>

### <span data-ttu-id="e68b4-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e68b4-150">None</span></span>
<span data-ttu-id="e68b4-151">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e68b4-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e68b4-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e68b4-152">OUTPUTS</span></span>

### <span data-ttu-id="e68b4-153">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e68b4-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="e68b4-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e68b4-154">NOTES</span></span>

## <span data-ttu-id="e68b4-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e68b4-155">RELATED LINKS</span></span>

[<span data-ttu-id="e68b4-156">Az. Keykasa</span><span class="sxs-lookup"><span data-stu-id="e68b4-156">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
