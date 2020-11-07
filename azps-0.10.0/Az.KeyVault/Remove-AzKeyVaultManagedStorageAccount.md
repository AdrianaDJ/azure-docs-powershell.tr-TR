---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: d57f672ef440515e69535503f006e08b4c924646
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935773"
---
# <span data-ttu-id="20f4a-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20f4a-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="20f4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="20f4a-103">Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20f4a-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="20f4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20f4a-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="20f4a-106">Bir Azure Depolama hesabını anahtar kasasına geri ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="20f4a-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="20f4a-107">Bu, Azure Depolama hesabını kaldırmaz ancak hesap anahtarlarını Azure Anahtar Kasası tarafından yönetilmeyecek şekilde kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20f4a-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="20f4a-108">Tüm ilişkili anahtar kasası yönetimli depolama SAS tanımları da kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="20f4a-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="20f4a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20f4a-109">EXAMPLES</span></span>

### <span data-ttu-id="20f4a-110">Örnek 1: Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="20f4a-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="20f4a-111">' Mykasasına ' anahtar kasasından ' mystorageaccount ' adlı Azure Depolama hesabını disde</span><span class="sxs-lookup"><span data-stu-id="20f4a-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="20f4a-112">' Mystorageaccount ' hesabı kaldırılmayacak.</span><span class="sxs-lookup"><span data-stu-id="20f4a-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="20f4a-113">Bu hesapla ilişkili tüm Anahtar Kasası yönetilen depolama SAS tanımları kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="20f4a-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="20f4a-114">Örnek 2: Anahtar Kasası yönetilen Azure Depolama hesabını ve tüm ilişkili SAS tanımlarını Kullanıcı onayı olmadan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="20f4a-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="20f4a-115">' Mykasasına ' anahtar kasasından ' mystorageaccount ' adlı Azure Depolama hesabını disde</span><span class="sxs-lookup"><span data-stu-id="20f4a-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="20f4a-116">' Mystorageaccount ' hesabı kaldırılmayacak.</span><span class="sxs-lookup"><span data-stu-id="20f4a-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="20f4a-117">Bu hesapla ilişkili tüm Anahtar Kasası yönetilen depolama SAS tanımları kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="20f4a-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="20f4a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20f4a-118">PARAMETERS</span></span>

### <span data-ttu-id="20f4a-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20f4a-119">-AccountName</span></span>
<span data-ttu-id="20f4a-120">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="20f4a-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="20f4a-121">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20f4a-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="20f4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f4a-122">-DefaultProfile</span></span>
<span data-ttu-id="20f4a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="20f4a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20f4a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="20f4a-124">-Force</span></span>
<span data-ttu-id="20f4a-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="20f4a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="20f4a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20f4a-126">-PassThru</span></span>
<span data-ttu-id="20f4a-127">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="20f4a-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="20f4a-128">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="20f4a-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="20f4a-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="20f4a-129">-VaultName</span></span>
<span data-ttu-id="20f4a-130">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="20f4a-130">Vault name.</span></span>
<span data-ttu-id="20f4a-131">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20f4a-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="20f4a-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="20f4a-132">-Confirm</span></span>
<span data-ttu-id="20f4a-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20f4a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f4a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f4a-134">-WhatIf</span></span>
<span data-ttu-id="20f4a-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20f4a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20f4a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="20f4a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f4a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f4a-137">CommonParameters</span></span>
<span data-ttu-id="20f4a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20f4a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f4a-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f4a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f4a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20f4a-140">INPUTS</span></span>

### <span data-ttu-id="20f4a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="20f4a-141">System.String</span></span>

## <span data-ttu-id="20f4a-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20f4a-142">OUTPUTS</span></span>

### <span data-ttu-id="20f4a-143">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20f4a-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="20f4a-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20f4a-144">NOTES</span></span>

## <span data-ttu-id="20f4a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20f4a-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

