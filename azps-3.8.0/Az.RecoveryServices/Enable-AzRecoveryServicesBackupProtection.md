---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7b52c6064f7dd692b732558b682290e8612f383c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938216"
---
# <span data-ttu-id="38949-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="38949-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="38949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38949-102">SYNOPSIS</span></span>
<span data-ttu-id="38949-103">Belirtilen yedekleme koruma ilkesine sahip bir öğe için yedeklemeyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="38949-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="38949-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38949-104">SYNTAX</span></span>

### <span data-ttu-id="38949-105">AzureVMComputeEnableProtection (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38949-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38949-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="38949-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38949-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="38949-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38949-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="38949-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38949-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="38949-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38949-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="38949-110">DESCRIPTION</span></span>
<span data-ttu-id="38949-111">**Enable-AzRecoveryServicesBackupProtection** cmdlet 'i bir öğede Azure yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="38949-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="38949-112">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="38949-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="38949-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38949-113">EXAMPLES</span></span>

### <span data-ttu-id="38949-114">Örnek 1: bir öğe için yedekleme korumasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="38949-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="38949-115">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="38949-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="38949-116">İkinci cmdlet, yedeklenecek disk LUN 'Ları belirtir ve $inclusionDiskLUNS değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="38949-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="38949-117">Üçüncü cmdlet $Pol ilkeyi kullanarak V2VM adındaki ARM sanal makinesi için yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="38949-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="38949-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38949-118">PARAMETERS</span></span>

### <span data-ttu-id="38949-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38949-119">-DefaultProfile</span></span>
<span data-ttu-id="38949-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38949-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38949-121">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="38949-121">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="38949-122">Yalnızca işletim sistemi disklerini yedeklemeyi belirtme seçeneği</span><span class="sxs-lookup"><span data-stu-id="38949-122">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="38949-123">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="38949-123">-ExclusionDisksList</span></span>
<span data-ttu-id="38949-124">Yedeklemede dışlanacak disk LUN 'Ları listesi</span><span class="sxs-lookup"><span data-stu-id="38949-124">List of Disk LUNs to exclude in backup</span></span>

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

### <span data-ttu-id="38949-125">-Her Ikisi de</span><span class="sxs-lookup"><span data-stu-id="38949-125">-InclusionDisksList</span></span>
<span data-ttu-id="38949-126">Yedeklemeye eklenecek disk LUN 'Ları listesi</span><span class="sxs-lookup"><span data-stu-id="38949-126">List of Disk LUNs to include in backup</span></span>

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

### <span data-ttu-id="38949-127">-Öğe</span><span class="sxs-lookup"><span data-stu-id="38949-127">-Item</span></span>
<span data-ttu-id="38949-128">Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38949-128">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="38949-129">**Azurermrecoveryservicesbackupıtem** almak için Get-AzRecoveryServicesBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="38949-129">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="38949-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="38949-130">-Name</span></span>
<span data-ttu-id="38949-131">Yedekleme öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38949-131">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="38949-132">-İlke</span><span class="sxs-lookup"><span data-stu-id="38949-132">-Policy</span></span>
<span data-ttu-id="38949-133">Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38949-133">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="38949-134">**Azurermrecoveryservicesbackupprotectionpolicy** nesnesi almak için Get-AzRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="38949-134">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="38949-135">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="38949-135">-ProtectableItem</span></span>
<span data-ttu-id="38949-136">İş durumu için filtre değeri.</span><span class="sxs-lookup"><span data-stu-id="38949-136">Filter value for status of job.</span></span>

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

### <span data-ttu-id="38949-137">-Resetexclusııısettings</span><span class="sxs-lookup"><span data-stu-id="38949-137">-ResetExclusionSettings</span></span>
<span data-ttu-id="38949-138">Öğeyle ilişkilendirilmiş disk dışlama ayarını sıfırlama</span><span class="sxs-lookup"><span data-stu-id="38949-138">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="38949-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38949-139">-ResourceGroupName</span></span>
<span data-ttu-id="38949-140">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38949-140">Specifies the name of the resource group.</span></span>
<span data-ttu-id="38949-141">Bu parametreyi yalnızca ARM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="38949-141">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="38949-142">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="38949-142">-ServiceName</span></span>
<span data-ttu-id="38949-143">Hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38949-143">Specifies the service name.</span></span>
<span data-ttu-id="38949-144">Bu parametreyi yalnızca ASM sanal makineleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="38949-144">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38949-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="38949-145">-StorageAccountName</span></span>
<span data-ttu-id="38949-146">Azure dosya paylaşımı depolama hesabı adı</span><span class="sxs-lookup"><span data-stu-id="38949-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="38949-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="38949-147">-VaultId</span></span>
<span data-ttu-id="38949-148">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="38949-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="38949-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="38949-149">-Confirm</span></span>
<span data-ttu-id="38949-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38949-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38949-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38949-151">-WhatIf</span></span>
<span data-ttu-id="38949-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38949-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38949-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38949-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38949-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38949-154">CommonParameters</span></span>
<span data-ttu-id="38949-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38949-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38949-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="38949-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38949-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38949-157">INPUTS</span></span>

### <span data-ttu-id="38949-158">System. String</span><span class="sxs-lookup"><span data-stu-id="38949-158">System.String</span></span>

### <span data-ttu-id="38949-159">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="38949-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="38949-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38949-160">OUTPUTS</span></span>

### <span data-ttu-id="38949-161">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="38949-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="38949-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38949-162">NOTES</span></span>

## <span data-ttu-id="38949-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38949-163">RELATED LINKS</span></span>

[<span data-ttu-id="38949-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="38949-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="38949-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38949-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


