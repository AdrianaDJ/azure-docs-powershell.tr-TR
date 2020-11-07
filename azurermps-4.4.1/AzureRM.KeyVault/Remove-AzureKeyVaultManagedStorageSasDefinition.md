---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: fadf6b15eb25f07d88254a5d3a998f1692e5cf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764054"
---
# <span data-ttu-id="591df-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="591df-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="591df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591df-102">SYNOPSIS</span></span>
<span data-ttu-id="591df-103">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="591df-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="591df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="591df-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="591df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="591df-105">DESCRIPTION</span></span>
<span data-ttu-id="591df-106">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="591df-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="591df-107">Bu, SAS belirtecini bu SAS tanımına almak için kullanılan parolayı da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="591df-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="591df-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="591df-108">EXAMPLES</span></span>

### <span data-ttu-id="591df-109">Örnek 1: Anahtar Kasası yönetimli Azure depolama SAS tanımını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="591df-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="591df-110">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="591df-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="591df-111">Örnek 2: Kullanıcı onayı olmadan bir Anahtar Kasası yönetilen Azure depolama SAS tanımını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="591df-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="591df-112">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="591df-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="591df-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="591df-113">PARAMETERS</span></span>

### <span data-ttu-id="591df-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="591df-114">-AccountName</span></span>
<span data-ttu-id="591df-115">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="591df-115">Storage account name.</span></span>
<span data-ttu-id="591df-116">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve depolama hesabı adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="591df-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591df-117">-Force</span><span class="sxs-lookup"><span data-stu-id="591df-117">-Force</span></span>
<span data-ttu-id="591df-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="591df-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="591df-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="591df-119">-Name</span></span>
<span data-ttu-id="591df-120">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="591df-120">Storage sas definition name.</span></span>
<span data-ttu-id="591df-121">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="591df-121">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591df-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="591df-122">-PassThru</span></span>
<span data-ttu-id="591df-123">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="591df-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="591df-124">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="591df-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="591df-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="591df-125">-VaultName</span></span>
<span data-ttu-id="591df-126">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="591df-126">Vault name.</span></span>
<span data-ttu-id="591df-127">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="591df-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="591df-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="591df-128">-Confirm</span></span>
<span data-ttu-id="591df-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="591df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591df-130">-WhatIf</span></span>
<span data-ttu-id="591df-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="591df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591df-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="591df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591df-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591df-133">-DefaultProfile</span></span>
<span data-ttu-id="591df-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="591df-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="591df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591df-135">CommonParameters</span></span>
<span data-ttu-id="591df-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="591df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591df-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591df-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="591df-138">INPUTS</span></span>

### <span data-ttu-id="591df-139">System. String</span><span class="sxs-lookup"><span data-stu-id="591df-139">System.String</span></span>

## <span data-ttu-id="591df-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="591df-140">OUTPUTS</span></span>

### <span data-ttu-id="591df-141">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="591df-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="591df-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="591df-142">NOTES</span></span>

## <span data-ttu-id="591df-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="591df-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

