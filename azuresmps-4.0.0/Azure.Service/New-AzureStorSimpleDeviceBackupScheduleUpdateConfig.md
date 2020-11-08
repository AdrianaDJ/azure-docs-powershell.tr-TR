---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105524"
---
# <span data-ttu-id="6da11-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6da11-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="6da11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6da11-102">SYNOPSIS</span></span>
<span data-ttu-id="6da11-103">Yedekleme zamanlama güncelleştirmesi yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6da11-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="6da11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6da11-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6da11-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6da11-105">DESCRIPTION</span></span>
<span data-ttu-id="6da11-106">**New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet 'ı bir **Backupscheduleupdaterequest** yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6da11-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="6da11-107">**Set-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak yedekleme ilkesini güncelleştirmek için bu yapılandırma nesnesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6da11-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="6da11-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6da11-108">EXAMPLES</span></span>

### <span data-ttu-id="6da11-109">Örnek 1: zamanlama güncelleştirme isteği oluşturma</span><span class="sxs-lookup"><span data-stu-id="6da11-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="6da11-110">Bu komut zamanlama için belirtilen KIMLIĞE sahip bir yedekleme zamanlama güncelleştirme isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6da11-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="6da11-111">İstek, zamanlamayı her saat yinelenirse bir bulut anlık görüntü yedeklemesi yapmak.</span><span class="sxs-lookup"><span data-stu-id="6da11-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="6da11-112">Yedeklemeler 50 gündür.</span><span class="sxs-lookup"><span data-stu-id="6da11-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="6da11-113">Bu zamanlama, geçerli saat olan varsayılan saatten etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6da11-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="6da11-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6da11-114">PARAMETERS</span></span>

### <span data-ttu-id="6da11-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="6da11-115">-BackupType</span></span>
<span data-ttu-id="6da11-116">Yedekleme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6da11-116">Specifies the backup type.</span></span>
<span data-ttu-id="6da11-117">Geçerli değerler: LocalSnapshot ve CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="6da11-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="6da11-118">Özellikli</span><span class="sxs-lookup"><span data-stu-id="6da11-118">-Enabled</span></span>
<span data-ttu-id="6da11-119">Yedekleme zamanlamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6da11-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da11-120">-ID</span><span class="sxs-lookup"><span data-stu-id="6da11-120">-Id</span></span>
<span data-ttu-id="6da11-121">Güncelleştirilecek yedekleme zamanlamasının örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6da11-121">Specifies the instance ID of the backup schedule to update.</span></span>

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

### <span data-ttu-id="6da11-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="6da11-122">-Profile</span></span>
<span data-ttu-id="6da11-123">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="6da11-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6da11-124">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="6da11-124">-RecurrenceType</span></span>
<span data-ttu-id="6da11-125">Bu yedekleme zamanlaması için yinelenme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6da11-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="6da11-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="6da11-126">Valid values are:</span></span> 

- <span data-ttu-id="6da11-127">Dakika</span><span class="sxs-lookup"><span data-stu-id="6da11-127">Minutes</span></span>
- <span data-ttu-id="6da11-128">Dayanarak</span><span class="sxs-lookup"><span data-stu-id="6da11-128">Hourly</span></span>
- <span data-ttu-id="6da11-129">Mü</span><span class="sxs-lookup"><span data-stu-id="6da11-129">Daily</span></span>
- <span data-ttu-id="6da11-130">Haftalık</span><span class="sxs-lookup"><span data-stu-id="6da11-130">Weekly</span></span>

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

### <span data-ttu-id="6da11-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="6da11-131">-RecurrenceValue</span></span>
<span data-ttu-id="6da11-132">Yedeklemenin ne sıklıkta yapılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6da11-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="6da11-133">Bu parametre, *RecurrenceType* parametresiyle belirtilen birimi kullanır.</span><span class="sxs-lookup"><span data-stu-id="6da11-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="6da11-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="6da11-134">-RetentionCount</span></span>
<span data-ttu-id="6da11-135">Yedeklemenin tutulacağı gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6da11-135">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="6da11-136">-Startfromdatetıme</span><span class="sxs-lookup"><span data-stu-id="6da11-136">-StartFromDateTime</span></span>
<span data-ttu-id="6da11-137">Yedeklemelerin başlayacağı tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6da11-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="6da11-138">Varsayılan değer geçerli süredir.</span><span class="sxs-lookup"><span data-stu-id="6da11-138">The default value is the current time.</span></span>

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

### <span data-ttu-id="6da11-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da11-139">CommonParameters</span></span>
<span data-ttu-id="6da11-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6da11-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da11-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da11-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da11-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6da11-142">INPUTS</span></span>

### <span data-ttu-id="6da11-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6da11-143">None</span></span>

## <span data-ttu-id="6da11-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6da11-144">OUTPUTS</span></span>

### <span data-ttu-id="6da11-145">Yedeklemescheduleupdaterequest</span><span class="sxs-lookup"><span data-stu-id="6da11-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="6da11-146">Bu cmdlet, güncelleştirilmiş yedekleme zamanlamaları hakkında bilgi içeren bir **Backupscheduleupdaterequest** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="6da11-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="6da11-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6da11-147">NOTES</span></span>

## <span data-ttu-id="6da11-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6da11-148">RELATED LINKS</span></span>

[<span data-ttu-id="6da11-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="6da11-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="6da11-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6da11-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


