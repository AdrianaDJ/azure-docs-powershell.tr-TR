---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109038"
---
# <span data-ttu-id="469c5-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="469c5-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="469c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="469c5-102">SYNOPSIS</span></span>
<span data-ttu-id="469c5-103">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="469c5-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="469c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="469c5-104">SYNTAX</span></span>

### <span data-ttu-id="469c5-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="469c5-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="469c5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="469c5-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="469c5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="469c5-107">DESCRIPTION</span></span>
<span data-ttu-id="469c5-108">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="469c5-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="469c5-109">Bu, SAS belirtecini bu SAS tanımına almak için kullanılan parolayı da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="469c5-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="469c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="469c5-110">EXAMPLES</span></span>

### <span data-ttu-id="469c5-111">Örnek 1: Anahtar Kasası yönetimli Azure depolama SAS tanımını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="469c5-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="469c5-112">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="469c5-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="469c5-113">Örnek 2: Kullanıcı onayı olmadan bir Anahtar Kasası yönetilen Azure depolama SAS tanımını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="469c5-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="469c5-114">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="469c5-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="469c5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="469c5-115">PARAMETERS</span></span>

### <span data-ttu-id="469c5-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="469c5-116">-AccountName</span></span>
<span data-ttu-id="469c5-117">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="469c5-117">Storage account name.</span></span>
<span data-ttu-id="469c5-118">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve depolama hesabı adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="469c5-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="469c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469c5-119">-DefaultProfile</span></span>
<span data-ttu-id="469c5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="469c5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="469c5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="469c5-121">-Force</span></span>
<span data-ttu-id="469c5-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="469c5-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="469c5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="469c5-123">-InputObject</span></span>
<span data-ttu-id="469c5-124">ManagedStorageSasDefinition nesnesi.</span><span class="sxs-lookup"><span data-stu-id="469c5-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="469c5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="469c5-125">-Name</span></span>
<span data-ttu-id="469c5-126">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="469c5-126">Storage sas definition name.</span></span>
<span data-ttu-id="469c5-127">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="469c5-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="469c5-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="469c5-128">-PassThru</span></span>
<span data-ttu-id="469c5-129">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="469c5-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="469c5-130">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="469c5-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="469c5-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="469c5-131">-VaultName</span></span>
<span data-ttu-id="469c5-132">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="469c5-132">Vault name.</span></span>
<span data-ttu-id="469c5-133">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="469c5-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="469c5-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="469c5-134">-Confirm</span></span>
<span data-ttu-id="469c5-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="469c5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="469c5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="469c5-136">-WhatIf</span></span>
<span data-ttu-id="469c5-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="469c5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="469c5-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="469c5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="469c5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469c5-139">CommonParameters</span></span>
<span data-ttu-id="469c5-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="469c5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469c5-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="469c5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469c5-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="469c5-142">INPUTS</span></span>

### <span data-ttu-id="469c5-143">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstoragesasdefinitionıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="469c5-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="469c5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="469c5-144">OUTPUTS</span></span>

### <span data-ttu-id="469c5-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="469c5-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="469c5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="469c5-146">NOTES</span></span>

## <span data-ttu-id="469c5-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="469c5-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

