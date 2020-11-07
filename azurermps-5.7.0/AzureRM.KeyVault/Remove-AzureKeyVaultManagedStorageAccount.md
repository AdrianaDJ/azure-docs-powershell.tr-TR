---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c422975af622fe54602224b0c311ea8e738f838f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762521"
---
# <span data-ttu-id="b01b8-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b01b8-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="b01b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b01b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b01b8-103">Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b01b8-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b01b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b01b8-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b01b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b01b8-105">DESCRIPTION</span></span>
<span data-ttu-id="b01b8-106">Bir Azure Depolama hesabını anahtar kasasına geri ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="b01b8-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="b01b8-107">Bu, Azure Depolama hesabını kaldırmaz ancak hesap anahtarlarını Azure Anahtar Kasası tarafından yönetilmeyecek şekilde kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b01b8-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="b01b8-108">Tüm ilişkili anahtar kasası yönetimli depolama SAS tanımları da kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="b01b8-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="b01b8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b01b8-109">EXAMPLES</span></span>

### <span data-ttu-id="b01b8-110">Örnek 1: Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b01b8-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="b01b8-111">' Mykasasına ' anahtar kasasından ' mystorageaccount ' adlı Azure Depolama hesabını disde</span><span class="sxs-lookup"><span data-stu-id="b01b8-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="b01b8-112">' Mystorageaccount ' hesabı kaldırılmayacak.</span><span class="sxs-lookup"><span data-stu-id="b01b8-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="b01b8-113">Bu hesapla ilişkili tüm Anahtar Kasası yönetilen depolama SAS tanımları kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b01b8-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="b01b8-114">Örnek 2: Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını Kullanıcı onayı olmadan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b01b8-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="b01b8-115">' Mykasasına ' anahtar kasasından ' mystorageaccount ' adlı Azure Depolama hesabını disde</span><span class="sxs-lookup"><span data-stu-id="b01b8-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="b01b8-116">' Mystorageaccount ' hesabı kaldırılmayacak.</span><span class="sxs-lookup"><span data-stu-id="b01b8-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="b01b8-117">Bu hesapla ilişkili tüm Anahtar Kasası yönetilen depolama SAS tanımları kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b01b8-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="b01b8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b01b8-118">PARAMETERS</span></span>

### <span data-ttu-id="b01b8-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b01b8-119">-AccountName</span></span>
<span data-ttu-id="b01b8-120">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b01b8-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="b01b8-121">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b01b8-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="b01b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01b8-122">-DefaultProfile</span></span>
<span data-ttu-id="b01b8-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b01b8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b01b8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b01b8-124">-Force</span></span>
<span data-ttu-id="b01b8-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="b01b8-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b01b8-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b01b8-126">-PassThru</span></span>
<span data-ttu-id="b01b8-127">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b01b8-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b01b8-128">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b01b8-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="b01b8-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b01b8-129">-VaultName</span></span>
<span data-ttu-id="b01b8-130">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="b01b8-130">Vault name.</span></span>
<span data-ttu-id="b01b8-131">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b01b8-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b01b8-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="b01b8-132">-Confirm</span></span>
<span data-ttu-id="b01b8-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b01b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b01b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b01b8-134">-WhatIf</span></span>
<span data-ttu-id="b01b8-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b01b8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b01b8-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b01b8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b01b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01b8-137">CommonParameters</span></span>
<span data-ttu-id="b01b8-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b01b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01b8-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b01b8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01b8-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b01b8-140">INPUTS</span></span>

### <span data-ttu-id="b01b8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b01b8-141">System.String</span></span>

## <span data-ttu-id="b01b8-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b01b8-142">OUTPUTS</span></span>

### <span data-ttu-id="b01b8-143">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b01b8-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="b01b8-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b01b8-144">NOTES</span></span>

## <span data-ttu-id="b01b8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b01b8-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

