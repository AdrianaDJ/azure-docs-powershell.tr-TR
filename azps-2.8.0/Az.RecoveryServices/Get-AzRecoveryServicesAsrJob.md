---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933047"
---
# <span data-ttu-id="eeef1-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eeef1-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="eeef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeef1-102">SYNOPSIS</span></span>
<span data-ttu-id="eeef1-103">Belirtilen ASR işinin ayrıntılarını veya kurtarma hizmetleri kasasındaki en son ASR işlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="eeef1-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="eeef1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eeef1-104">SYNTAX</span></span>

### <span data-ttu-id="eeef1-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eeef1-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeef1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="eeef1-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeef1-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="eeef1-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eeef1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eeef1-108">DESCRIPTION</span></span>
<span data-ttu-id="eeef1-109">**Get-AzRecoveryServicesAsrJob** cmdlet 'ı Azure Site Recovery işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="eeef1-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="eeef1-110">Kurtarma Hizmetleri kasasındaki ASR işlerini görüntülemek için bu cmdlet 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eeef1-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="eeef1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eeef1-111">EXAMPLES</span></span>

### <span data-ttu-id="eeef1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eeef1-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="eeef1-113">Belirli bir ASR nesnesindeki tüm işleri döndürür (çoğaltılmış öğe veya kurtarma planı gibi ASR nesnesini KIMLIĞIYLE başvuru.)</span><span class="sxs-lookup"><span data-stu-id="eeef1-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="eeef1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eeef1-114">PARAMETERS</span></span>

### <span data-ttu-id="eeef1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeef1-115">-DefaultProfile</span></span>
<span data-ttu-id="eeef1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eeef1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="eeef1-117">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="eeef1-117">-EndTime</span></span>
<span data-ttu-id="eeef1-118">İşlerin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeef1-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="eeef1-119">Bu cmdlet belirtilen süreden önce başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="eeef1-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="eeef1-120">Bu parametre için bir **DateTime** nesnesi almak istiyorsanız Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eeef1-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="eeef1-121">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="eeef1-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeef1-122">-Job</span><span class="sxs-lookup"><span data-stu-id="eeef1-122">-Job</span></span>
<span data-ttu-id="eeef1-123">Güncelleştirme ayrıntılarının alınacağı ASR iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeef1-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeef1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="eeef1-124">-Name</span></span>
<span data-ttu-id="eeef1-125">ASR işini ada göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="eeef1-125">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeef1-126">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="eeef1-126">-StartTime</span></span>
<span data-ttu-id="eeef1-127">İşlerin başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeef1-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="eeef1-128">Bu cmdlet belirtilen süreden sonra başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="eeef1-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeef1-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="eeef1-129">-State</span></span>
<span data-ttu-id="eeef1-130">ASR işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeef1-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="eeef1-131">Bu cmdlet belirtilen durumla eşleşen tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="eeef1-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="eeef1-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eeef1-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eeef1-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="eeef1-133">NotStarted</span></span>
- <span data-ttu-id="eeef1-134">Progress</span><span class="sxs-lookup"><span data-stu-id="eeef1-134">InProgress</span></span>
- <span data-ttu-id="eeef1-135">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="eeef1-135">Succeeded</span></span>
- <span data-ttu-id="eeef1-136">Diğerini</span><span class="sxs-lookup"><span data-stu-id="eeef1-136">Other</span></span>
- <span data-ttu-id="eeef1-137">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="eeef1-137">Failed</span></span>
- <span data-ttu-id="eeef1-138">İptal</span><span class="sxs-lookup"><span data-stu-id="eeef1-138">Cancelled</span></span>
- <span data-ttu-id="eeef1-139">Etsin</span><span class="sxs-lookup"><span data-stu-id="eeef1-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeef1-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="eeef1-140">-TargetObjectId</span></span>
<span data-ttu-id="eeef1-141">Nesnenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeef1-141">Specifies the ID of the object.</span></span> <span data-ttu-id="eeef1-142">Belirtilen nesnedeki işleri aramak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eeef1-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeef1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeef1-143">CommonParameters</span></span>
<span data-ttu-id="eeef1-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eeef1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeef1-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeef1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeef1-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eeef1-146">INPUTS</span></span>

### <span data-ttu-id="eeef1-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eeef1-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eeef1-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eeef1-148">OUTPUTS</span></span>

### <span data-ttu-id="eeef1-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eeef1-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eeef1-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eeef1-150">NOTES</span></span>

## <span data-ttu-id="eeef1-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eeef1-151">RELATED LINKS</span></span>

[<span data-ttu-id="eeef1-152">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eeef1-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="eeef1-153">Özgeçmiş-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eeef1-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="eeef1-154">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eeef1-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
