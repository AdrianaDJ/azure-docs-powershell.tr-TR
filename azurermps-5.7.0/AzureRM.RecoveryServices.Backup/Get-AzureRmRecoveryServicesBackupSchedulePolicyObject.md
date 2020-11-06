---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 4a3602363436c396b0706d9c195569874a35fdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587487"
---
# <span data-ttu-id="e8799-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="e8799-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="e8799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8799-102">SYNOPSIS</span></span>
<span data-ttu-id="e8799-103">Temel bir zamanlama İlkesi nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="e8799-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8799-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8799-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8799-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8799-105">DESCRIPTION</span></span>
<span data-ttu-id="e8799-106">**Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet 'ini bir temel **Azurermrecoveryservicesschedulepolicyobject** alır.</span><span class="sxs-lookup"><span data-stu-id="e8799-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="e8799-107">Bu nesne sistemde kalıcı değil.</span><span class="sxs-lookup"><span data-stu-id="e8799-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="e8799-108">Bu, yeni yedekleme koruma ilkesi oluşturmak için New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'i işleyebileceğiniz ve kullanabileceğiniz geçici bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="e8799-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="e8799-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8799-109">EXAMPLES</span></span>

### <span data-ttu-id="e8799-110">Örnek 1: zamanlama frekansını haftalık olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="e8799-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e8799-111">İlk komut bekletme ilkesi nesnesini alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e8799-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="e8799-112">İkinci komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e8799-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="e8799-113">Üçüncü komut zamanlama İlkesi sıklığını haftalık olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e8799-113">The third command changes the frequency for the schedule policy to weekly.</span></span>

<span data-ttu-id="e8799-114">Son komut, güncelleştirilmiş zamanlamaya sahip yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8799-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="e8799-115">Örnek 2: yedekleme süresini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e8799-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e8799-116">İlk komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e8799-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="e8799-117">İkinci komut $SchPol tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e8799-117">The second command removes all scheduled run times from $SchPol.</span></span>

<span data-ttu-id="e8799-118">Üçüncü komut geçerli tarih ve saati alır ve $DT değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e8799-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="e8799-119">Dördüncü komut zamanlanmış çalışma saatlerini geçerli saat ile değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e8799-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="e8799-120">Günde yalnızca bir kez AzureVM, yedekleme süresini sıfırlamak için özgün zamanlamayı değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e8799-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>

<span data-ttu-id="e8799-121">Son komut yeni zamanlamayı kullanarak yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8799-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="e8799-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8799-122">PARAMETERS</span></span>

### <span data-ttu-id="e8799-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e8799-123">-BackupManagementType</span></span>
<span data-ttu-id="e8799-124">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8799-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="e8799-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e8799-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8799-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e8799-126">AzureVM</span></span> 
- <span data-ttu-id="e8799-127">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="e8799-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8799-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8799-128">-DefaultProfile</span></span>
<span data-ttu-id="e8799-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8799-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8799-130">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e8799-130">-WorkloadType</span></span>
<span data-ttu-id="e8799-131">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8799-131">Specifies the workload type.</span></span>
<span data-ttu-id="e8799-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e8799-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8799-133">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e8799-133">AzureVM</span></span> 
- <span data-ttu-id="e8799-134">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="e8799-134">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8799-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8799-135">CommonParameters</span></span>
<span data-ttu-id="e8799-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8799-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8799-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8799-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8799-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8799-138">INPUTS</span></span>

### <span data-ttu-id="e8799-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e8799-139">None</span></span>
<span data-ttu-id="e8799-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e8799-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8799-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8799-141">OUTPUTS</span></span>

### <span data-ttu-id="e8799-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="e8799-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="e8799-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8799-143">NOTES</span></span>

## <span data-ttu-id="e8799-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8799-144">RELATED LINKS</span></span>

[<span data-ttu-id="e8799-145">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8799-145">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e8799-146">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8799-146">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


