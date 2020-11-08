---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275289"
---
# <span data-ttu-id="3b1a5-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="3b1a5-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="3b1a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1a5-103">Yönetilen HSM 'de bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="3b1a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b1a5-104">SYNTAX</span></span>

### <span data-ttu-id="3b1a5-105">RemoveByKeyNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b1a5-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b1a5-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1a5-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b1a5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b1a5-107">DESCRIPTION</span></span>
<span data-ttu-id="3b1a5-108">Remove-AzManagedHsmKey cmdlet 'i yönetilen bir HSM 'de bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="3b1a5-109">Anahtar yanlışlıkla silinmişse anahtar, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzManagedHsmKeyRemoval kullanılarak kurtarılabilir.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="3b1a5-110">Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="3b1a5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b1a5-111">EXAMPLES</span></span>

### <span data-ttu-id="3b1a5-112">Örnek 1: yönetilen HSM 'den anahtar kaldırma</span><span class="sxs-lookup"><span data-stu-id="3b1a5-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="3b1a5-113">Bu komut testmhsm adındaki yönetilen HSM 'den TestKey adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="3b1a5-114">Örnek 2: Kullanıcı onayı olmadan bir anahtarı kaldırma</span><span class="sxs-lookup"><span data-stu-id="3b1a5-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="3b1a5-115">Bu komut testmhsm adındaki yönetilen HSM 'den TestKey adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="3b1a5-116">Komut *Force* parametresini belirtir ve bu nedenle cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="3b1a5-117">Örnek 3: silinen anahtarı, yönetilen HSM kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="3b1a5-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="3b1a5-118">Bu komut testmhsm adlı yönetilen HSM 'den kalıcı olarak adlandırılan anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="3b1a5-119">Bu cmdlet 'i çalıştırmak için, bu yönetilen HSM için önceden kullanıcıya önceden atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="3b1a5-120">Örnek 4: ardışık düzen işlecini kullanarak anahtarları kaldırma</span><span class="sxs-lookup"><span data-stu-id="3b1a5-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="3b1a5-121">Bu komut testmhsm adındaki yönetilen HSM 'deki tüm anahtarları alır ve ardışık düzen işlecini kullanarak bunları **nesne** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3b1a5-122">Bu cmdlet geçerli cmdlet 'e **Enabled** özniteliği için $false değeri olan anahtarları geçirir.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="3b1a5-123">Bu cmdlet bu tuşları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="3b1a5-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b1a5-124">PARAMETERS</span></span>

### <span data-ttu-id="3b1a5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1a5-125">-DefaultProfile</span></span>
<span data-ttu-id="3b1a5-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b1a5-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3b1a5-127">-Force</span></span>
<span data-ttu-id="3b1a5-128">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3b1a5-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="3b1a5-129">-HsmName</span></span>
<span data-ttu-id="3b1a5-130">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-130">HSM name.</span></span> <span data-ttu-id="3b1a5-131">Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1a5-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b1a5-132">-InputObject</span></span>
<span data-ttu-id="3b1a5-133">Anahtar nesnesi</span><span class="sxs-lookup"><span data-stu-id="3b1a5-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1a5-134">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="3b1a5-134">-InRemovedState</span></span>
<span data-ttu-id="3b1a5-135">Önceden silinen anahtarı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="3b1a5-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b1a5-136">-Name</span></span>
<span data-ttu-id="3b1a5-137">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-137">Key name.</span></span>
<span data-ttu-id="3b1a5-138">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan ve anahtar adından bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1a5-139">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3b1a5-139">-PassThru</span></span>
<span data-ttu-id="3b1a5-140">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3b1a5-141">Bu anahtar belirtilmişse, cmdlet silinen Key nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="3b1a5-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b1a5-142">-Confirm</span></span>
<span data-ttu-id="3b1a5-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b1a5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1a5-144">-WhatIf</span></span>
<span data-ttu-id="3b1a5-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b1a5-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b1a5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1a5-147">CommonParameters</span></span>
<span data-ttu-id="3b1a5-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1a5-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1a5-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b1a5-150">INPUTS</span></span>

### <span data-ttu-id="3b1a5-151">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="3b1a5-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="3b1a5-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b1a5-152">OUTPUTS</span></span>

### <span data-ttu-id="3b1a5-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3b1a5-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="3b1a5-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b1a5-154">NOTES</span></span>

## <span data-ttu-id="3b1a5-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b1a5-155">RELATED LINKS</span></span>

[<span data-ttu-id="3b1a5-156">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="3b1a5-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="3b1a5-157">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="3b1a5-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="3b1a5-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="3b1a5-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="3b1a5-159">Geri al-Azmanagedhsmanahtarkaldırma</span><span class="sxs-lookup"><span data-stu-id="3b1a5-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="3b1a5-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="3b1a5-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="3b1a5-161">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="3b1a5-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)