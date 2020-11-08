---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267349"
---
# <span data-ttu-id="888f1-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="888f1-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="888f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="888f1-102">SYNOPSIS</span></span>
<span data-ttu-id="888f1-103">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="888f1-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="888f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="888f1-104">SYNTAX</span></span>

### <span data-ttu-id="888f1-105">ByDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="888f1-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="888f1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="888f1-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="888f1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="888f1-107">DESCRIPTION</span></span>
<span data-ttu-id="888f1-108">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur ve anahtarı etkin anahtar olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="888f1-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="888f1-109">Anahtar Kasası proxy 'leri anahtarı yeniden oluşturmak için Azure Resource Manager 'a çağrı.</span><span class="sxs-lookup"><span data-stu-id="888f1-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="888f1-110">Arayan, verilen Azure depolama hesabında anahtarları yeniden oluşturmak için izinleri karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="888f1-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="888f1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="888f1-111">EXAMPLES</span></span>

### <span data-ttu-id="888f1-112">Örnek 1: anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="888f1-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="888f1-113">' Mystorageaccount ' hesabının ' anahtar ' hesabını yeniden oluşturur ve ' anahtar ' değerini Anahtar Kasası yönetilen Azure depolama hesabı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="888f1-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="888f1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="888f1-114">PARAMETERS</span></span>

### <span data-ttu-id="888f1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="888f1-115">-AccountName</span></span>
<span data-ttu-id="888f1-116">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="888f1-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="888f1-117">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="888f1-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888f1-118">-DefaultProfile</span></span>
<span data-ttu-id="888f1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="888f1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="888f1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="888f1-120">-Force</span></span>
<span data-ttu-id="888f1-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="888f1-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="888f1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="888f1-122">-InputObject</span></span>
<span data-ttu-id="888f1-123">ManagedStorageAccount nesnesi.</span><span class="sxs-lookup"><span data-stu-id="888f1-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="888f1-124">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="888f1-124">-KeyName</span></span>
<span data-ttu-id="888f1-125">Yeniden oluşturmak ve etkinleştirmek için depolama hesabı anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="888f1-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888f1-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="888f1-126">-PassThru</span></span>
<span data-ttu-id="888f1-127">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="888f1-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="888f1-128">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="888f1-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="888f1-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="888f1-129">-VaultName</span></span>
<span data-ttu-id="888f1-130">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="888f1-130">Vault name.</span></span>
<span data-ttu-id="888f1-131">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="888f1-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888f1-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="888f1-132">-Confirm</span></span>
<span data-ttu-id="888f1-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="888f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="888f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="888f1-134">-WhatIf</span></span>
<span data-ttu-id="888f1-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="888f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="888f1-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="888f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="888f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888f1-137">CommonParameters</span></span>
<span data-ttu-id="888f1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="888f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888f1-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="888f1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888f1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="888f1-140">INPUTS</span></span>

### <span data-ttu-id="888f1-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="888f1-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="888f1-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="888f1-142">OUTPUTS</span></span>

### <span data-ttu-id="888f1-143">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="888f1-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="888f1-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="888f1-144">NOTES</span></span>

## <span data-ttu-id="888f1-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="888f1-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

