---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106290"
---
# <span data-ttu-id="bf13e-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="bf13e-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="bf13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf13e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf13e-103">Bir cihazdan yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-103">Gets backups from a device.</span></span>

## <span data-ttu-id="bf13e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf13e-104">SYNTAX</span></span>

### <span data-ttu-id="bf13e-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf13e-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bf13e-106">Identifybyıd</span><span class="sxs-lookup"><span data-stu-id="bf13e-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bf13e-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="bf13e-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bf13e-108">Identifybyobject</span><span class="sxs-lookup"><span data-stu-id="bf13e-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bf13e-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="bf13e-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf13e-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf13e-110">DESCRIPTION</span></span>
<span data-ttu-id="bf13e-111">**Get-AzureStorSimpleDeviceBackup** cmdlet 'i bir cihazdan yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="bf13e-112">Yedekler için yedekleme ilkesi, hacim ve oluşturulma zamanını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf13e-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="bf13e-113">Bu cmdlet ilk sayfada maksimum 100 yedeği döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="bf13e-114">100 yedekleri varsa, *ilk* ve *Atla* parametrelerini kullanarak sonraki sayfaları alın.</span><span class="sxs-lookup"><span data-stu-id="bf13e-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="bf13e-115">*İlk* olarak *Atla* ve 50 için 100 değerini belirtirseniz, bu cmdlet ilk 100 sonucunu döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bf13e-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="bf13e-116">Bu, atlan100 dıktan sonraki 50 sonuçlarının sonraki sonucunu verir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="bf13e-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf13e-117">EXAMPLES</span></span>

### <span data-ttu-id="bf13e-118">Örnek 1: aygıttaki tüm yedekleri alma</span><span class="sxs-lookup"><span data-stu-id="bf13e-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="bf13e-119">Bu komut, Contoso63-AppVm adlı cihazda bulunan tüm yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="bf13e-120">İlk sayfa için izin verilen maksimum 100 yedeğinden daha fazlası varsa, *ilkini* kullanarak ek sonuçları görüntüleyin. *Skip*</span><span class="sxs-lookup"><span data-stu-id="bf13e-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="bf13e-121">Örnek 2: iki tarih arasındaki yedekleri alma</span><span class="sxs-lookup"><span data-stu-id="bf13e-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="bf13e-122">Bu komut, 10/7/2014 tarihinde veya bu tarihten sonra veya 10/8/2014 tarihinde oluşturulan Contoso63-AppVm adlı cihazda yedeklemeler alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="bf13e-123">Bu cmdlet ilk sonucu atlar ve ilk iki sonucun ilk sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf13e-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="bf13e-124">*İlk* için değerleri değiştirin ve diğer sonuçları görüntülemek için *atlayın* .</span><span class="sxs-lookup"><span data-stu-id="bf13e-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="bf13e-125">Örnek 3: yedekleme ilkesi KIMLIĞI için yedeklemeler alma</span><span class="sxs-lookup"><span data-stu-id="bf13e-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="bf13e-126">Bu komut, oluşturma Contoso63-AppVm belirtilen tarihte veya daha önce oluşturulan cihazda yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="bf13e-127">Komut, belirtilen KIMLIĞE sahip yedekleme ilkesi kullanılarak oluşturulmuş yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="bf13e-128">Bu komut *ilk* parametreyi belirtir, dolayısıyla yalnızca ilk 10 sonucu verir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="bf13e-129">Örnek 4: yedekleme ilkesi nesnesini yedekleme</span><span class="sxs-lookup"><span data-stu-id="bf13e-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="bf13e-130">Bu komut **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak bir **backuppolicydetails** nesnesi alır ve bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf13e-131">Bu cmdlet, komutun ilk bölümündeki yedekleme ilkesi kullanılarak oluşturulan Contoso63-AppVm adlı cihaz için yedeklemeler alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="bf13e-132">Komut, önceki örnekte olduğu gibi, belirtilen tarihte veya belirtilen tarihte oluşturulmuş yedekleri alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="bf13e-133">Bu komut yalnızca ilk 10 sonucu döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf13e-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="bf13e-134">Örnek 5: birim KIMLIĞI için yedekleme edinme</span><span class="sxs-lookup"><span data-stu-id="bf13e-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="bf13e-135">Bu komut, belirtilen örnek KIMLIĞINE sahip olan birimde oluşturulan cihazda bir yedekleme alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="bf13e-136">Bu komut *Birinci* parametreyi belirtir, dolayısıyla yalnızca ilk sonucu verir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="bf13e-137">Örnek 6: birim adı için yedekleme edinme</span><span class="sxs-lookup"><span data-stu-id="bf13e-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="bf13e-138">Bu komut, **Get-AzureStorSimpleDeviceVolume** cmdlet 'ini kullanarak bir **VirtualDisk** nesnesi alır ve bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf13e-139">Bu cmdlet, komutun ilk bölümünden birimde oluşturulan Contoso63-AppVm adlı cihaz için yedeklemeler alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="bf13e-140">Bu komut yalnızca ilk sonucu döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf13e-140">This command returns only the first result.</span></span>

## <span data-ttu-id="bf13e-141">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf13e-141">PARAMETERS</span></span>

### <span data-ttu-id="bf13e-142">-Yedeklemekuralı</span><span class="sxs-lookup"><span data-stu-id="bf13e-142">-BackupPolicy</span></span>
<span data-ttu-id="bf13e-143">**Backuppolicydetails** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="bf13e-144">Bu cmdlet, hangi yedeklemelerin alınacağını belirlemek için bu nesnenin **InstanceId** 'yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="bf13e-145">**Backuppolicydetails** nesnesini edinmek için **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf13e-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13e-146">-Backuppolicyıd</span><span class="sxs-lookup"><span data-stu-id="bf13e-146">-BackupPolicyId</span></span>
<span data-ttu-id="bf13e-147">Yedekleme ilkesinin örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="bf13e-148">Bu cmdlet, bu parametrenin belirttiği ilkeye ait cihaz yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf13e-149">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="bf13e-149">-DeviceName</span></span>
<span data-ttu-id="bf13e-150">Yedeklemelerin alınacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

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

### <span data-ttu-id="bf13e-151">-Önce</span><span class="sxs-lookup"><span data-stu-id="bf13e-151">-First</span></span>
<span data-ttu-id="bf13e-152">Yalnızca belirtilen sayıda nesneyi alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="bf13e-153">Alınacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="bf13e-153">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf13e-154">'Den</span><span class="sxs-lookup"><span data-stu-id="bf13e-154">-From</span></span>
<span data-ttu-id="bf13e-155">Bu cmdlet 'in aldığı yedeklemelerin başlangıç tarihini ve saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf13e-156">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf13e-156">-Profile</span></span>
<span data-ttu-id="bf13e-157">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bf13e-158">-Atla</span><span class="sxs-lookup"><span data-stu-id="bf13e-158">-Skip</span></span>
<span data-ttu-id="bf13e-159">Belirtilen sayıda nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="bf13e-160">Atlanacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="bf13e-160">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf13e-161">-To</span><span class="sxs-lookup"><span data-stu-id="bf13e-161">-To</span></span>
<span data-ttu-id="bf13e-162">Bu cmdlet 'in aldığı yedeklemelerin bitiş tarihini ve saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf13e-163">-Hacim</span><span class="sxs-lookup"><span data-stu-id="bf13e-163">-Volume</span></span>
<span data-ttu-id="bf13e-164">**VirtualDisk** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="bf13e-165">Bu cmdlet, yedeklemelerin olduğu birimi belirlemek için bu nesnenin **InstanceId** 'si kullanır.</span><span class="sxs-lookup"><span data-stu-id="bf13e-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="bf13e-166">**VirtualDisk** nesnesi edinmek için **Get-AzureStorSimpleDeviceVolume** parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf13e-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13e-167">-VolumeId</span><span class="sxs-lookup"><span data-stu-id="bf13e-167">-VolumeId</span></span>
<span data-ttu-id="bf13e-168">Yedeklemelerin olduğu birimin örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf13e-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf13e-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf13e-169">CommonParameters</span></span>
<span data-ttu-id="bf13e-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf13e-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf13e-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf13e-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf13e-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf13e-172">INPUTS</span></span>

### <span data-ttu-id="bf13e-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="bf13e-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="bf13e-174">Bu cmdlet **Backuppolicydetails** ve **VirtualDisk** nesnelerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="bf13e-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="bf13e-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf13e-175">OUTPUTS</span></span>

### <span data-ttu-id="bf13e-176">'Te\<Backup\></span><span class="sxs-lookup"><span data-stu-id="bf13e-176">IList\<Backup\></span></span>
<span data-ttu-id="bf13e-177">Bu cmdlet, **yedekleme** nesnelerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf13e-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="bf13e-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf13e-178">NOTES</span></span>

## <span data-ttu-id="bf13e-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf13e-179">RELATED LINKS</span></span>

[<span data-ttu-id="bf13e-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="bf13e-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="bf13e-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bf13e-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="bf13e-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="bf13e-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


