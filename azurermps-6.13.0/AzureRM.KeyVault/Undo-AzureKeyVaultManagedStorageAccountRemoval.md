---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: a8e8bb9a4a006c30275f1de959181ad640a04f88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764649"
---
# <span data-ttu-id="30fe1-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="30fe1-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="30fe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="30fe1-103">Önceden silinmiş bir Keykasası yönetimli depolama hesabını kurtarır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30fe1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30fe1-104">SYNTAX</span></span>

### <span data-ttu-id="30fe1-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30fe1-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30fe1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="30fe1-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval
 [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30fe1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="30fe1-107">DESCRIPTION</span></span>
<span data-ttu-id="30fe1-108">**Undo-AzureKeyVaultManagedStorageAccountRemoval** komutu önceden silinmiş bir yönetilen depolama hesabını kurtarır, bu kasa için geçici yazılımdan silme özelliği etkin ve kurtarma girişimi de kurtarma aralığı sırasında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-108">The **Undo-AzureKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="30fe1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30fe1-109">EXAMPLES</span></span>

### <span data-ttu-id="30fe1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="30fe1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="30fe1-111">Bu komut dizisi, belirtilen depolama hesabının kasada silinmiş bir durumda olup olmadığını belirler; Sonraki komut silinmiş depolama hesabını kurtarır ve etkin bir duruma geri döner.</span><span class="sxs-lookup"><span data-stu-id="30fe1-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="30fe1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30fe1-112">PARAMETERS</span></span>

### <span data-ttu-id="30fe1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30fe1-113">-DefaultProfile</span></span>
<span data-ttu-id="30fe1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30fe1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30fe1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30fe1-115">-InputObject</span></span>
<span data-ttu-id="30fe1-116">Yönetilen depolama hesabı nesnesi silindi</span><span class="sxs-lookup"><span data-stu-id="30fe1-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30fe1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="30fe1-117">-Name</span></span>
<span data-ttu-id="30fe1-118">Anahtar Kasası yönetilen depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="30fe1-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="30fe1-119">Cmdlet, hedef için kasa adı, seçili ortam ve yönetilen depolama hesabının adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30fe1-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30fe1-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="30fe1-120">-VaultName</span></span>
<span data-ttu-id="30fe1-121">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="30fe1-121">Vault name.</span></span>
<span data-ttu-id="30fe1-122">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30fe1-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30fe1-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="30fe1-123">-Confirm</span></span>
<span data-ttu-id="30fe1-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30fe1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30fe1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30fe1-125">-WhatIf</span></span>
<span data-ttu-id="30fe1-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30fe1-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30fe1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30fe1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30fe1-128">CommonParameters</span></span>
<span data-ttu-id="30fe1-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30fe1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30fe1-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30fe1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30fe1-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30fe1-131">INPUTS</span></span>

### <span data-ttu-id="30fe1-132">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="30fe1-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="30fe1-133">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30fe1-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="30fe1-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30fe1-134">OUTPUTS</span></span>

### <span data-ttu-id="30fe1-135">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30fe1-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="30fe1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30fe1-136">NOTES</span></span>

## <span data-ttu-id="30fe1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30fe1-137">RELATED LINKS</span></span>
