---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 84c6df195b0d24e5096748a4a5e3fd8360665831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587905"
---
# <span data-ttu-id="54372-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54372-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="54372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54372-102">SYNOPSIS</span></span>
<span data-ttu-id="54372-103">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="54372-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54372-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54372-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54372-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54372-105">DESCRIPTION</span></span>
<span data-ttu-id="54372-106">Anahtar Kasası yönetilen Azure depolama hesabının düzenlenebilir özniteliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="54372-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="54372-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54372-107">EXAMPLES</span></span>

### <span data-ttu-id="54372-108">Örnek 1: Anahtar Kasası yönetilen Azure depolama hesabında etkin anahtarı ' anahtar2 ' olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="54372-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="54372-109">Anahtar Kasası yönetilen Azure depolama hesabı etkin anahtarını ' anahtar2 ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="54372-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="54372-110">bu güncelleştirmeden sonra SAS belirteçlerini oluşturmak için ' anahtar2 ' kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="54372-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="54372-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54372-111">PARAMETERS</span></span>

### <span data-ttu-id="54372-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54372-112">-AccountName</span></span>
<span data-ttu-id="54372-113">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="54372-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="54372-114">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54372-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="54372-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="54372-115">-ActiveKeyName</span></span>
<span data-ttu-id="54372-116">Etkin anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="54372-116">Active key name.</span></span>
<span data-ttu-id="54372-117">Belirtilmezse, yönetilen depolama hesabının etkin anahtar adının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="54372-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54372-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="54372-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="54372-119">Otomatik yeniden üret tuşu.</span><span class="sxs-lookup"><span data-stu-id="54372-119">Auto regenerate key.</span></span>
<span data-ttu-id="54372-120">Belirtilmemişse, yönetilen depolama hesabının otomatik yeniden üret anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="54372-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54372-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="54372-121">-Confirm</span></span>
<span data-ttu-id="54372-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54372-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54372-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="54372-123">-Enable</span></span>
<span data-ttu-id="54372-124">Varsa, değer doğru ise SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını sunar.</span><span class="sxs-lookup"><span data-stu-id="54372-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="54372-125">Değer yanlışsa, SAS belirteç üretimi için yönetilen depolama hesabı anahtarının kullanımını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="54372-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="54372-126">Belirtilmezse, depolama hesabının etkin/devre dışı durumundaki mevcut değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="54372-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="54372-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="54372-127">-PassThru</span></span>
<span data-ttu-id="54372-128">Cmdlet, varsayılan olarak nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="54372-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="54372-129">Bu anahtar belirtilmişse, yönetilen depolama hesabı nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="54372-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="54372-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="54372-130">-RegenerationPeriod</span></span>
<span data-ttu-id="54372-131">Yeniden oluşturma dönemi.</span><span class="sxs-lookup"><span data-stu-id="54372-131">Regeneration period.</span></span> <span data-ttu-id="54372-132">Otomatik yeniden üret anahtarı etkinleştirilirse, bu değer, yönetilen depolama hesabının etkin olmayan anahtar otomatik olarak yeniden üretilmesinden sonraki ve etkin anahtar haline gelir.</span><span class="sxs-lookup"><span data-stu-id="54372-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="54372-133">Belirtilmezse, yönetilen depolama hesabı anahtarının varolan anahtarının mevcut değeri değişmeden kalır</span><span class="sxs-lookup"><span data-stu-id="54372-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="54372-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="54372-134">-Tag</span></span>
<span data-ttu-id="54372-135">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="54372-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="54372-136">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="54372-136">For example:</span></span>

<span data-ttu-id="54372-137">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="54372-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="54372-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54372-138">-VaultName</span></span>
<span data-ttu-id="54372-139">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="54372-139">Vault name.</span></span>
<span data-ttu-id="54372-140">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54372-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="54372-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54372-141">-WhatIf</span></span>
<span data-ttu-id="54372-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54372-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54372-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54372-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54372-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54372-144">-DefaultProfile</span></span>
<span data-ttu-id="54372-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54372-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54372-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54372-146">CommonParameters</span></span>
<span data-ttu-id="54372-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54372-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54372-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54372-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54372-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54372-149">INPUTS</span></span>

## <span data-ttu-id="54372-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54372-150">OUTPUTS</span></span>

### <span data-ttu-id="54372-151">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54372-151">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="54372-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54372-152">NOTES</span></span>

## <span data-ttu-id="54372-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54372-153">RELATED LINKS</span></span>

[<span data-ttu-id="54372-154">AzureRM. Keykasası</span><span class="sxs-lookup"><span data-stu-id="54372-154">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
