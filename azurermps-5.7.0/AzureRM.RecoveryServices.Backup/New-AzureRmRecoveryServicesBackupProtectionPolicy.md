---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587482"
---
# <span data-ttu-id="3333e-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3333e-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="3333e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3333e-102">SYNOPSIS</span></span>
<span data-ttu-id="3333e-103">Yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3333e-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3333e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3333e-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3333e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3333e-105">DESCRIPTION</span></span>
<span data-ttu-id="3333e-106">**Yeni-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet 'Inde bir yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3333e-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="3333e-107">Koruma ilkesi en az bir bekletme ilkesiyle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3333e-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="3333e-108">Bekletme ilkesi, bir kurtarma noktasının Azure Backup ile ne kadar tutulacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3333e-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="3333e-109">Varsayılan bekletme ilkesini almak için Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3333e-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="3333e-110">Ayrıca, varsayılan zamanlama ilkesini almak için Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3333e-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="3333e-111">**Schedulepolicy** ve **RetentionPolicy** nesneleri, **Yeni-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet 'inin girdileri olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3333e-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="3333e-112">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3333e-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3333e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3333e-113">EXAMPLES</span></span>

### <span data-ttu-id="3333e-114">Örnek 1: yedekleme koruma ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3333e-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="3333e-115">İlk komut bir temel **Schedulepolicyobject** alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3333e-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="3333e-116">İkinci komut $SchPol zamanlama ilkesindeki tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3333e-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="3333e-117">Üçüncü komut, geçerli tarih ve saati almak için Get-Date cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3333e-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="3333e-118">Dördüncü komut, zamanlama ilkesine zamanlanan çalışma süresi olarak $Dt geçerli tarihi ve saati ekler.</span><span class="sxs-lookup"><span data-stu-id="3333e-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="3333e-119">Beşinci komut bir temel **RetentionPolicy** nesnesi alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3333e-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="3333e-120">Altıncı komut, bekletme süresi ilkesini 365 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3333e-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="3333e-121">Son komutu, önceki komutlar tarafından oluşturulan zamanlama ve bekletme ilkelerine dayalı bir **Backupprotectionpolicy** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3333e-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="3333e-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3333e-122">PARAMETERS</span></span>

### <span data-ttu-id="3333e-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3333e-123">-BackupManagementType</span></span>
<span data-ttu-id="3333e-124">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3333e-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="3333e-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3333e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3333e-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3333e-126">AzureVM</span></span> 
- <span data-ttu-id="3333e-127">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="3333e-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3333e-128">-DefaultProfile</span></span>
<span data-ttu-id="3333e-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3333e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="3333e-130">-Name</span></span>
<span data-ttu-id="3333e-131">İlkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3333e-131">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3333e-132">-RetentionPolicy</span></span>
<span data-ttu-id="3333e-133">Temel **RetentionPolicy** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3333e-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="3333e-134">**RetentionPolicy** nesnesi almak için Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3333e-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="3333e-135">-SchedulePolicy</span></span>
<span data-ttu-id="3333e-136">Temel **Schedulepolicy** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3333e-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="3333e-137">**Schedulepolicy** nesnesini almak için Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3333e-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-138">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="3333e-138">-WorkloadType</span></span>
<span data-ttu-id="3333e-139">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3333e-139">Specifies the workload type.</span></span>
<span data-ttu-id="3333e-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3333e-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3333e-141">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3333e-141">AzureVM</span></span> 
- <span data-ttu-id="3333e-142">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="3333e-142">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="3333e-143">-Confirm</span></span>
<span data-ttu-id="3333e-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3333e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3333e-145">-WhatIf</span></span>
<span data-ttu-id="3333e-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3333e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3333e-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3333e-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3333e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3333e-148">CommonParameters</span></span>
<span data-ttu-id="3333e-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3333e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3333e-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3333e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3333e-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3333e-151">INPUTS</span></span>

### <span data-ttu-id="3333e-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3333e-152">None</span></span>
<span data-ttu-id="3333e-153">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3333e-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3333e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3333e-154">OUTPUTS</span></span>

### <span data-ttu-id="3333e-155">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="3333e-155">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="3333e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3333e-156">NOTES</span></span>

## <span data-ttu-id="3333e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3333e-157">RELATED LINKS</span></span>

[<span data-ttu-id="3333e-158">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3333e-158">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="3333e-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3333e-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3333e-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3333e-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="3333e-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="3333e-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="3333e-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3333e-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3333e-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3333e-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


