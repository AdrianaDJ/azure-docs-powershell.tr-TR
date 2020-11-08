---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106208"
---
# <span data-ttu-id="9e50a-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9e50a-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="9e50a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e50a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e50a-103">Yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e50a-103">Creates a backup policy.</span></span>

## <span data-ttu-id="9e50a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e50a-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e50a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e50a-105">DESCRIPTION</span></span>
<span data-ttu-id="9e50a-106">**New-AzureStorSimpleDeviceBackupPolicy** cmdlet 'i bir yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e50a-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="9e50a-107">Yedekleme ilkesi, bir veya daha fazla birimde çalıştırılabilecek bir veya daha fazla yedekleme zamanlaması içerir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="9e50a-108">Yedekleme zamanlaması oluşturmak için, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9e50a-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="9e50a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e50a-109">EXAMPLES</span></span>

### <span data-ttu-id="9e50a-110">Örnek 1: yedekleme ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9e50a-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="9e50a-111">İlk komut, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ini kullanarak bir yedekleme zamanlama yapılandırması nesnesi oluşturur ve bu nesneyi $Schedule 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e50a-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="9e50a-112">İkinci komut, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** kullanarak başka bir yedek yapılandırma nesnesi oluşturur ve bu nesneyi $Schedule 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e50a-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="9e50a-113">Üçüncü komut, $ScheduleArray adlı boş bir dizi değişkeni oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e50a-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="9e50a-114">Sonraki iki komut $ScheduleArray için ilk iki komuttan oluşturulan nesneleri ekler.</span><span class="sxs-lookup"><span data-stu-id="9e50a-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="9e50a-115">Altıncı komut, **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanarak Contoso63-AppVm adlı aygıtın birim kapsayıcısını alır ve bu kapsayıcı nesnesini $DeviceContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e50a-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="9e50a-116">Yedinci komutu, **Get-AzureStorSimpleDeviceVolume** cmdlet 'ini kullanarak $DeviceContainer ilk üyesinde depolanan birim kapsayıcısının birimini alır ve bu birimi $Volume değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e50a-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="9e50a-117">Sekizinci komutu, $VolumeArray adlı boş bir dizi değişkeni oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e50a-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="9e50a-118">Next komutu $VolumeArray için bir birim KIMLIĞI ekler.</span><span class="sxs-lookup"><span data-stu-id="9e50a-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="9e50a-119">Bu değer, yedekleme ilkesinin çalıştığı $Volume depolanan birimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9e50a-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="9e50a-120">$VolumeArray ek birim kimlikleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e50a-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="9e50a-121">Son komutu Contoso63-AppVm adlı cihaz için GeneralPolicy07 adlı yedekleme ilkesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e50a-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="9e50a-122">Komut, $ScheduleArray depolanan zamanlama yapılandırması nesnelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="9e50a-123">Komut $VolumeArray ilkenin uygulanacağı birim veya birimleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="9e50a-124">**Get-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak yedekleme ilkesini doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e50a-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="9e50a-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e50a-125">PARAMETERS</span></span>

### <span data-ttu-id="9e50a-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="9e50a-126">-BackupPolicyName</span></span>
<span data-ttu-id="9e50a-127">Yedekleme ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="9e50a-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="9e50a-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="9e50a-129">İlkeye eklenecek **Backupschedulebase** nesnelerinin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="9e50a-130">Her nesne bir zamanlamayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="9e50a-130">Each object represents a schedule.</span></span>
<span data-ttu-id="9e50a-131">Yedekleme ilkesi, bir veya daha fazla zamanlama içerir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="9e50a-132">**Backupschedulebase** nesnesi edinmek Için, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9e50a-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e50a-133">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="9e50a-133">-DeviceName</span></span>
<span data-ttu-id="9e50a-134">Yedekleme ilkesinin oluşturulacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="9e50a-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="9e50a-135">-Profile</span></span>
<span data-ttu-id="9e50a-136">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9e50a-137">-Volumeıdstoadd</span><span class="sxs-lookup"><span data-stu-id="9e50a-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="9e50a-138">Yedekleme ilkesine eklenecek birimlerin kimliklerinin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e50a-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9e50a-139">-WaitForComplete</span></span>
<span data-ttu-id="9e50a-140">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e50a-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="9e50a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e50a-141">CommonParameters</span></span>
<span data-ttu-id="9e50a-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e50a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e50a-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e50a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e50a-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e50a-144">INPUTS</span></span>

### <span data-ttu-id="9e50a-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9e50a-145">None</span></span>

## <span data-ttu-id="9e50a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e50a-146">OUTPUTS</span></span>

### <span data-ttu-id="9e50a-147">Yedeklemeilkesi</span><span class="sxs-lookup"><span data-stu-id="9e50a-147">BackupPolicy</span></span>
<span data-ttu-id="9e50a-148">Bu cmdlet, yeni zamanlamaları ve birimleri içeren bir **Backuppolicy** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e50a-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="9e50a-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e50a-149">NOTES</span></span>

## <span data-ttu-id="9e50a-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e50a-150">RELATED LINKS</span></span>

[<span data-ttu-id="9e50a-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9e50a-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9e50a-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9e50a-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9e50a-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9e50a-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="9e50a-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9e50a-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9e50a-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9e50a-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9e50a-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="9e50a-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


