---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: 7b56e7d251aee8887fe408237d17d275cb87034e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751610"
---
# <span data-ttu-id="b1f32-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="b1f32-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="b1f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1f32-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f32-103">Önceden silinmiş bir tuş Kasası yönetimli depolama SAS tanımını kurtarır.</span><span class="sxs-lookup"><span data-stu-id="b1f32-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="b1f32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1f32-104">SYNTAX</span></span>

### <span data-ttu-id="b1f32-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1f32-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1f32-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b1f32-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1f32-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f32-108">**Undo-Azanahtarvaultmanagedstoragesasdefinitionkaldırma** komutu, önceden silinmiş bir YÖNETILEN depolama SAS tanımını kurtarır, bu kasa için geçici yazılımdan silme etkinleştirilir ve kurtarma girişimi kurtarma aralığı sırasında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="b1f32-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="b1f32-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1f32-109">EXAMPLES</span></span>

### <span data-ttu-id="b1f32-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1f32-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="b1f32-111">Bu komut dizisi, belirtilen depolama SAS tanımının, silinmiş bir durumda kasada bulunup bulunmadığını belirler; Sonraki komut silinmiş SAS tanımını kurtarır ve bunu etkin bir duruma geri döner.</span><span class="sxs-lookup"><span data-stu-id="b1f32-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="b1f32-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1f32-112">PARAMETERS</span></span>

### <span data-ttu-id="b1f32-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b1f32-113">-AccountName</span></span>
<span data-ttu-id="b1f32-114">Tuş Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b1f32-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="b1f32-115">Cmdlet, kasa adından yönetilen depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı ve yönetilen depolama hesabı adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1f32-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f32-116">-DefaultProfile</span></span>
<span data-ttu-id="b1f32-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1f32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f32-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1f32-118">-InputObject</span></span>
<span data-ttu-id="b1f32-119">Silinmiş yönetilen depolama SAS tanım nesnesi</span><span class="sxs-lookup"><span data-stu-id="b1f32-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f32-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1f32-120">-Name</span></span>
<span data-ttu-id="b1f32-121">Anahtar Kasası yönetimli depolama SAS tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="b1f32-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="b1f32-122">Cmdlet, hedefin FQDN 'sini kasa adından, şu anda seçili ortamdan, yönetilen depolama hesabının adını ve SAS tanımının adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1f32-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f32-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b1f32-123">-VaultName</span></span>
<span data-ttu-id="b1f32-124">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="b1f32-124">Vault name.</span></span>
<span data-ttu-id="b1f32-125">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1f32-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b1f32-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1f32-126">-Confirm</span></span>
<span data-ttu-id="b1f32-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1f32-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f32-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f32-128">-WhatIf</span></span>
<span data-ttu-id="b1f32-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1f32-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f32-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1f32-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f32-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f32-131">CommonParameters</span></span>
<span data-ttu-id="b1f32-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1f32-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f32-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f32-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f32-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1f32-134">INPUTS</span></span>

### <span data-ttu-id="b1f32-135">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultmanagedstoragesasdefinitionıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="b1f32-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="b1f32-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1f32-136">OUTPUTS</span></span>

### <span data-ttu-id="b1f32-137">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b1f32-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b1f32-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1f32-138">NOTES</span></span>

## <span data-ttu-id="b1f32-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1f32-139">RELATED LINKS</span></span>
