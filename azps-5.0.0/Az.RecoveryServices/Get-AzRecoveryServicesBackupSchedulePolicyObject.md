---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275707"
---
# <span data-ttu-id="87688-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="87688-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="87688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87688-102">SYNOPSIS</span></span>
<span data-ttu-id="87688-103">Temel bir zamanlama İlkesi nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="87688-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="87688-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87688-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87688-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87688-105">DESCRIPTION</span></span>
<span data-ttu-id="87688-106">**Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet 'i bir Base **Azurermrecoveryservicesschedulepolicyobject** alır.</span><span class="sxs-lookup"><span data-stu-id="87688-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="87688-107">Bu nesne sistemde kalıcı değil.</span><span class="sxs-lookup"><span data-stu-id="87688-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="87688-108">Bu, yeni yedekleme koruma ilkesi oluşturmak için New-AzRecoveryServicesBackupProtectionPolicy cmdlet 'i işleyebileceğiniz ve kullanabileceğiniz geçici bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="87688-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="87688-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87688-109">EXAMPLES</span></span>

### <span data-ttu-id="87688-110">Örnek 1: zamanlama frekansını haftalık olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="87688-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="87688-111">İlk komut bekletme ilkesi nesnesini alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87688-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="87688-112">İkinci komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87688-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="87688-113">Üçüncü komut zamanlama İlkesi sıklığını haftalık olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="87688-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="87688-114">Son komut, güncelleştirilmiş zamanlamaya sahip yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87688-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="87688-115">Örnek 2: yedekleme süresini ayarlama</span><span class="sxs-lookup"><span data-stu-id="87688-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="87688-116">İlk komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87688-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="87688-117">İkinci komut $SchPol tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87688-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="87688-118">Üçüncü komut geçerli tarih ve saati alır ve $DT değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87688-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="87688-119">Dördüncü komut zamanlanmış çalışma saatlerini geçerli saat ile değiştirir.</span><span class="sxs-lookup"><span data-stu-id="87688-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="87688-120">Günde yalnızca bir kez AzureVM, yedekleme süresini sıfırlamak için özgün zamanlamayı değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="87688-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="87688-121">Son komut yeni zamanlamayı kullanarak yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87688-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="87688-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87688-122">PARAMETERS</span></span>

### <span data-ttu-id="87688-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="87688-123">-BackupManagementType</span></span>
<span data-ttu-id="87688-124">Korunan kaynakların sınıfı.</span><span class="sxs-lookup"><span data-stu-id="87688-124">The class of resources being protected.</span></span> <span data-ttu-id="87688-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="87688-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87688-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="87688-126">AzureVM</span></span> 
- <span data-ttu-id="87688-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="87688-127">AzureStorage</span></span>
- <span data-ttu-id="87688-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="87688-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87688-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87688-129">-DefaultProfile</span></span>
<span data-ttu-id="87688-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87688-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87688-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="87688-131">-WorkloadType</span></span>
<span data-ttu-id="87688-132">Kaynağın iş yükü türü.</span><span class="sxs-lookup"><span data-stu-id="87688-132">Workload type of the resource.</span></span> <span data-ttu-id="87688-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="87688-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87688-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="87688-134">AzureVM</span></span> 
- <span data-ttu-id="87688-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="87688-135">AzureFiles</span></span>
- <span data-ttu-id="87688-136">KLASÖRÜNÜN</span><span class="sxs-lookup"><span data-stu-id="87688-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87688-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87688-137">CommonParameters</span></span>
<span data-ttu-id="87688-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87688-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87688-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="87688-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87688-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87688-140">INPUTS</span></span>

### <span data-ttu-id="87688-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="87688-141">None</span></span>

## <span data-ttu-id="87688-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87688-142">OUTPUTS</span></span>

### <span data-ttu-id="87688-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="87688-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="87688-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87688-144">NOTES</span></span>

## <span data-ttu-id="87688-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87688-145">RELATED LINKS</span></span>

[<span data-ttu-id="87688-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="87688-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="87688-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="87688-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


