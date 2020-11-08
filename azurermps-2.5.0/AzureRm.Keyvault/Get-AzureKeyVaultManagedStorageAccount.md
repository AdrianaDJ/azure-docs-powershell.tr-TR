---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 51e7b941e5dbb4d07b48444196f6e3d3aa830452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939551"
---
# <span data-ttu-id="ee8c5-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee8c5-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ee8c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8c5-103">Anahtar Kasası yönetimli Azure depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee8c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee8c5-104">SYNTAX</span></span>

### <span data-ttu-id="ee8c5-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee8c5-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee8c5-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="ee8c5-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee8c5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee8c5-107">DESCRIPTION</span></span>
<span data-ttu-id="ee8c5-108">Hesabın adı belirtilmişse ve hesap anahtarları belirtilen kasa tarafından yönetiliyorsa, Anahtar Kasası yönetilen Azure Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="ee8c5-109">Hesap adı belirtilmezse, anahtarları belirtilen kasa tarafından yönetilen tüm hesaplar listelenir.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="ee8c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee8c5-110">EXAMPLES</span></span>

### <span data-ttu-id="ee8c5-111">Örnek 1: Tüm Anahtar Kasası yönetilen depolama hesaplarını listeler</span><span class="sxs-lookup"><span data-stu-id="ee8c5-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="ee8c5-112">Anahtarları ' mykasası ' kasası ile yönetilen tüm hesapları listeler</span><span class="sxs-lookup"><span data-stu-id="ee8c5-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="ee8c5-113">Örnek 2: Anahtar Kasası yönetimli depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="ee8c5-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="ee8c5-114">Anahtarları ' mykasa ' Kasası tarafından yönetiliyorsa ' mystorageaccount ' Anahtar Kasası yönetimli depolama hesabının ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="ee8c5-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="ee8c5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee8c5-115">PARAMETERS</span></span>

### <span data-ttu-id="ee8c5-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ee8c5-116">-AccountName</span></span>
<span data-ttu-id="ee8c5-117">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="ee8c5-118">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="ee8c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8c5-119">-DefaultProfile</span></span>
<span data-ttu-id="ee8c5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee8c5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee8c5-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ee8c5-121">-VaultName</span></span>
<span data-ttu-id="ee8c5-122">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-122">Vault name.</span></span>
<span data-ttu-id="ee8c5-123">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ee8c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8c5-124">CommonParameters</span></span>
<span data-ttu-id="ee8c5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8c5-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee8c5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8c5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee8c5-127">INPUTS</span></span>

### <span data-ttu-id="ee8c5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ee8c5-128">System.String</span></span>

## <span data-ttu-id="ee8c5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee8c5-129">OUTPUTS</span></span>

### <span data-ttu-id="ee8c5-130">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Keykasa. modeller. ManagedStorageAccount, Microsoft. Azure. Commands. Keykasası, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ee8c5-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ee8c5-131">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee8c5-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="ee8c5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee8c5-132">NOTES</span></span>

## <span data-ttu-id="ee8c5-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee8c5-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
