---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: 51fde6c5dd92a2b542dbe49522d372084540ea99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590218"
---
# <span data-ttu-id="bd49a-101">Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="bd49a-101">Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="bd49a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd49a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd49a-103">Önceden silinmiş bir tuş Kasası yönetimli depolama SAS tanımını kurtarır.</span><span class="sxs-lookup"><span data-stu-id="bd49a-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd49a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd49a-104">SYNTAX</span></span>

### <span data-ttu-id="bd49a-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd49a-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd49a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bd49a-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd49a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd49a-107">DESCRIPTION</span></span>
<span data-ttu-id="bd49a-108">**Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval** komutu önceden silinmiş bir YÖNETILEN depolama SAS tanımını kurtarır, bu kasa için geçici yazılımdan silme etkinleştirilir ve kurtarma girişimi de kurtarma aralığı sırasında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="bd49a-108">The **Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="bd49a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd49a-109">EXAMPLES</span></span>

### <span data-ttu-id="bd49a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd49a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

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

<span data-ttu-id="bd49a-111">Bu komut dizisi, belirtilen depolama SAS tanımının, silinmiş bir durumda kasada bulunup bulunmadığını belirler; Sonraki komut silinmiş SAS tanımını kurtarır ve bunu etkin bir duruma geri döner.</span><span class="sxs-lookup"><span data-stu-id="bd49a-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="bd49a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd49a-112">PARAMETERS</span></span>

### <span data-ttu-id="bd49a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd49a-113">-AccountName</span></span>
<span data-ttu-id="bd49a-114">Tuş Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="bd49a-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="bd49a-115">Cmdlet, kasa adından yönetilen depolama SAS tanımının FQDN 'sini, şu anda seçili olan ortamı ve yönetilen depolama hesabı adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd49a-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="bd49a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd49a-116">-DefaultProfile</span></span>
<span data-ttu-id="bd49a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd49a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd49a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd49a-118">-InputObject</span></span>
<span data-ttu-id="bd49a-119">Silinmiş yönetilen depolama SAS tanım nesnesi</span><span class="sxs-lookup"><span data-stu-id="bd49a-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="bd49a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd49a-120">-Name</span></span>
<span data-ttu-id="bd49a-121">Anahtar Kasası yönetimli depolama SAS tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="bd49a-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="bd49a-122">Cmdlet, hedefin FQDN 'sini kasa adından, şu anda seçili ortamdan, yönetilen depolama hesabının adını ve SAS tanımının adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd49a-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="bd49a-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bd49a-123">-VaultName</span></span>
<span data-ttu-id="bd49a-124">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="bd49a-124">Vault name.</span></span>
<span data-ttu-id="bd49a-125">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd49a-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="bd49a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd49a-126">-Confirm</span></span>
<span data-ttu-id="bd49a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd49a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd49a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd49a-128">-WhatIf</span></span>
<span data-ttu-id="bd49a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd49a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd49a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd49a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd49a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd49a-131">CommonParameters</span></span>
<span data-ttu-id="bd49a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd49a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd49a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd49a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd49a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd49a-134">INPUTS</span></span>

### <span data-ttu-id="bd49a-135">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultmanagedstoragesasdefinitionıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="bd49a-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>
<span data-ttu-id="bd49a-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bd49a-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bd49a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd49a-137">OUTPUTS</span></span>

### <span data-ttu-id="bd49a-138">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="bd49a-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="bd49a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd49a-139">NOTES</span></span>

## <span data-ttu-id="bd49a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd49a-140">RELATED LINKS</span></span>
