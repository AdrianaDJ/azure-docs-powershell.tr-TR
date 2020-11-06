---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 2e096b04830d50840d6298e7aa8085b0090a347e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593241"
---
# <span data-ttu-id="8b08b-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8b08b-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="8b08b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b08b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b08b-103">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b08b-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b08b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b08b-104">SYNTAX</span></span>

### <span data-ttu-id="8b08b-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b08b-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b08b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b08b-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b08b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b08b-107">DESCRIPTION</span></span>
<span data-ttu-id="8b08b-108">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur ve anahtarı etkin anahtar olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8b08b-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="8b08b-109">Anahtar Kasası proxy 'leri anahtarı yeniden oluşturmak için Azure Resource Manager 'a çağrı.</span><span class="sxs-lookup"><span data-stu-id="8b08b-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="8b08b-110">Arayan, verilen Azure depolama hesabında anahtarları yeniden oluşturmak için izinleri karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b08b-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="8b08b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b08b-111">EXAMPLES</span></span>

### <span data-ttu-id="8b08b-112">Örnek 1: anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b08b-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

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

<span data-ttu-id="8b08b-113">' Mystorageaccount ' hesabının ' anahtar ' hesabını yeniden oluşturur ve ' anahtar ' değerini Anahtar Kasası yönetilen Azure depolama hesabı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8b08b-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="8b08b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b08b-114">PARAMETERS</span></span>

### <span data-ttu-id="8b08b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b08b-115">-AccountName</span></span>
<span data-ttu-id="8b08b-116">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="8b08b-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="8b08b-117">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b08b-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="8b08b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b08b-118">-DefaultProfile</span></span>
<span data-ttu-id="8b08b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8b08b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b08b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8b08b-120">-Force</span></span>
<span data-ttu-id="8b08b-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="8b08b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8b08b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b08b-122">-InputObject</span></span>
<span data-ttu-id="8b08b-123">ManagedStorageAccount nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8b08b-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="8b08b-124">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="8b08b-124">-KeyName</span></span>
<span data-ttu-id="8b08b-125">Yeniden oluşturmak ve etkinleştirmek için depolama hesabı anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="8b08b-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b08b-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8b08b-126">-PassThru</span></span>
<span data-ttu-id="8b08b-127">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="8b08b-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8b08b-128">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b08b-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="8b08b-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8b08b-129">-VaultName</span></span>
<span data-ttu-id="8b08b-130">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="8b08b-130">Vault name.</span></span>
<span data-ttu-id="8b08b-131">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b08b-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8b08b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b08b-132">-Confirm</span></span>
<span data-ttu-id="8b08b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b08b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b08b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b08b-134">-WhatIf</span></span>
<span data-ttu-id="8b08b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b08b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b08b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b08b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b08b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b08b-137">CommonParameters</span></span>
<span data-ttu-id="8b08b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b08b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b08b-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b08b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b08b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b08b-140">INPUTS</span></span>

### <span data-ttu-id="8b08b-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="8b08b-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="8b08b-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b08b-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8b08b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b08b-143">OUTPUTS</span></span>

### <span data-ttu-id="8b08b-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b08b-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8b08b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b08b-145">NOTES</span></span>

## <span data-ttu-id="8b08b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b08b-146">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

