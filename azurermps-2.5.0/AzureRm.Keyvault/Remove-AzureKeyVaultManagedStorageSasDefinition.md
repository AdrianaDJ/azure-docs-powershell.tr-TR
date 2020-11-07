---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 61c58d4dae5d990a72ca81e7016a3e312e82229a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938829"
---
# <span data-ttu-id="c1ebd-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="c1ebd-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="c1ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ebd-103">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ebd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1ebd-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1ebd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ebd-106">Anahtar Kasası yönetimli Azure depolama SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="c1ebd-107">Bu, SAS belirtecini bu SAS tanımına almak için kullanılan parolayı da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="c1ebd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1ebd-108">EXAMPLES</span></span>

### <span data-ttu-id="c1ebd-109">Örnek 1: Anahtar Kasası yönetimli Azure depolama SAS tanımını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="c1ebd-110">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="c1ebd-111">Örnek 2: Kullanıcı onayı olmadan bir Anahtar Kasası yönetilen Azure depolama SAS tanımını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="c1ebd-112">' Mykasası ' kasasındaki ' mystorageaccount ' hesabıyla ilişkilendirilmiş bir Anahtar Kasası yönetilen depolama alanı SAS tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="c1ebd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1ebd-113">PARAMETERS</span></span>

### <span data-ttu-id="c1ebd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1ebd-114">-AccountName</span></span>
<span data-ttu-id="c1ebd-115">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-115">Storage account name.</span></span>
<span data-ttu-id="c1ebd-116">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve depolama hesabı adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="c1ebd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ebd-117">-DefaultProfile</span></span>
<span data-ttu-id="c1ebd-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c1ebd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ebd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c1ebd-119">-Force</span></span>
<span data-ttu-id="c1ebd-120">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c1ebd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1ebd-121">-Name</span></span>
<span data-ttu-id="c1ebd-122">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-122">Storage sas definition name.</span></span>
<span data-ttu-id="c1ebd-123">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="c1ebd-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c1ebd-124">-PassThru</span></span>
<span data-ttu-id="c1ebd-125">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c1ebd-126">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="c1ebd-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c1ebd-127">-VaultName</span></span>
<span data-ttu-id="c1ebd-128">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-128">Vault name.</span></span>
<span data-ttu-id="c1ebd-129">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c1ebd-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1ebd-130">-Confirm</span></span>
<span data-ttu-id="c1ebd-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1ebd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ebd-132">-WhatIf</span></span>
<span data-ttu-id="c1ebd-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1ebd-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1ebd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ebd-135">CommonParameters</span></span>
<span data-ttu-id="c1ebd-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1ebd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ebd-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ebd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ebd-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1ebd-138">INPUTS</span></span>

### <span data-ttu-id="c1ebd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c1ebd-139">System.String</span></span>

## <span data-ttu-id="c1ebd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1ebd-140">OUTPUTS</span></span>

### <span data-ttu-id="c1ebd-141">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="c1ebd-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="c1ebd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1ebd-142">NOTES</span></span>

## <span data-ttu-id="c1ebd-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1ebd-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

