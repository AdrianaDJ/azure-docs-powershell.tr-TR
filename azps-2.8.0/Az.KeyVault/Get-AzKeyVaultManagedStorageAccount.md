---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 165419eb13376becedf72b4e44ee17f0c3655ec4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751668"
---
# <span data-ttu-id="1d829-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d829-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1d829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d829-102">SYNOPSIS</span></span>
<span data-ttu-id="1d829-103">Anahtar Kasası yönetimli Azure depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="1d829-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="1d829-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d829-104">SYNTAX</span></span>

### <span data-ttu-id="1d829-105">ByAccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1d829-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d829-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d829-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d829-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="1d829-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d829-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d829-108">DESCRIPTION</span></span>
<span data-ttu-id="1d829-109">Hesabın adı belirtilmişse ve hesap anahtarları belirtilen kasa tarafından yönetiliyorsa, Anahtar Kasası yönetilen Azure Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="1d829-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="1d829-110">Hesap adı belirtilmezse, anahtarları belirtilen kasa tarafından yönetilen tüm hesaplar listelenir.</span><span class="sxs-lookup"><span data-stu-id="1d829-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="1d829-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d829-111">EXAMPLES</span></span>

### <span data-ttu-id="1d829-112">Örnek 1: Tüm Anahtar Kasası yönetilen depolama hesaplarını listeler</span><span class="sxs-lookup"><span data-stu-id="1d829-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="1d829-113">Anahtarları ' mykasası ' kasası ile yönetilen tüm hesapları listeler</span><span class="sxs-lookup"><span data-stu-id="1d829-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="1d829-114">Örnek 2: Anahtar Kasası yönetimli depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="1d829-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="1d829-115">Anahtarları ' mykasa ' Kasası tarafından yönetiliyorsa ' mystorageaccount ' Anahtar Kasası yönetimli depolama hesabının ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="1d829-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="1d829-116">Örnek 3: filtreleme kullanarak tüm Anahtar Kasası yönetilen depolama hesaplarını listeleme</span><span class="sxs-lookup"><span data-stu-id="1d829-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="1d829-117">Anahtarları "test" ile başlayan ' mykasa ' Kasası tarafından yönetilen tüm hesapları listeler</span><span class="sxs-lookup"><span data-stu-id="1d829-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="1d829-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d829-118">PARAMETERS</span></span>

### <span data-ttu-id="1d829-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d829-119">-AccountName</span></span>
<span data-ttu-id="1d829-120">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="1d829-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="1d829-121">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d829-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1d829-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d829-122">-DefaultProfile</span></span>
<span data-ttu-id="1d829-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1d829-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d829-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d829-124">-InputObject</span></span>
<span data-ttu-id="1d829-125">Kasa.</span><span class="sxs-lookup"><span data-stu-id="1d829-125">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d829-126">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="1d829-126">-InRemovedState</span></span>
<span data-ttu-id="1d829-127">Çıkışta önceden silinmiş depolama hesaplarının gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d829-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="1d829-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1d829-128">-ResourceId</span></span>
<span data-ttu-id="1d829-129">Kasa kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1d829-129">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d829-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1d829-130">-VaultName</span></span>
<span data-ttu-id="1d829-131">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="1d829-131">Vault name.</span></span>
<span data-ttu-id="1d829-132">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d829-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d829-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d829-133">CommonParameters</span></span>
<span data-ttu-id="1d829-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d829-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d829-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1d829-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d829-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d829-136">INPUTS</span></span>

### <span data-ttu-id="1d829-137">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="1d829-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1d829-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1d829-138">System.String</span></span>

## <span data-ttu-id="1d829-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d829-139">OUTPUTS</span></span>

### <span data-ttu-id="1d829-140">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="1d829-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="1d829-141">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d829-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="1d829-142">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="1d829-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="1d829-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d829-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1d829-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d829-144">NOTES</span></span>

## <span data-ttu-id="1d829-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d829-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

