---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587470"
---
# <span data-ttu-id="35e60-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="35e60-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="35e60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e60-102">SYNOPSIS</span></span>
<span data-ttu-id="35e60-103">Belirtilen ASR işinin ayrıntılarını veya kurtarma hizmetleri kasasındaki en son ASR işlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="35e60-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35e60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35e60-104">SYNTAX</span></span>

### <span data-ttu-id="35e60-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35e60-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35e60-106">ByName</span><span class="sxs-lookup"><span data-stu-id="35e60-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35e60-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="35e60-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35e60-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="35e60-108">DESCRIPTION</span></span>
<span data-ttu-id="35e60-109">**Get-AzureRmRecoveryServicesAsrJob** cmdlet 'ı Azure Site Recovery işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="35e60-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="35e60-110">Kurtarma Hizmetleri kasasındaki ASR işlerini görüntülemek için bu cmdlet 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="35e60-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="35e60-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35e60-111">EXAMPLES</span></span>

### <span data-ttu-id="35e60-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="35e60-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="35e60-113">Belirli bir ASR nesnesindeki tüm işleri döndürür (çoğaltılmış öğe veya kurtarma planı gibi ASR nesnesini KIMLIĞIYLE başvuru.)</span><span class="sxs-lookup"><span data-stu-id="35e60-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="35e60-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35e60-114">PARAMETERS</span></span>

### <span data-ttu-id="35e60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e60-115">-DefaultProfile</span></span>
<span data-ttu-id="35e60-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35e60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e60-117">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="35e60-117">-EndTime</span></span>
<span data-ttu-id="35e60-118">İşlerin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="35e60-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="35e60-119">Bu cmdlet belirtilen süreden önce başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="35e60-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="35e60-120">Bu parametre için bir **DateTime** nesnesi almak istiyorsanız Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="35e60-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="35e60-121">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="35e60-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="35e60-122">-Job</span><span class="sxs-lookup"><span data-stu-id="35e60-122">-Job</span></span>
<span data-ttu-id="35e60-123">Güncelleştirme ayrıntılarının alınacağı ASR iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="35e60-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="35e60-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="35e60-124">-Name</span></span>
<span data-ttu-id="35e60-125">ASR işini ada göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="35e60-125">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e60-126">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="35e60-126">-StartTime</span></span>
<span data-ttu-id="35e60-127">İşlerin başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="35e60-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="35e60-128">Bu cmdlet belirtilen süreden sonra başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="35e60-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="35e60-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="35e60-129">-State</span></span>
<span data-ttu-id="35e60-130">ASR işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="35e60-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="35e60-131">Bu cmdlet belirtilen durumla eşleşen tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="35e60-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="35e60-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="35e60-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35e60-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="35e60-133">NotStarted</span></span>
- <span data-ttu-id="35e60-134">Progress</span><span class="sxs-lookup"><span data-stu-id="35e60-134">InProgress</span></span>
- <span data-ttu-id="35e60-135">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="35e60-135">Succeeded</span></span>
- <span data-ttu-id="35e60-136">Diğerini</span><span class="sxs-lookup"><span data-stu-id="35e60-136">Other</span></span>
- <span data-ttu-id="35e60-137">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="35e60-137">Failed</span></span>
- <span data-ttu-id="35e60-138">İptal</span><span class="sxs-lookup"><span data-stu-id="35e60-138">Cancelled</span></span>
- <span data-ttu-id="35e60-139">Etsin</span><span class="sxs-lookup"><span data-stu-id="35e60-139">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e60-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="35e60-140">-TargetObjectId</span></span>
<span data-ttu-id="35e60-141">Nesnenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="35e60-141">Specifies the ID of the object.</span></span> <span data-ttu-id="35e60-142">Belirtilen nesnedeki işleri aramak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="35e60-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="35e60-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e60-143">CommonParameters</span></span>
<span data-ttu-id="35e60-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35e60-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e60-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35e60-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e60-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35e60-146">INPUTS</span></span>

### <span data-ttu-id="35e60-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="35e60-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="35e60-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35e60-148">OUTPUTS</span></span>

### <span data-ttu-id="35e60-149">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="35e60-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="35e60-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35e60-150">NOTES</span></span>

## <span data-ttu-id="35e60-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35e60-151">RELATED LINKS</span></span>

[<span data-ttu-id="35e60-152">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="35e60-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="35e60-153">Özgeçmiş-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="35e60-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="35e60-154">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="35e60-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
