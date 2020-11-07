---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 15e11e9deedbc8a2e442d9b3f006511a98fd6394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935795"
---
# <span data-ttu-id="e9de8-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e9de8-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e9de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9de8-102">SYNOPSIS</span></span>
<span data-ttu-id="e9de8-103">Anahtar Kasası yönetimli depolama SAS tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e9de8-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="e9de8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9de8-104">SYNTAX</span></span>

### <span data-ttu-id="e9de8-105">ByAccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e9de8-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9de8-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e9de8-106">ByDefinitionName</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9de8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9de8-107">DESCRIPTION</span></span>
<span data-ttu-id="e9de8-108">Tanımın adı belirtilmişse, Anahtar Kasası yönetilen depolama SAS tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="e9de8-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="e9de8-109">Tanım adı belirtilmezse, kasadaki belirtilen anahtar kasası yönetimli depolama hesabıyla ilişkilendirilmiş tüm SAS tanımları listelenir.</span><span class="sxs-lookup"><span data-stu-id="e9de8-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="e9de8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9de8-110">EXAMPLES</span></span>

### <span data-ttu-id="e9de8-111">Örnek 1: Tüm Anahtar Kasası yönetilen depolama SAS tanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="e9de8-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="e9de8-112">' Mykasası ' Kasası tarafından yönetilen ' mystorageaccount ' Anahtar Kasası yönetimli depolama hesabıyla ilişkilendirilmiş tüm SAS tanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="e9de8-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="e9de8-113">Örnek 2: Anahtar Kasası yönetimli depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="e9de8-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="e9de8-114">' Mykasası ' Kasası tarafından yönetilen ' mystorageaccount ' Anahtar Kasası yönetilen depolama hesabı ile ilişkilendirilmiş SAS tanımının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e9de8-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="e9de8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9de8-115">PARAMETERS</span></span>

### <span data-ttu-id="e9de8-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9de8-116">-AccountName</span></span>
<span data-ttu-id="e9de8-117">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="e9de8-117">Vault name.</span></span>
<span data-ttu-id="e9de8-118">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9de8-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e9de8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9de8-119">-DefaultProfile</span></span>
<span data-ttu-id="e9de8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9de8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9de8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9de8-121">-Name</span></span>
<span data-ttu-id="e9de8-122">Depolama SAS tanım adı.</span><span class="sxs-lookup"><span data-stu-id="e9de8-122">Storage sas definition name.</span></span>
<span data-ttu-id="e9de8-123">Cmdlet, kasa adından depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı, depolama hesabı adını ve SAS tanım adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9de8-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9de8-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e9de8-124">-VaultName</span></span>
<span data-ttu-id="e9de8-125">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="e9de8-125">Vault name.</span></span>
<span data-ttu-id="e9de8-126">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9de8-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e9de8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9de8-127">CommonParameters</span></span>
<span data-ttu-id="e9de8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9de8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9de8-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9de8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9de8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9de8-130">INPUTS</span></span>

### <span data-ttu-id="e9de8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e9de8-131">System.String</span></span>

## <span data-ttu-id="e9de8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9de8-132">OUTPUTS</span></span>

### <span data-ttu-id="e9de8-133">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Keykasa. modeller. Managedstoragesasdefinitionlistıtem, Microsoft. Azure. Commands. Keykasası, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e9de8-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e9de8-134">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e9de8-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e9de8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9de8-135">NOTES</span></span>

## <span data-ttu-id="e9de8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9de8-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

