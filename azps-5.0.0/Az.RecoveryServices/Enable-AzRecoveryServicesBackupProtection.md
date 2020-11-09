---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323074"
---
# <span data-ttu-id="2ae43-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2ae43-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="2ae43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ae43-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae43-103">Belirtilen yedekleme koruma ilkesine sahip bir öğe için yedeklemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="2ae43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ae43-104">SYNTAX</span></span>

### <span data-ttu-id="2ae43-105">AzureVMComputeEnableProtection (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ae43-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ae43-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2ae43-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae43-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2ae43-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae43-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2ae43-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae43-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="2ae43-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ae43-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ae43-110">DESCRIPTION</span></span>
<span data-ttu-id="2ae43-111">**Enable-AzRecoveryServicesBackupProtection** cmdlet 'i, bir koruma ilkesini öğeyle ilişkilendirerek yedekleme özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="2ae43-112">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2ae43-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2ae43-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ae43-113">EXAMPLES</span></span>

### <span data-ttu-id="2ae43-114">Örnek 1: bir öğe için yedekleme korumasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2ae43-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="2ae43-115">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2ae43-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="2ae43-116">İkinci cmdlet, yedeklenecek disk LUN 'Ları belirtir ve $inclusionDiskLUNS değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2ae43-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="2ae43-117">Üçüncü cmdlet $Pol ilkeyi kullanarak V2VM adındaki ARM sanal makinesi için yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2ae43-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="2ae43-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2ae43-118">Example 2</span></span>

<span data-ttu-id="2ae43-119">Belirtilen yedekleme koruma ilkesine sahip bir öğe için yedeklemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="2ae43-120">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="2ae43-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="2ae43-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ae43-121">PARAMETERS</span></span>

### <span data-ttu-id="2ae43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae43-122">-DefaultProfile</span></span>
<span data-ttu-id="2ae43-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ae43-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ae43-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="2ae43-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="2ae43-125">Yalnızca işletim sistemi disklerini yedeklemeyi belirtme seçeneği</span><span class="sxs-lookup"><span data-stu-id="2ae43-125">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="2ae43-126">-ExclusionDisksList</span></span>
<span data-ttu-id="2ae43-127">Yedeklemede dışlanacak disk LUN 'Ları listesi, Rest otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-128">-Her Ikisi de</span><span class="sxs-lookup"><span data-stu-id="2ae43-128">-InclusionDisksList</span></span>
<span data-ttu-id="2ae43-129">Yedeklemeye dahil edilecek disk LUN 'Ları listesi ve REST, işletim sistemi diski dışında otomatik olarak dışlanır.</span><span class="sxs-lookup"><span data-stu-id="2ae43-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-130">-Öğe</span><span class="sxs-lookup"><span data-stu-id="2ae43-130">-Item</span></span>
<span data-ttu-id="2ae43-131">Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="2ae43-132">**Azurermrecoveryservicesbackupıtem** almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ae43-132">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ae43-133">-Name</span></span>
<span data-ttu-id="2ae43-134">Yedekleme öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-134">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-135">-İlke</span><span class="sxs-lookup"><span data-stu-id="2ae43-135">-Policy</span></span>
<span data-ttu-id="2ae43-136">Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="2ae43-137">**Azurermrecoveryservicesbackupprotectionpolicy** nesnesi almak için Get-AzRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ae43-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-138">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="2ae43-138">-ProtectableItem</span></span>
<span data-ttu-id="2ae43-139">Verilen ilke ile korunacak öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-139">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-140">-Resetexclusııısettings</span><span class="sxs-lookup"><span data-stu-id="2ae43-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="2ae43-141">Öğeyle ilişkilendirilmiş disk dışlama ayarını sıfırlama</span><span class="sxs-lookup"><span data-stu-id="2ae43-141">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae43-142">-ResourceGroupName</span></span>
<span data-ttu-id="2ae43-143">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="2ae43-144">Bu parametreyi yalnızca ARM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="2ae43-144">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2ae43-145">-StorageAccountName</span></span>
<span data-ttu-id="2ae43-146">Azure dosya paylaşımı depolama hesabı adı</span><span class="sxs-lookup"><span data-stu-id="2ae43-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2ae43-147">-VaultId</span></span>
<span data-ttu-id="2ae43-148">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2ae43-148">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae43-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ae43-149">-Confirm</span></span>
<span data-ttu-id="2ae43-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ae43-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae43-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae43-151">-WhatIf</span></span>
<span data-ttu-id="2ae43-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ae43-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="2ae43-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae43-153">CommonParameters</span></span>
<span data-ttu-id="2ae43-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ae43-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae43-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ae43-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae43-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ae43-156">INPUTS</span></span>

### <span data-ttu-id="2ae43-157">System. String</span><span class="sxs-lookup"><span data-stu-id="2ae43-157">System.String</span></span>

### <span data-ttu-id="2ae43-158">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="2ae43-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="2ae43-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ae43-159">OUTPUTS</span></span>

### <span data-ttu-id="2ae43-160">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="2ae43-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2ae43-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ae43-161">NOTES</span></span>

## <span data-ttu-id="2ae43-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ae43-162">RELATED LINKS</span></span>

[<span data-ttu-id="2ae43-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2ae43-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2ae43-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2ae43-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


