---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105528"
---
# <span data-ttu-id="e6bfa-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="e6bfa-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="e6bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bfa-103">Yedekleme zamanlama yapılandırması nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="e6bfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6bfa-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6bfa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="e6bfa-106">**New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ı bir **backupschedulebase** yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="e6bfa-107">**New-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak yeni yedekleme ilkesi oluşturmak için bu yapılandırma nesnesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="e6bfa-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6bfa-108">EXAMPLES</span></span>

### <span data-ttu-id="e6bfa-109">Örnek 1: yedek yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6bfa-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="e6bfa-110">Bu komut, bulut anlık görüntü yedekleri için yedekleme zamanlama taban nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="e6bfa-111">Yedekleme her gün gerçekleşir ve yedeklemeler 100 gündür tutulur.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="e6bfa-112">Bu zamanlama, geçerli saat olan varsayılan saatten etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="e6bfa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6bfa-113">PARAMETERS</span></span>

### <span data-ttu-id="e6bfa-114">-BackupType</span><span class="sxs-lookup"><span data-stu-id="e6bfa-114">-BackupType</span></span>
<span data-ttu-id="e6bfa-115">Yedekleme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-115">Specifies the backup type.</span></span>
<span data-ttu-id="e6bfa-116">Geçerli değerler: LocalSnapshot ve CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="e6bfa-117">Özellikli</span><span class="sxs-lookup"><span data-stu-id="e6bfa-117">-Enabled</span></span>
<span data-ttu-id="e6bfa-118">Yedekleme zamanlamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bfa-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="e6bfa-119">-Profile</span></span>
<span data-ttu-id="e6bfa-120">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e6bfa-121">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="e6bfa-121">-RecurrenceType</span></span>
<span data-ttu-id="e6bfa-122">Bu yedekleme zamanlaması için yinelenme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="e6bfa-123">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e6bfa-123">Valid values are:</span></span> 

- <span data-ttu-id="e6bfa-124">Dakika</span><span class="sxs-lookup"><span data-stu-id="e6bfa-124">Minutes</span></span>
- <span data-ttu-id="e6bfa-125">Dayanarak</span><span class="sxs-lookup"><span data-stu-id="e6bfa-125">Hourly</span></span>
- <span data-ttu-id="e6bfa-126">Mü</span><span class="sxs-lookup"><span data-stu-id="e6bfa-126">Daily</span></span>
- <span data-ttu-id="e6bfa-127">Haftalık</span><span class="sxs-lookup"><span data-stu-id="e6bfa-127">Weekly</span></span>

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

### <span data-ttu-id="e6bfa-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="e6bfa-128">-RecurrenceValue</span></span>
<span data-ttu-id="e6bfa-129">Yedeklemenin ne sıklıkta yapılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="e6bfa-130">Bu parametre, *RecurrenceType* parametresiyle belirtilen birimi kullanır.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bfa-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="e6bfa-131">-RetentionCount</span></span>
<span data-ttu-id="e6bfa-132">Yedeklemenin tutulacağı gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-132">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bfa-133">-Startfromdatetıme</span><span class="sxs-lookup"><span data-stu-id="e6bfa-133">-StartFromDateTime</span></span>
<span data-ttu-id="e6bfa-134">Yedeklemelerin başlayacağı tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="e6bfa-135">Varsayılan değer geçerli süredir.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="e6bfa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bfa-136">CommonParameters</span></span>
<span data-ttu-id="e6bfa-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bfa-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6bfa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bfa-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6bfa-139">INPUTS</span></span>

### <span data-ttu-id="e6bfa-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e6bfa-140">None</span></span>

## <span data-ttu-id="e6bfa-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6bfa-141">OUTPUTS</span></span>

### <span data-ttu-id="e6bfa-142">Yedeklemeschedulebase</span><span class="sxs-lookup"><span data-stu-id="e6bfa-142">BackupScheduleBase</span></span>
<span data-ttu-id="e6bfa-143">Bu cmdlet bir **Backupschedulebase** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="e6bfa-144">Yeni yedekleme ilkesi oluşturmak için **Backupschedulebase** kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6bfa-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="e6bfa-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6bfa-145">NOTES</span></span>

## <span data-ttu-id="e6bfa-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6bfa-146">RELATED LINKS</span></span>

[<span data-ttu-id="e6bfa-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e6bfa-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="e6bfa-148">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e6bfa-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


