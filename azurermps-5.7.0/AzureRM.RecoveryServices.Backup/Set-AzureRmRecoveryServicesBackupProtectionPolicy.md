---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 5a60320736e65fae83547bbf9b2825979f73601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587480"
---
# <span data-ttu-id="6d312-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d312-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6d312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d312-102">SYNOPSIS</span></span>
<span data-ttu-id="6d312-103">Yedekleme koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d312-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d312-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d312-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d312-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d312-105">DESCRIPTION</span></span>
<span data-ttu-id="6d312-106">**Set-AzureRmBackupProtectionPolicy** cmdlet 'i mevcut bir Azure yedekleme koruması ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d312-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="6d312-107">Yedekleme zamanlaması ve bekletme ilkesi bileşenlerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d312-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="6d312-108">Yaptığınız tüm değişiklikler, ilkeyle ilişkili öğeleri yedeklemeyi ve bekletmesini etkiler.</span><span class="sxs-lookup"><span data-stu-id="6d312-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="6d312-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6d312-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6d312-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d312-110">EXAMPLES</span></span>

### <span data-ttu-id="6d312-111">Örnek 1: yedekleme koruma ilkesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="6d312-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="6d312-112">İlk komut bir temel SchedulePolicy nesnesi alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6d312-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="6d312-113">İkinci komut $SchPol zamanlama ilkesindeki tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d312-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="6d312-114">Üçüncü komut, Get-Date cmdlet 'ini kullanarak geçerli tarih ve saati alır ve $DT değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6d312-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="6d312-115">Dördüncü komut $DT tarih ve saati zamanlama ilkesinin çalışma zamanına göre ekler.</span><span class="sxs-lookup"><span data-stu-id="6d312-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="6d312-116">Beşinci komut bir temel bekletme ilkesi nesnesi alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6d312-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="6d312-117">Altıncı komut, bekletme süresini 365 güne ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6d312-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="6d312-118">Yedinci komutu NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6d312-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="6d312-119">Son komutu, $SchPol zamanlama ilkesini ve $RetPol bekletme ilkesini kullanarak $Pol yedekleme koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d312-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="6d312-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d312-120">PARAMETERS</span></span>

### <span data-ttu-id="6d312-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d312-121">-DefaultProfile</span></span>
<span data-ttu-id="6d312-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d312-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d312-123">-İlke</span><span class="sxs-lookup"><span data-stu-id="6d312-123">-Policy</span></span>
<span data-ttu-id="6d312-124">Bu cmdlet 'in değiştirdiği yedekleme koruması ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d312-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="6d312-125">**Backupprotectionpolicy** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d312-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d312-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d312-126">-RetentionPolicy</span></span>
<span data-ttu-id="6d312-127">Temel bekletme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d312-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="6d312-128">**RetentionPolicy** nesnesi almak için Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d312-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d312-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="6d312-129">-SchedulePolicy</span></span>
<span data-ttu-id="6d312-130">Temel zamanlama İlkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d312-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="6d312-131">**Schedulepolicy** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupSchedulePolicyObject nesnesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d312-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d312-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d312-132">-Confirm</span></span>
<span data-ttu-id="6d312-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d312-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d312-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d312-134">-WhatIf</span></span>
<span data-ttu-id="6d312-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d312-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d312-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d312-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d312-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d312-137">CommonParameters</span></span>
<span data-ttu-id="6d312-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d312-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d312-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d312-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d312-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d312-140">INPUTS</span></span>

### <span data-ttu-id="6d312-141">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6d312-141">PolicyBase</span></span>
<span data-ttu-id="6d312-142">Parametre ' Ilke ', ardışık düzenin ' PolicyBase ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6d312-142">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="6d312-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d312-143">OUTPUTS</span></span>

### <span data-ttu-id="6d312-144">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. JobBase]</span><span class="sxs-lookup"><span data-stu-id="6d312-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="6d312-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d312-145">NOTES</span></span>

## <span data-ttu-id="6d312-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d312-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d312-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d312-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6d312-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6d312-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="6d312-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d312-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6d312-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d312-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


