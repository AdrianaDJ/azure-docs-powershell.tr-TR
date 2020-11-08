---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105558"
---
# <span data-ttu-id="44814-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="44814-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="44814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44814-102">SYNOPSIS</span></span>
<span data-ttu-id="44814-103">StorSimple işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="44814-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="44814-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44814-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="44814-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="44814-105">DESCRIPTION</span></span>
<span data-ttu-id="44814-106">**Get-AzureStorSimpleJob** cmdlet 'ı Azure StorSimple işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="44814-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="44814-107">Belirli bir iş almak için bir örnek KIMLIĞI belirtin.</span><span class="sxs-lookup"><span data-stu-id="44814-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="44814-108">Bu cmdlet 'in aldığı işleri sınırlandırmak için diğer parametreleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="44814-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="44814-109">Bu cmdlet en çok 200 işi döndürür.</span><span class="sxs-lookup"><span data-stu-id="44814-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="44814-110">200 'den fazla işi varsa, *ilk* ve *Atla* parametrelerini kullanarak kalan işleri alın.</span><span class="sxs-lookup"><span data-stu-id="44814-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="44814-111">*İlk* olarak *Atla* ve 50 için 100 değerini belirtirseniz, bu cmdlet ilk 100 sonucunu döndürmez.</span><span class="sxs-lookup"><span data-stu-id="44814-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="44814-112">Bu, atlan100 dıktan sonraki 50 sonuçlarının sonraki sonucunu verir.</span><span class="sxs-lookup"><span data-stu-id="44814-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="44814-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44814-113">EXAMPLES</span></span>

### <span data-ttu-id="44814-114">Örnek 1: KIMLIK kullanarak iş alma</span><span class="sxs-lookup"><span data-stu-id="44814-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="44814-115">Bu komut, belirtilen KIMLIĞE sahip olan iş için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="44814-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="44814-116">Örnek 2: bir cihaz adı kullanarak işleri alma</span><span class="sxs-lookup"><span data-stu-id="44814-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="44814-117">Bu komut, 8600-Bravo 001 adlı aygıttaki işlerle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="44814-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="44814-118">Komut, aygıtın ilk iki işini alır.</span><span class="sxs-lookup"><span data-stu-id="44814-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="44814-119">Örnek 3: tamamlanan işleri alma</span><span class="sxs-lookup"><span data-stu-id="44814-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="44814-120">Bu komut tamamlanmış işleri alır.</span><span class="sxs-lookup"><span data-stu-id="44814-120">This command gets completed jobs.</span></span>
<span data-ttu-id="44814-121">Komut ilk on işi atladıktan sonra yalnızca ilk iki işi alır.</span><span class="sxs-lookup"><span data-stu-id="44814-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="44814-122">Örnek 4: elle yedekleme işleri edinme</span><span class="sxs-lookup"><span data-stu-id="44814-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="44814-123">Bu komut, el ile yedekleme türündeki işleri alır.</span><span class="sxs-lookup"><span data-stu-id="44814-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="44814-124">Örnek 5: belirtilen saatler arasındaki işleri alma</span><span class="sxs-lookup"><span data-stu-id="44814-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="44814-125">İlk iki komut Get-Date cmdlet 'ini kullanarak **DateTime** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44814-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="44814-126">Komutlar $StartTime ve $EndTime değişkenlerinde yeni zamanları depolar.</span><span class="sxs-lookup"><span data-stu-id="44814-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="44814-127">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="44814-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="44814-128">Son komutu, $StartTime ve $EndTime depolanan saatler arasında bulunan Device07 adlı cihaz için işler alır.</span><span class="sxs-lookup"><span data-stu-id="44814-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="44814-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44814-129">PARAMETERS</span></span>

### <span data-ttu-id="44814-130">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="44814-130">-DeviceName</span></span>
<span data-ttu-id="44814-131">StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44814-131">Specifies the name of a StorSimple device.</span></span>

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

### <span data-ttu-id="44814-132">-Önce</span><span class="sxs-lookup"><span data-stu-id="44814-132">-First</span></span>
<span data-ttu-id="44814-133">Yalnızca belirtilen sayıda nesneyi alır.</span><span class="sxs-lookup"><span data-stu-id="44814-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="44814-134">Alınacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="44814-134">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="44814-135">'Den</span><span class="sxs-lookup"><span data-stu-id="44814-135">-From</span></span>
<span data-ttu-id="44814-136">Bu cmdlet 'in aldığı işlerin başlangıç tarihini ve saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44814-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44814-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="44814-137">-InstanceId</span></span>
<span data-ttu-id="44814-138">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="44814-138">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="44814-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="44814-139">-Profile</span></span>
<span data-ttu-id="44814-140">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44814-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44814-141">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="44814-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44814-142">-Atla</span><span class="sxs-lookup"><span data-stu-id="44814-142">-Skip</span></span>
<span data-ttu-id="44814-143">Belirtilen sayıda nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="44814-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="44814-144">Atlanacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="44814-144">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="44814-145">-Durum</span><span class="sxs-lookup"><span data-stu-id="44814-145">-Status</span></span>
<span data-ttu-id="44814-146">Durumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="44814-146">Specifies the status.</span></span>
<span data-ttu-id="44814-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="44814-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44814-148">Çalışması</span><span class="sxs-lookup"><span data-stu-id="44814-148">Running</span></span>
- <span data-ttu-id="44814-149">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="44814-149">Completed</span></span>
- <span data-ttu-id="44814-150">İptal</span><span class="sxs-lookup"><span data-stu-id="44814-150">Cancelled</span></span>
- <span data-ttu-id="44814-151">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="44814-151">Failed</span></span>
- <span data-ttu-id="44814-152">İşleminin</span><span class="sxs-lookup"><span data-stu-id="44814-152">Canceling</span></span>
- <span data-ttu-id="44814-153">Completederrors</span><span class="sxs-lookup"><span data-stu-id="44814-153">CompletedWithErrors</span></span>

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

### <span data-ttu-id="44814-154">-To</span><span class="sxs-lookup"><span data-stu-id="44814-154">-To</span></span>
<span data-ttu-id="44814-155">Bu cmdlet 'in aldığı işlerin bitiş tarihini ve saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44814-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44814-156">-Tür</span><span class="sxs-lookup"><span data-stu-id="44814-156">-Type</span></span>
<span data-ttu-id="44814-157">İş türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="44814-157">Specifies the job type.</span></span>
<span data-ttu-id="44814-158">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="44814-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44814-159">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="44814-159">Backup</span></span>
- <span data-ttu-id="44814-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="44814-160">ManualBackup</span></span>
- <span data-ttu-id="44814-161">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="44814-161">Restore</span></span>
- <span data-ttu-id="44814-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="44814-162">CloneWorkflow</span></span>
- <span data-ttu-id="44814-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="44814-163">DeviceRestore</span></span>
- <span data-ttu-id="44814-164">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="44814-164">Update</span></span>
- <span data-ttu-id="44814-165">Destek paketi</span><span class="sxs-lookup"><span data-stu-id="44814-165">SupportPackage</span></span>
- <span data-ttu-id="44814-166">Virtualappliancesağlamasını</span><span class="sxs-lookup"><span data-stu-id="44814-166">VirtualApplianceProvisioning</span></span>

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

### <span data-ttu-id="44814-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44814-167">CommonParameters</span></span>
<span data-ttu-id="44814-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44814-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44814-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44814-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44814-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44814-170">INPUTS</span></span>

### <span data-ttu-id="44814-171">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="44814-171">None</span></span>
<span data-ttu-id="44814-172">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="44814-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="44814-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44814-173">OUTPUTS</span></span>

### <span data-ttu-id="44814-174">IList \<DeviceJobDetails\> , devicejobdetails</span><span class="sxs-lookup"><span data-stu-id="44814-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="44814-175">Bu cmdlet iş ayrıntıları nesnelerinin listesini döndürür veya *InstanceId* parametresini belirtirseniz, tek bir iş ayrıntı nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="44814-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="44814-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44814-176">NOTES</span></span>

## <span data-ttu-id="44814-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44814-177">RELATED LINKS</span></span>

[<span data-ttu-id="44814-178">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="44814-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


