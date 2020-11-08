---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105852"
---
# <span data-ttu-id="8bcdc-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcdc-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="8bcdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bcdc-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcdc-103">Var olan bir yedekleme ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="8bcdc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bcdc-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8bcdc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bcdc-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcdc-106">**Set-AzureStorSimpleDeviceBackupPolicy** cmdlet 'i var olan bir yedekleme ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="8bcdc-107">İlkeyi yeniden adlandırabilir, zamanlama ekleyebilir, güncelleştirebilir veya silebilir ve ilkeyle ilişkili birimleri güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="8bcdc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bcdc-108">EXAMPLES</span></span>

### <span data-ttu-id="8bcdc-109">Örnek 1: yedekleme ilkesinin adını değiştirme</span><span class="sxs-lookup"><span data-stu-id="8bcdc-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="8bcdc-110">Bu komut, belirtilen KIMLIĞI UpdatedGeneralPolicy07 olan yedekleme ilkesinin adını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="8bcdc-111">Bu komut *Waitforcomplete* parametresini belirtir; böylece komut görevi tamamlar ve görev Için bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="8bcdc-112">Örnek 2: yedekleme ilkesi zamanlamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8bcdc-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="8bcdc-113">İlk komut, **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet 'ini kullanarak bir güncelleştirme yapılandırma nesnesi oluşturur ve bunu $UpdateConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="8bcdc-114">İkinci komut, $UpdateArray adlı yeni bir dizi değişkeni oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="8bcdc-115">Next komutu $UpdateConfig 'de depolanan güncelleştirmeyi bu diziye ekler.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="8bcdc-116">Diziye birden fazla güncelleştirme ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="8bcdc-117">Son komut, Contoso63-AppVm adlı aygıtta belirtilen KIMLIĞE sahip yedekleme ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="8bcdc-118">İlkede artık $UpdateArray depolanan güncelleştirilmiş zamanlama vardır.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="8bcdc-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bcdc-119">PARAMETERS</span></span>

### <span data-ttu-id="8bcdc-120">-Backuppolicyıd</span><span class="sxs-lookup"><span data-stu-id="8bcdc-120">-BackupPolicyId</span></span>
<span data-ttu-id="8bcdc-121">Güncelleştirilecek **Backuppolicy** NESNESININ örnek kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="8bcdc-122">-BackupPolicyName</span></span>
<span data-ttu-id="8bcdc-123">Yedekleme ilkesi için yeni bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-123">Specifies a new name for the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-124">-Backupscheduleıdstodelete</span><span class="sxs-lookup"><span data-stu-id="8bcdc-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="8bcdc-125">Silinecek **Backupzamanlama** nesnelerinin örnek kimliklerinin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="8bcdc-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="8bcdc-127">İlkeye eklenecek **Backupschedulebase** nesnelerinin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="8bcdc-128">**Backupschedulebase** nesnesi edinmek Için, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="8bcdc-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="8bcdc-130">Güncelleştirilecek bir **yedekleme Scheduleupdaterequest** nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="8bcdc-131">**Backupscheduleupdaterequest** nesnesi edinmek Için, **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-132">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="8bcdc-132">-DeviceName</span></span>
<span data-ttu-id="8bcdc-133">Yedekleme ilkesi güncelleştirilecek StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="8bcdc-134">-NewName</span></span>
<span data-ttu-id="8bcdc-135">Cihaz için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-135">Specifies a name for the device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="8bcdc-136">-Profile</span></span>
<span data-ttu-id="8bcdc-137">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-137">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-138">-Volumeıdstoupdate</span><span class="sxs-lookup"><span data-stu-id="8bcdc-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="8bcdc-139">Yedekleme ilkelerinin güncelleştirilebilecek birim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8bcdc-140">-WaitForComplete</span></span>
<span data-ttu-id="8bcdc-141">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcdc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcdc-142">CommonParameters</span></span>
<span data-ttu-id="8bcdc-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcdc-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bcdc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcdc-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bcdc-145">INPUTS</span></span>

### <span data-ttu-id="8bcdc-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8bcdc-146">None</span></span>

## <span data-ttu-id="8bcdc-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bcdc-147">OUTPUTS</span></span>

### <span data-ttu-id="8bcdc-148">Taskstatusınfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="8bcdc-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="8bcdc-149">*Waitforcomplete* parametresini belirtirseniz, bu cmdlet bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="8bcdc-150">Bu parametreyi belirtmezseniz, bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bcdc-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="8bcdc-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bcdc-151">NOTES</span></span>

## <span data-ttu-id="8bcdc-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bcdc-152">RELATED LINKS</span></span>

[<span data-ttu-id="8bcdc-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcdc-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="8bcdc-154">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcdc-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="8bcdc-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8bcdc-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="8bcdc-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="8bcdc-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


