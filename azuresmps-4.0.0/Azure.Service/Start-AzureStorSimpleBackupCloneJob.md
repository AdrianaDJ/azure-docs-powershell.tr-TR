---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105748"
---
# <span data-ttu-id="b55d8-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="b55d8-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="b55d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b55d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b55d8-103">Bir cihazda yedeklemeyi klonuygulayan bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="b55d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b55d8-104">SYNTAX</span></span>

### <span data-ttu-id="b55d8-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b55d8-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b55d8-106">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="b55d8-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b55d8-107">Identifybyıd</span><span class="sxs-lookup"><span data-stu-id="b55d8-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b55d8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b55d8-108">DESCRIPTION</span></span>
<span data-ttu-id="b55d8-109">**Start-AzureStorSimpleBackupCloneJob** cmdlet 'ı StorSimple cihazında var olan bir yedeği klonuygulayan bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="b55d8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b55d8-110">EXAMPLES</span></span>

### <span data-ttu-id="b55d8-111">Örnek 1: cihaz adlarını kullanarak yedeği farklı bir birime kopyalama</span><span class="sxs-lookup"><span data-stu-id="b55d8-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="b55d8-112">İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="b55d8-113">Komut bu yedeği $Backup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="b55d8-114">İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="b55d8-115">Komut sonucu $Acrs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="b55d8-116">Son komut, bir birimdeki bir birimin belirtilen yedeğini aynı cihazdaki farklı bir birime klonuygulayan bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="b55d8-117">Bu örnek, cihazı adıyla belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-117">This example specifies the device by name.</span></span>
<span data-ttu-id="b55d8-118">Komut, $Backup ve $Acrs depolanan değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="b55d8-119">Komut işin KIMLIĞINI döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55d8-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="b55d8-120">Örnek 2: cihaz kimliklerini kullanarak yedeği farklı bir birime kopyalama</span><span class="sxs-lookup"><span data-stu-id="b55d8-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="b55d8-121">İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="b55d8-122">Komut bu yedeği $Backup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="b55d8-123">İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="b55d8-124">Komut sonucu $Acrs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="b55d8-125">Son komut, bir birimdeki bir birimin belirtilen yedeğini aynı cihazdaki farklı bir birime klonuygulayan bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="b55d8-126">Bu örnekte cihazı cihaz KIMLIĞIYLE belirtilir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="b55d8-127">Komut, $Backup ve $Acrs depolanan değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="b55d8-128">Komut işin KIMLIĞINI döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55d8-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="b55d8-129">Örnek 3: cihaz adlarını kullanarak yedeği farklı bir cihazda bir birime kopyalama</span><span class="sxs-lookup"><span data-stu-id="b55d8-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="b55d8-130">İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="b55d8-131">Komut bu yedeği $Backup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="b55d8-132">İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="b55d8-133">Komut sonucu $Acrs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="b55d8-134">Son komutu, bir birimdeki bir birimin belirtilen yedeğini farklı bir aygıttaki birime klonuygulayan bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="b55d8-135">Bu örnekte, cihazlar ada göre belirtilir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="b55d8-136">Komut, $Backup ve $Acrs depolanan değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="b55d8-137">Komut işin KIMLIĞINI döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55d8-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="b55d8-138">Örnek 4: cihaz adlarını ve ardışık düzen işlecini kullanarak yedeği farklı bir birime kopyalama</span><span class="sxs-lookup"><span data-stu-id="b55d8-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="b55d8-139">İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="b55d8-140">Komut bu yedeği $Backup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="b55d8-141">İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="b55d8-142">Komut sonuçları ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b55d8-143">Geçerli cmdlet, bir aygıttaki bir birimin belirtilen yedeğini aynı cihazdaki farklı bir birime klonuygulayan bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="b55d8-144">Bu örnek, cihazı adıyla belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-144">This example specifies the device by name.</span></span>
<span data-ttu-id="b55d8-145">Komutta $Backup depolanan değer kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="b55d8-146">Komut, ardışık düzenin *Targetaccesscontrolrecords* parametresinin değerini alır.</span><span class="sxs-lookup"><span data-stu-id="b55d8-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="b55d8-147">Komut işin KIMLIĞINI döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55d8-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="b55d8-148">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b55d8-148">PARAMETERS</span></span>

### <span data-ttu-id="b55d8-149">-BackupID</span><span class="sxs-lookup"><span data-stu-id="b55d8-149">-BackupId</span></span>
<span data-ttu-id="b55d8-150">Kopya oluşturulacak yedeğin örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="b55d8-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="b55d8-151">-CloneVolumeName</span></span>
<span data-ttu-id="b55d8-152">Hedef aygıttaki yeni kopyalanmış birimin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="b55d8-153">-Force</span><span class="sxs-lookup"><span data-stu-id="b55d8-153">-Force</span></span>
<span data-ttu-id="b55d8-154">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b55d8-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b55d8-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="b55d8-155">-Profile</span></span>
<span data-ttu-id="b55d8-156">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b55d8-157">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="b55d8-157">-Snapshot</span></span>
<span data-ttu-id="b55d8-158">Bu cmdlet 'in klonkullandığı anlık görüntü nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b55d8-159">-Sourcedeviceıd</span><span class="sxs-lookup"><span data-stu-id="b55d8-159">-SourceDeviceId</span></span>
<span data-ttu-id="b55d8-160">Kaynak aygıtın örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="b55d8-161">Bu cmdlet, kaynak cihazdan geri döner.</span><span class="sxs-lookup"><span data-stu-id="b55d8-161">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55d8-162">-Sourceaygıtadı</span><span class="sxs-lookup"><span data-stu-id="b55d8-162">-SourceDeviceName</span></span>
<span data-ttu-id="b55d8-163">Kaynak aygıtın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="b55d8-164">Bu cmdlet, kaynak cihazdan geri döner.</span><span class="sxs-lookup"><span data-stu-id="b55d8-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55d8-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="b55d8-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="b55d8-166">Erişim denetimi kayıtlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b55d8-167">-Targetdeviceıd</span><span class="sxs-lookup"><span data-stu-id="b55d8-167">-TargetDeviceId</span></span>
<span data-ttu-id="b55d8-168">Hedef aygıtın örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-168">Specifies the instance ID of the target device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55d8-169">-Targetaygıtadı</span><span class="sxs-lookup"><span data-stu-id="b55d8-169">-TargetDeviceName</span></span>
<span data-ttu-id="b55d8-170">Bu cmdlet 'in yedeği klondıkları aygıtın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55d8-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55d8-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55d8-171">CommonParameters</span></span>
<span data-ttu-id="b55d8-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b55d8-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55d8-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b55d8-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55d8-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b55d8-174">INPUTS</span></span>

### <span data-ttu-id="b55d8-175">Anlık görüntü, AccessControlRecord listesi</span><span class="sxs-lookup"><span data-stu-id="b55d8-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="b55d8-176">**Anlık görüntü** nesnelerini veya **accesscontrolrecord** nesnelerinin listesini bu cmdlet 'e boru yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b55d8-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="b55d8-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b55d8-177">OUTPUTS</span></span>

## <span data-ttu-id="b55d8-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b55d8-178">NOTES</span></span>

## <span data-ttu-id="b55d8-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b55d8-179">RELATED LINKS</span></span>

[<span data-ttu-id="b55d8-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="b55d8-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="b55d8-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b55d8-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


