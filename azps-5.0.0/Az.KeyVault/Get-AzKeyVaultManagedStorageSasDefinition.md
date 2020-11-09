---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319913"
---
# <span data-ttu-id="fa5a3-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fa5a3-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="fa5a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5a3-103">Anahtar Kasası yönetimli depolama SAS tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="fa5a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa5a3-104">SYNTAX</span></span>

### <span data-ttu-id="fa5a3-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa5a3-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa5a3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa5a3-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa5a3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa5a3-107">DESCRIPTION</span></span>
<span data-ttu-id="fa5a3-108">Tanımın adı belirtilmişse, Anahtar Kasası yönetilen depolama SAS tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="fa5a3-109">Tanım adı belirtilmezse, kasadaki belirtilen anahtar kasası yönetimli depolama hesabıyla ilişkilendirilmiş tüm SAS tanımları listelenir.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="fa5a3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa5a3-110">EXAMPLES</span></span>

### <span data-ttu-id="fa5a3-111">Örnek 1: Tüm Anahtar Kasası yönetilen depolama SAS tanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="fa5a3-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="fa5a3-112">' Mykasası ' Kasası tarafından yönetilen ' mystorageaccount ' Anahtar Kasası yönetimli depolama hesabıyla ilişkilendirilmiş tüm SAS tanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="fa5a3-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="fa5a3-113">Örnek 2: Anahtar Kasası yönetimli depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="fa5a3-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="fa5a3-114">' Mykasa ' Kasası tarafından yönetilen ' mystorageaccount ' Anahtar Kasası yönetimli depolama hesabıyla ilişkili SAS tanımı ' accountsas ' ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="fa5a3-115">Örnek 3: filtreleme kullanarak tüm Anahtar Kasası yönetilen depolama SAS tanımlarını listeleyin</span><span class="sxs-lookup"><span data-stu-id="fa5a3-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="fa5a3-116">"Hesap" ile başlayan ' mykasa ' Kasası tarafından yönetilen ' mystorageaccount ' Anahtar Kasası yönetimli depolama hesabıyla ilişkilendirilmiş tüm SAS tanımlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="fa5a3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa5a3-117">PARAMETERS</span></span>

### <span data-ttu-id="fa5a3-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fa5a3-118">-AccountName</span></span>
<span data-ttu-id="fa5a3-119">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-119">Vault name.</span></span>
<span data-ttu-id="fa5a3-120">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fa5a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5a3-121">-DefaultProfile</span></span>
<span data-ttu-id="fa5a3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fa5a3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa5a3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa5a3-123">-InputObject</span></span>
<span data-ttu-id="fa5a3-124">ManagedStorageAccount nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="fa5a3-125">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="fa5a3-125">-InRemovedState</span></span>
<span data-ttu-id="fa5a3-126">Çıktıda önceden silinmiş depolama SAS tanımlarının gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="fa5a3-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa5a3-127">-Name</span></span>
<span data-ttu-id="fa5a3-128">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-128">Storage sas definition name.</span></span>
<span data-ttu-id="fa5a3-129">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5a3-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fa5a3-130">-VaultName</span></span>
<span data-ttu-id="fa5a3-131">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-131">Vault name.</span></span>
<span data-ttu-id="fa5a3-132">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fa5a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5a3-133">CommonParameters</span></span>
<span data-ttu-id="fa5a3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5a3-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fa5a3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5a3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa5a3-136">INPUTS</span></span>

### <span data-ttu-id="fa5a3-137">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="fa5a3-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="fa5a3-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa5a3-138">OUTPUTS</span></span>

### <span data-ttu-id="fa5a3-139">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstoragesasdefinitionıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="fa5a3-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="fa5a3-140">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fa5a3-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="fa5a3-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fa5a3-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="fa5a3-142">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultmanagedstoragesasdefinitionıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="fa5a3-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="fa5a3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa5a3-143">NOTES</span></span>

## <span data-ttu-id="fa5a3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa5a3-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

