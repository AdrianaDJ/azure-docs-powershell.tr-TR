---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105595"
---
# <span data-ttu-id="3a165-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3a165-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="3a165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a165-102">SYNOPSIS</span></span>
<span data-ttu-id="3a165-103">Site kurtarma Kasası için işlem bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a165-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="3a165-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a165-104">SYNTAX</span></span>

### <span data-ttu-id="3a165-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a165-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3a165-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="3a165-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3a165-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="3a165-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a165-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a165-108">DESCRIPTION</span></span>
<span data-ttu-id="3a165-109">**Get-AzureSiteRecoveryJob** cmdlet 'ı Azure Site Recovery işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a165-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="3a165-110">Bu cmdlet 'i, geçerli site kurtarma Kasası için işlem bilgilerini görüntülemek üzere kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a165-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="3a165-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a165-111">EXAMPLES</span></span>

### <span data-ttu-id="3a165-112">Örnek 1: KIMLIK belirterek iş alma</span><span class="sxs-lookup"><span data-stu-id="3a165-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="3a165-113">Bu komut belirtilen KIMLIĞE sahip Azure Site kurtarma işini alır.</span><span class="sxs-lookup"><span data-stu-id="3a165-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="3a165-114">Örnek 2: bir işi zamanında alır</span><span class="sxs-lookup"><span data-stu-id="3a165-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="3a165-115">Bu komut, belirtilen başlangıç saati ve bitiş saati arasında kalan site kurtarma işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a165-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="3a165-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a165-116">PARAMETERS</span></span>

### <span data-ttu-id="3a165-117">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="3a165-117">-EndTime</span></span>
<span data-ttu-id="3a165-118">İşlerin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a165-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="3a165-119">Bu cmdlet belirtilen süreden önce başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="3a165-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="3a165-120">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a165-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="3a165-121">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="3a165-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a165-122">-ID</span><span class="sxs-lookup"><span data-stu-id="3a165-122">-Id</span></span>
<span data-ttu-id="3a165-123">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a165-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a165-124">-Job</span><span class="sxs-lookup"><span data-stu-id="3a165-124">-Job</span></span>
<span data-ttu-id="3a165-125">Alınacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a165-125">Specifies a job to get.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a165-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a165-126">-Profile</span></span>
<span data-ttu-id="3a165-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a165-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a165-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3a165-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a165-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="3a165-129">-StartTime</span></span>
<span data-ttu-id="3a165-130">İşlerin başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a165-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="3a165-131">Bu cmdlet belirtilen süreden sonra başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="3a165-131">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a165-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="3a165-132">-State</span></span>
<span data-ttu-id="3a165-133">Site kurtarma işi için giriş durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a165-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="3a165-134">Bu cmdlet belirtilen durumla eşleşen tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="3a165-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="3a165-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3a165-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a165-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="3a165-136">NotStarted</span></span>
- <span data-ttu-id="3a165-137">Progress</span><span class="sxs-lookup"><span data-stu-id="3a165-137">InProgress</span></span>
- <span data-ttu-id="3a165-138">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3a165-138">Succeeded</span></span>
- <span data-ttu-id="3a165-139">Diğerini</span><span class="sxs-lookup"><span data-stu-id="3a165-139">Other</span></span>
- <span data-ttu-id="3a165-140">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="3a165-140">Failed</span></span>
- <span data-ttu-id="3a165-141">İptal</span><span class="sxs-lookup"><span data-stu-id="3a165-141">Cancelled</span></span>
- <span data-ttu-id="3a165-142">Etsin</span><span class="sxs-lookup"><span data-stu-id="3a165-142">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a165-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="3a165-143">-TargetObjectId</span></span>
<span data-ttu-id="3a165-144">İş tarafından hedeflenen nesnenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a165-144">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a165-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a165-145">CommonParameters</span></span>
<span data-ttu-id="3a165-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a165-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a165-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a165-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a165-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a165-148">INPUTS</span></span>

## <span data-ttu-id="3a165-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a165-149">OUTPUTS</span></span>

## <span data-ttu-id="3a165-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a165-150">NOTES</span></span>

## <span data-ttu-id="3a165-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a165-151">RELATED LINKS</span></span>

[<span data-ttu-id="3a165-152">Azure Site Recovery Hizmetleri cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="3a165-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="3a165-153">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3a165-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="3a165-154">Özgeçmiş-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3a165-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="3a165-155">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3a165-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


