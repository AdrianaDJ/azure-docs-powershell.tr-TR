---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 98c4cca6b2de508ca48da4ccbc5cf9f9a31eaa0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935772"
---
# <span data-ttu-id="f37d4-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f37d4-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f37d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f37d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f37d4-103">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f37d4-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="f37d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f37d4-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f37d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f37d4-105">DESCRIPTION</span></span>
<span data-ttu-id="f37d4-106">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f37d4-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="f37d4-107">Bu, SAS belirtecini bu SAS tanımına almak için kullanılan parolayı da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f37d4-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="f37d4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f37d4-108">EXAMPLES</span></span>

### <span data-ttu-id="f37d4-109">Örnek 1: Anahtar Kasası yönetimli Azure depolama SAS tanımını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="f37d4-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="f37d4-110">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f37d4-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="f37d4-111">Örnek 2: Kullanıcı onayı olmadan bir Anahtar Kasası yönetilen Azure depolama SAS tanımını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="f37d4-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="f37d4-112">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f37d4-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="f37d4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f37d4-113">PARAMETERS</span></span>

### <span data-ttu-id="f37d4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f37d4-114">-AccountName</span></span>
<span data-ttu-id="f37d4-115">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f37d4-115">Storage account name.</span></span>
<span data-ttu-id="f37d4-116">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve depolama hesabı adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f37d4-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f37d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37d4-117">-DefaultProfile</span></span>
<span data-ttu-id="f37d4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f37d4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f37d4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f37d4-119">-Force</span></span>
<span data-ttu-id="f37d4-120">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="f37d4-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f37d4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="f37d4-121">-Name</span></span>
<span data-ttu-id="f37d4-122">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="f37d4-122">Storage sas definition name.</span></span>
<span data-ttu-id="f37d4-123">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f37d4-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f37d4-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f37d4-124">-PassThru</span></span>
<span data-ttu-id="f37d4-125">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="f37d4-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f37d4-126">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f37d4-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="f37d4-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f37d4-127">-VaultName</span></span>
<span data-ttu-id="f37d4-128">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="f37d4-128">Vault name.</span></span>
<span data-ttu-id="f37d4-129">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f37d4-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f37d4-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="f37d4-130">-Confirm</span></span>
<span data-ttu-id="f37d4-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f37d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f37d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f37d4-132">-WhatIf</span></span>
<span data-ttu-id="f37d4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f37d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f37d4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f37d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f37d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37d4-135">CommonParameters</span></span>
<span data-ttu-id="f37d4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f37d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37d4-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f37d4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37d4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f37d4-138">INPUTS</span></span>

### <span data-ttu-id="f37d4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f37d4-139">System.String</span></span>

## <span data-ttu-id="f37d4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f37d4-140">OUTPUTS</span></span>

### <span data-ttu-id="f37d4-141">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f37d4-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f37d4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f37d4-142">NOTES</span></span>

## <span data-ttu-id="f37d4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f37d4-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

