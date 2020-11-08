---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275280"
---
# <span data-ttu-id="6ff5c-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="6ff5c-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="6ff5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ff5c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff5c-103">Yönetilen bir HSM 'deki silinmiş anahtarı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="6ff5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ff5c-104">SYNTAX</span></span>

### <span data-ttu-id="6ff5c-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ff5c-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff5c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ff5c-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff5c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ff5c-107">DESCRIPTION</span></span>
<span data-ttu-id="6ff5c-108">**Undo-Azmanagedhsmkeykaldırmada** cmdlet 'i önceden silinmiş bir anahtarı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="6ff5c-109">Kurtarılan anahtar etkin olacak ve tüm normal anahtar işlemlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="6ff5c-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="6ff5c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ff5c-111">EXAMPLES</span></span>

### <span data-ttu-id="6ff5c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ff5c-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="6ff5c-113">Bu komut, önceden silinmiş olan ' testkey001 ' anahtarını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="6ff5c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ff5c-114">PARAMETERS</span></span>

### <span data-ttu-id="6ff5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff5c-115">-DefaultProfile</span></span>
<span data-ttu-id="6ff5c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff5c-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6ff5c-117">-HsmName</span></span>
<span data-ttu-id="6ff5c-118">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-118">HSM name.</span></span> <span data-ttu-id="6ff5c-119">Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6ff5c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ff5c-120">-InputObject</span></span>
<span data-ttu-id="6ff5c-121">Anahtar nesne silindi</span><span class="sxs-lookup"><span data-stu-id="6ff5c-121">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff5c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ff5c-122">-Name</span></span>
<span data-ttu-id="6ff5c-123">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-123">Key name.</span></span>
<span data-ttu-id="6ff5c-124">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan ve anahtar adından bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff5c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ff5c-125">-Confirm</span></span>
<span data-ttu-id="6ff5c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff5c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff5c-127">-WhatIf</span></span>
<span data-ttu-id="6ff5c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff5c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff5c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff5c-130">CommonParameters</span></span>
<span data-ttu-id="6ff5c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff5c-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ff5c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff5c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ff5c-133">INPUTS</span></span>

### <span data-ttu-id="6ff5c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="6ff5c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="6ff5c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ff5c-135">OUTPUTS</span></span>

### <span data-ttu-id="6ff5c-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6ff5c-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="6ff5c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ff5c-137">NOTES</span></span>

## <span data-ttu-id="6ff5c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ff5c-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ff5c-139">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6ff5c-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="6ff5c-140">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6ff5c-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="6ff5c-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6ff5c-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="6ff5c-142">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6ff5c-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="6ff5c-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6ff5c-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="6ff5c-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6ff5c-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)