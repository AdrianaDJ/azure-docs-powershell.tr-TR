---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 6aaf7fcd32ae7d50f273d69835f9131032b68c21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933481"
---
# <span data-ttu-id="799bf-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="799bf-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="799bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="799bf-102">SYNOPSIS</span></span>
<span data-ttu-id="799bf-103">Yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="799bf-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="799bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="799bf-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="799bf-105">DESCRIPTION</span></span>
<span data-ttu-id="799bf-106">**New-AzRecoveryServicesBackupProtectionPolicy** cmdlet 'Inde bir yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="799bf-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="799bf-107">Koruma ilkesi en az bir bekletme ilkesiyle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="799bf-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="799bf-108">Bekletme ilkesi, bir kurtarma noktasının Azure Backup ile ne kadar tutulacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="799bf-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="799bf-109">Varsayılan bekletme ilkesini almak için Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="799bf-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="799bf-110">Ayrıca, varsayılan zamanlama ilkesini almak için Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="799bf-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="799bf-111">**Schedulepolicy** ve **RetentionPolicy** nesneleri, **Yeni-AzRecoveryServicesBackupProtectionPolicy** cmdlet 'ine giriş olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="799bf-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="799bf-112">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="799bf-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="799bf-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="799bf-113">EXAMPLES</span></span>

### <span data-ttu-id="799bf-114">Örnek 1: yedekleme koruma ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="799bf-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="799bf-115">İlk komut bir temel **Schedulepolicyobject** alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="799bf-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="799bf-116">İkinci komut $SchPol zamanlama ilkesindeki tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="799bf-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="799bf-117">Üçüncü komut, geçerli tarih ve saati almak için Get-Date cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="799bf-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="799bf-118">Dördüncü komut, zamanlama ilkesine zamanlanan çalışma süresi olarak $Dt geçerli tarihi ve saati ekler.</span><span class="sxs-lookup"><span data-stu-id="799bf-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="799bf-119">Beşinci komut bir temel **RetentionPolicy** nesnesi alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="799bf-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="799bf-120">Altıncı komut, bekletme süresi ilkesini 365 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="799bf-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="799bf-121">Son komutu, önceki komutlar tarafından oluşturulan zamanlama ve bekletme ilkelerine dayalı bir **Backupprotectionpolicy** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="799bf-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="799bf-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="799bf-122">PARAMETERS</span></span>

### <span data-ttu-id="799bf-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="799bf-123">-BackupManagementType</span></span>
<span data-ttu-id="799bf-124">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="799bf-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="799bf-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="799bf-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="799bf-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="799bf-126">AzureVM</span></span> 
- <span data-ttu-id="799bf-127">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="799bf-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="799bf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799bf-128">-DefaultProfile</span></span>
<span data-ttu-id="799bf-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="799bf-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="799bf-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="799bf-130">-Name</span></span>
<span data-ttu-id="799bf-131">İlkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="799bf-131">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799bf-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="799bf-132">-RetentionPolicy</span></span>
<span data-ttu-id="799bf-133">Temel **RetentionPolicy** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="799bf-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="799bf-134">**RetentionPolicy** nesnesi almak için Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="799bf-134">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="799bf-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="799bf-135">-SchedulePolicy</span></span>
<span data-ttu-id="799bf-136">Temel **Schedulepolicy** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="799bf-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="799bf-137">**Schedulepolicy** nesnesini almak için Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="799bf-137">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="799bf-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="799bf-138">-VaultId</span></span>
<span data-ttu-id="799bf-139">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="799bf-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="799bf-140">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="799bf-140">-WorkloadType</span></span>
<span data-ttu-id="799bf-141">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="799bf-141">Specifies the workload type.</span></span>
<span data-ttu-id="799bf-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="799bf-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="799bf-143">AzureVM</span><span class="sxs-lookup"><span data-stu-id="799bf-143">AzureVM</span></span> 
- <span data-ttu-id="799bf-144">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="799bf-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="799bf-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="799bf-145">-Confirm</span></span>
<span data-ttu-id="799bf-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="799bf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799bf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799bf-147">-WhatIf</span></span>
<span data-ttu-id="799bf-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="799bf-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="799bf-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="799bf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799bf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799bf-150">CommonParameters</span></span>
<span data-ttu-id="799bf-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="799bf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799bf-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="799bf-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799bf-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="799bf-153">INPUTS</span></span>

### <span data-ttu-id="799bf-154">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="799bf-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="799bf-155">System. Nullable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. Yedeklememanagementtype, Microsoft. Azure. PowerShell. cmdlet. RecoveryServices. Backup. model, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="799bf-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="799bf-156">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="799bf-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="799bf-157">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="799bf-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="799bf-158">System. String</span><span class="sxs-lookup"><span data-stu-id="799bf-158">System.String</span></span>

## <span data-ttu-id="799bf-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="799bf-159">OUTPUTS</span></span>

### <span data-ttu-id="799bf-160">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="799bf-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="799bf-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="799bf-161">NOTES</span></span>

## <span data-ttu-id="799bf-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="799bf-162">RELATED LINKS</span></span>

[<span data-ttu-id="799bf-163">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="799bf-163">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="799bf-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="799bf-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="799bf-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="799bf-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="799bf-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="799bf-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="799bf-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="799bf-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="799bf-168">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="799bf-168">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

