---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933455"
---
# <span data-ttu-id="582df-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="582df-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="582df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="582df-102">SYNOPSIS</span></span>
<span data-ttu-id="582df-103">Yedekleme koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="582df-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="582df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="582df-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="582df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="582df-105">DESCRIPTION</span></span>
<span data-ttu-id="582df-106">**Set-AzBackupProtectionPolicy** cmdlet 'i mevcut bir Azure yedekleme koruması ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="582df-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="582df-107">Yedekleme zamanlaması ve bekletme ilkesi bileşenlerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="582df-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="582df-108">Yaptığınız tüm değişiklikler, ilkeyle ilişkili öğeleri yedeklemeyi ve bekletmesini etkiler.</span><span class="sxs-lookup"><span data-stu-id="582df-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="582df-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="582df-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="582df-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="582df-110">EXAMPLES</span></span>

### <span data-ttu-id="582df-111">Örnek 1: yedekleme koruma ilkesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="582df-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="582df-112">İlk komut bir temel SchedulePolicy nesnesi alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="582df-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="582df-113">İkinci komut $SchPol zamanlama ilkesindeki tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="582df-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="582df-114">Üçüncü komut, Get-Date cmdlet 'ini kullanarak geçerli tarih ve saati alır ve $DT değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="582df-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="582df-115">Dördüncü komut $DT tarih ve saati zamanlama ilkesinin çalışma zamanına göre ekler.</span><span class="sxs-lookup"><span data-stu-id="582df-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="582df-116">Beşinci komut bir temel bekletme ilkesi nesnesi alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="582df-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="582df-117">Altıncı komut, bekletme süresini 365 güne ayarlar.</span><span class="sxs-lookup"><span data-stu-id="582df-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="582df-118">Yedinci komutu NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="582df-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="582df-119">Son komutu, $SchPol zamanlama ilkesini ve $RetPol bekletme ilkesini kullanarak $Pol yedekleme koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="582df-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="582df-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="582df-120">PARAMETERS</span></span>

### <span data-ttu-id="582df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582df-121">-DefaultProfile</span></span>
<span data-ttu-id="582df-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="582df-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="582df-123">-İlke</span><span class="sxs-lookup"><span data-stu-id="582df-123">-Policy</span></span>
<span data-ttu-id="582df-124">Bu cmdlet 'in değiştirdiği yedekleme koruması ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="582df-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="582df-125">**Backupprotectionpolicy** nesnesi edinmek için Get-AzRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="582df-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="582df-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="582df-126">-RetentionPolicy</span></span>
<span data-ttu-id="582df-127">Temel bekletme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="582df-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="582df-128">**RetentionPolicy** nesnesi almak için Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="582df-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="582df-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="582df-129">-SchedulePolicy</span></span>
<span data-ttu-id="582df-130">Temel zamanlama İlkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="582df-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="582df-131">**Schedulepolicy** nesnesi edinmek için Get-AzRecoveryServicesBackupSchedulePolicyObject nesnesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="582df-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="582df-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="582df-132">-VaultId</span></span>
<span data-ttu-id="582df-133">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="582df-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="582df-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="582df-134">-Confirm</span></span>
<span data-ttu-id="582df-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="582df-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="582df-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="582df-136">-WhatIf</span></span>
<span data-ttu-id="582df-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="582df-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="582df-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="582df-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="582df-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582df-139">CommonParameters</span></span>
<span data-ttu-id="582df-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="582df-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582df-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="582df-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582df-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="582df-142">INPUTS</span></span>

### <span data-ttu-id="582df-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="582df-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="582df-144">System. String</span><span class="sxs-lookup"><span data-stu-id="582df-144">System.String</span></span>

## <span data-ttu-id="582df-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="582df-145">OUTPUTS</span></span>

### <span data-ttu-id="582df-146">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="582df-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="582df-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="582df-147">NOTES</span></span>

## <span data-ttu-id="582df-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="582df-148">RELATED LINKS</span></span>

[<span data-ttu-id="582df-149">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="582df-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="582df-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="582df-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="582df-151">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="582df-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="582df-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="582df-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


