---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759685"
---
# <span data-ttu-id="1fd61-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="1fd61-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="1fd61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fd61-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd61-103">Temel bir zamanlama İlkesi nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="1fd61-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="1fd61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fd61-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fd61-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fd61-105">DESCRIPTION</span></span>
<span data-ttu-id="1fd61-106">**Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet 'i bir Base **Azurermrecoveryservicesschedulepolicyobject** alır.</span><span class="sxs-lookup"><span data-stu-id="1fd61-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="1fd61-107">Bu nesne sistemde kalıcı değil.</span><span class="sxs-lookup"><span data-stu-id="1fd61-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="1fd61-108">Bu, yeni yedekleme koruma ilkesi oluşturmak için New-AzRecoveryServicesBackupProtectionPolicy cmdlet 'i işleyebileceğiniz ve kullanabileceğiniz geçici bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="1fd61-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="1fd61-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fd61-109">EXAMPLES</span></span>

### <span data-ttu-id="1fd61-110">Örnek 1: zamanlama frekansını haftalık olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="1fd61-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="1fd61-111">İlk komut bekletme ilkesi nesnesini alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1fd61-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="1fd61-112">İkinci komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1fd61-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="1fd61-113">Üçüncü komut zamanlama İlkesi sıklığını haftalık olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1fd61-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="1fd61-114">Son komut, güncelleştirilmiş zamanlamaya sahip yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fd61-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="1fd61-115">Örnek 2: yedekleme süresini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1fd61-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="1fd61-116">İlk komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1fd61-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="1fd61-117">İkinci komut $SchPol tüm zamanlanmış çalışma zamanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1fd61-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="1fd61-118">Üçüncü komut geçerli tarih ve saati alır ve $DT değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1fd61-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="1fd61-119">Dördüncü komut zamanlanmış çalışma saatlerini geçerli saat ile değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1fd61-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="1fd61-120">Günde yalnızca bir kez AzureVM, yedekleme süresini sıfırlamak için özgün zamanlamayı değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1fd61-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="1fd61-121">Son komut yeni zamanlamayı kullanarak yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fd61-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="1fd61-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fd61-122">PARAMETERS</span></span>

### <span data-ttu-id="1fd61-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1fd61-123">-BackupManagementType</span></span>
<span data-ttu-id="1fd61-124">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fd61-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="1fd61-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1fd61-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1fd61-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1fd61-126">AzureVM</span></span> 
- <span data-ttu-id="1fd61-127">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="1fd61-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="1fd61-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="1fd61-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd61-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd61-129">-DefaultProfile</span></span>
<span data-ttu-id="1fd61-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fd61-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fd61-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1fd61-131">-WorkloadType</span></span>
<span data-ttu-id="1fd61-132">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fd61-132">Specifies the workload type.</span></span>
<span data-ttu-id="1fd61-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1fd61-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1fd61-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1fd61-134">AzureVM</span></span> 
- <span data-ttu-id="1fd61-135">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="1fd61-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="1fd61-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="1fd61-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd61-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd61-137">CommonParameters</span></span>
<span data-ttu-id="1fd61-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fd61-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd61-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd61-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd61-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fd61-140">INPUTS</span></span>

### <span data-ttu-id="1fd61-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1fd61-141">None</span></span>

## <span data-ttu-id="1fd61-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fd61-142">OUTPUTS</span></span>

### <span data-ttu-id="1fd61-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="1fd61-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="1fd61-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fd61-144">NOTES</span></span>

## <span data-ttu-id="1fd61-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fd61-145">RELATED LINKS</span></span>

[<span data-ttu-id="1fd61-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fd61-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1fd61-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fd61-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


