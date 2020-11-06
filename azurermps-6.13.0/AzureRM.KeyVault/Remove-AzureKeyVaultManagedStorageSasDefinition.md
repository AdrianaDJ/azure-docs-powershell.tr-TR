---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a5176dea9ca1cff125d615e4f2d8cd5447ea28e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590231"
---
# <span data-ttu-id="8b692-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8b692-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8b692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b692-102">SYNOPSIS</span></span>
<span data-ttu-id="8b692-103">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b692-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b692-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b692-104">SYNTAX</span></span>

### <span data-ttu-id="8b692-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b692-105">ByDefinitionName (Default)</span></span>
```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b692-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b692-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultManagedStorageSasDefinition
 [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b692-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b692-107">DESCRIPTION</span></span>
<span data-ttu-id="8b692-108">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b692-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="8b692-109">Bu, SAS belirtecini bu SAS tanımına almak için kullanılan parolayı da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b692-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="8b692-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b692-110">EXAMPLES</span></span>

### <span data-ttu-id="8b692-111">Örnek 1: Anahtar Kasası yönetimli Azure depolama SAS tanımını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="8b692-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="8b692-112">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b692-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="8b692-113">Örnek 2: Kullanıcı onayı olmadan bir Anahtar Kasası yönetilen Azure depolama SAS tanımını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="8b692-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="8b692-114">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b692-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="8b692-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b692-115">PARAMETERS</span></span>

### <span data-ttu-id="8b692-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b692-116">-AccountName</span></span>
<span data-ttu-id="8b692-117">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="8b692-117">Storage account name.</span></span>
<span data-ttu-id="8b692-118">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve depolama hesabı adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b692-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b692-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b692-119">-DefaultProfile</span></span>
<span data-ttu-id="8b692-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8b692-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b692-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8b692-121">-Force</span></span>
<span data-ttu-id="8b692-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="8b692-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8b692-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b692-123">-InputObject</span></span>
<span data-ttu-id="8b692-124">ManagedStorageSasDefinition nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8b692-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b692-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b692-125">-Name</span></span>
<span data-ttu-id="8b692-126">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="8b692-126">Storage sas definition name.</span></span>
<span data-ttu-id="8b692-127">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b692-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b692-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8b692-128">-PassThru</span></span>
<span data-ttu-id="8b692-129">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="8b692-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8b692-130">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b692-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="8b692-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8b692-131">-VaultName</span></span>
<span data-ttu-id="8b692-132">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="8b692-132">Vault name.</span></span>
<span data-ttu-id="8b692-133">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b692-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8b692-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b692-134">-Confirm</span></span>
<span data-ttu-id="8b692-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b692-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b692-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b692-136">-WhatIf</span></span>
<span data-ttu-id="8b692-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b692-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b692-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b692-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b692-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b692-139">CommonParameters</span></span>
<span data-ttu-id="8b692-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b692-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b692-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b692-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b692-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b692-142">INPUTS</span></span>

### <span data-ttu-id="8b692-143">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstoragesasdefinitionıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="8b692-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>
<span data-ttu-id="8b692-144">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b692-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8b692-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b692-145">OUTPUTS</span></span>

### <span data-ttu-id="8b692-146">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8b692-146">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8b692-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b692-147">NOTES</span></span>

## <span data-ttu-id="8b692-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b692-148">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

