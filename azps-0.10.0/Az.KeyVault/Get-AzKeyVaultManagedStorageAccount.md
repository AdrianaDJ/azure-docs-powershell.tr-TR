---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936668"
---
# <span data-ttu-id="d8d3c-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8d3c-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d8d3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d3c-103">Anahtar Kasası yönetimli Azure depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="d8d3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8d3c-104">SYNTAX</span></span>

### <span data-ttu-id="d8d3c-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8d3c-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8d3c-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="d8d3c-106">ByAccountName</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d3c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8d3c-107">DESCRIPTION</span></span>
<span data-ttu-id="d8d3c-108">Hesabın adı belirtilmişse ve hesap anahtarları belirtilen kasa tarafından yönetiliyorsa, Anahtar Kasası yönetilen Azure Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="d8d3c-109">Hesap adı belirtilmezse, anahtarları belirtilen kasa tarafından yönetilen tüm hesaplar listelenir.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="d8d3c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8d3c-110">EXAMPLES</span></span>

### <span data-ttu-id="d8d3c-111">Örnek 1: Tüm Anahtar Kasası yönetilen depolama hesaplarını listeler</span><span class="sxs-lookup"><span data-stu-id="d8d3c-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="d8d3c-112">Anahtarları ' mykasası ' kasası ile yönetilen tüm hesapları listeler</span><span class="sxs-lookup"><span data-stu-id="d8d3c-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="d8d3c-113">Örnek 2: Anahtar Kasası yönetimli depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="d8d3c-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="d8d3c-114">Anahtarları ' mykasa ' Kasası tarafından yönetiliyorsa ' mystorageaccount ' Anahtar Kasası yönetimli depolama hesabının ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="d8d3c-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="d8d3c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8d3c-115">PARAMETERS</span></span>

### <span data-ttu-id="d8d3c-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d8d3c-116">-AccountName</span></span>
<span data-ttu-id="d8d3c-117">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="d8d3c-118">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d3c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d3c-119">-DefaultProfile</span></span>
<span data-ttu-id="d8d3c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d8d3c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8d3c-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d8d3c-121">-VaultName</span></span>
<span data-ttu-id="d8d3c-122">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-122">Vault name.</span></span>
<span data-ttu-id="d8d3c-123">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d8d3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d3c-124">CommonParameters</span></span>
<span data-ttu-id="d8d3c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8d3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d3c-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d3c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d3c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8d3c-127">INPUTS</span></span>

### <span data-ttu-id="d8d3c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d8d3c-128">System.String</span></span>

## <span data-ttu-id="d8d3c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8d3c-129">OUTPUTS</span></span>

### <span data-ttu-id="d8d3c-130">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Keykasa. modeller. ManagedStorageAccount, Microsoft. Azure. Commands. Keykasası, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d8d3c-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d8d3c-131">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8d3c-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="d8d3c-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8d3c-132">NOTES</span></span>

## <span data-ttu-id="d8d3c-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8d3c-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

