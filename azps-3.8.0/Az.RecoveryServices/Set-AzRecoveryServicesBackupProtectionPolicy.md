---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 16bb97fdfab6d890f67bef209acaa584b5a67487
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94099000"
---
# <span data-ttu-id="b103d-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b103d-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="b103d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b103d-102">SYNOPSIS</span></span>
<span data-ttu-id="b103d-103">Yedekleme koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b103d-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="b103d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b103d-104">SYNTAX</span></span>

### <span data-ttu-id="b103d-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="b103d-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b103d-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="b103d-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b103d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b103d-107">DESCRIPTION</span></span>
<span data-ttu-id="b103d-108">**Set-AzBackupProtectionPolicy** cmdlet 'i mevcut bir Azure yedekleme koruması ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b103d-108">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="b103d-109">Yedekleme zamanlaması ve bekletme ilkesi bileşenlerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b103d-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="b103d-110">Yaptığınız tüm değişiklikler, ilkeyle ilişkili öğeleri yedeklemeyi ve bekletmesini etkiler.</span><span class="sxs-lookup"><span data-stu-id="b103d-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="b103d-111">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b103d-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b103d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b103d-112">EXAMPLES</span></span>

### <span data-ttu-id="b103d-113">Örnek 1: yedekleme koruma ilkesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="b103d-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="b103d-114">İlk komut bir temel SchedulePolicy nesnesi alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b103d-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="b103d-115">İkinci komut $SchPol zamanlama ilkesindeki tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b103d-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="b103d-116">Üçüncü komut, Get-Date cmdlet 'ini kullanarak geçerli tarih ve saati alır ve $DT değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b103d-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="b103d-117">Dördüncü komut $DT tarih ve saati zamanlama ilkesinin çalışma zamanına göre ekler.</span><span class="sxs-lookup"><span data-stu-id="b103d-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="b103d-118">Beşinci komut bir temel bekletme ilkesi nesnesi alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b103d-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="b103d-119">Altıncı komut, bekletme süresini 365 güne ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b103d-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="b103d-120">Yedinci komutu NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b103d-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="b103d-121">Sekizinci ve dokuzuncu, geri yükleme noktalarını depolayan ilkeyle ilişkilendirilmiş kaynak grubu parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b103d-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="b103d-122">Son komutu, $SchPol zamanlama ilkesini ve $RetPol bekletme ilkesini kullanarak $Pol yedekleme koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b103d-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="b103d-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b103d-123">PARAMETERS</span></span>

### <span data-ttu-id="b103d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b103d-124">-DefaultProfile</span></span>
<span data-ttu-id="b103d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b103d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b103d-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="b103d-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="b103d-127">Başarısız öğeler için Ilke güncelleştirmesini yeniden denemeyi belirten Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="b103d-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b103d-128">-İlke</span><span class="sxs-lookup"><span data-stu-id="b103d-128">-Policy</span></span>
<span data-ttu-id="b103d-129">Bu cmdlet 'in değiştirdiği yedekleme koruması ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b103d-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="b103d-130">**Backupprotectionpolicy** nesnesi edinmek için Get-AzRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b103d-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b103d-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b103d-131">-RetentionPolicy</span></span>
<span data-ttu-id="b103d-132">Temel bekletme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b103d-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="b103d-133">**RetentionPolicy** nesnesi almak için Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b103d-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b103d-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="b103d-134">-SchedulePolicy</span></span>
<span data-ttu-id="b103d-135">Temel zamanlama İlkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b103d-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="b103d-136">**Schedulepolicy** nesnesi edinmek için Get-AzRecoveryServicesBackupSchedulePolicyObject nesnesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b103d-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b103d-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b103d-137">-VaultId</span></span>
<span data-ttu-id="b103d-138">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b103d-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b103d-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="b103d-139">-Confirm</span></span>
<span data-ttu-id="b103d-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b103d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b103d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b103d-141">-WhatIf</span></span>
<span data-ttu-id="b103d-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b103d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b103d-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b103d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b103d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b103d-144">CommonParameters</span></span>
<span data-ttu-id="b103d-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b103d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b103d-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b103d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b103d-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b103d-147">INPUTS</span></span>

### <span data-ttu-id="b103d-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="b103d-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="b103d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b103d-149">System.String</span></span>

## <span data-ttu-id="b103d-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b103d-150">OUTPUTS</span></span>

### <span data-ttu-id="b103d-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="b103d-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b103d-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b103d-152">NOTES</span></span>

## <span data-ttu-id="b103d-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b103d-153">RELATED LINKS</span></span>

[<span data-ttu-id="b103d-154">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b103d-154">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b103d-155">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b103d-155">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="b103d-156">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b103d-156">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b103d-157">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b103d-157">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


