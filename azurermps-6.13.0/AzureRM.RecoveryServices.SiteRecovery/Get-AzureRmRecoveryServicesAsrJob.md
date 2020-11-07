---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: f79bc9e32ab179c10c09f3780a591182ea1d630b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762906"
---
# <span data-ttu-id="bdb7e-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdb7e-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="bdb7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb7e-103">Belirtilen ASR işinin ayrıntılarını veya kurtarma hizmetleri kasasındaki en son ASR işlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdb7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdb7e-104">SYNTAX</span></span>

### <span data-ttu-id="bdb7e-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bdb7e-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb7e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bdb7e-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdb7e-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="bdb7e-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdb7e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdb7e-108">DESCRIPTION</span></span>
<span data-ttu-id="bdb7e-109">**Get-AzureRmRecoveryServicesAsrJob** cmdlet 'ı Azure Site Recovery işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="bdb7e-110">Kurtarma Hizmetleri kasasındaki ASR işlerini görüntülemek için bu cmdlet 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="bdb7e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdb7e-111">EXAMPLES</span></span>

### <span data-ttu-id="bdb7e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bdb7e-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="bdb7e-113">Belirli bir ASR nesnesindeki tüm işleri döndürür (çoğaltılmış öğe veya kurtarma planı gibi ASR nesnesini KIMLIĞIYLE başvuru.)</span><span class="sxs-lookup"><span data-stu-id="bdb7e-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="bdb7e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdb7e-114">PARAMETERS</span></span>

### <span data-ttu-id="bdb7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb7e-115">-DefaultProfile</span></span>
<span data-ttu-id="bdb7e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb7e-117">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="bdb7e-117">-EndTime</span></span>
<span data-ttu-id="bdb7e-118">İşlerin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="bdb7e-119">Bu cmdlet belirtilen süreden önce başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="bdb7e-120">Bu parametre için bir **DateTime** nesnesi almak istiyorsanız Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="bdb7e-121">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bdb7e-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="bdb7e-122">-Job</span><span class="sxs-lookup"><span data-stu-id="bdb7e-122">-Job</span></span>
<span data-ttu-id="bdb7e-123">Güncelleştirme ayrıntılarının alınacağı ASR iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="bdb7e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bdb7e-124">-Name</span></span>
<span data-ttu-id="bdb7e-125">ASR işini ada göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="bdb7e-126">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="bdb7e-126">-StartTime</span></span>
<span data-ttu-id="bdb7e-127">İşlerin başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="bdb7e-128">Bu cmdlet belirtilen süreden sonra başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="bdb7e-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="bdb7e-129">-State</span></span>
<span data-ttu-id="bdb7e-130">ASR işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="bdb7e-131">Bu cmdlet belirtilen durumla eşleşen tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="bdb7e-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdb7e-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bdb7e-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="bdb7e-133">NotStarted</span></span>
- <span data-ttu-id="bdb7e-134">Progress</span><span class="sxs-lookup"><span data-stu-id="bdb7e-134">InProgress</span></span>
- <span data-ttu-id="bdb7e-135">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdb7e-135">Succeeded</span></span>
- <span data-ttu-id="bdb7e-136">Diğerini</span><span class="sxs-lookup"><span data-stu-id="bdb7e-136">Other</span></span>
- <span data-ttu-id="bdb7e-137">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="bdb7e-137">Failed</span></span>
- <span data-ttu-id="bdb7e-138">İptal</span><span class="sxs-lookup"><span data-stu-id="bdb7e-138">Cancelled</span></span>
- <span data-ttu-id="bdb7e-139">Etsin</span><span class="sxs-lookup"><span data-stu-id="bdb7e-139">Suspended</span></span>

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

### <span data-ttu-id="bdb7e-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="bdb7e-140">-TargetObjectId</span></span>
<span data-ttu-id="bdb7e-141">Nesnenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-141">Specifies the ID of the object.</span></span> <span data-ttu-id="bdb7e-142">Belirtilen nesnedeki işleri aramak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="bdb7e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb7e-143">CommonParameters</span></span>
<span data-ttu-id="bdb7e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdb7e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb7e-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb7e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb7e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdb7e-146">INPUTS</span></span>

### <span data-ttu-id="bdb7e-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bdb7e-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bdb7e-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdb7e-148">OUTPUTS</span></span>

### <span data-ttu-id="bdb7e-149">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bdb7e-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bdb7e-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdb7e-150">NOTES</span></span>

## <span data-ttu-id="bdb7e-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdb7e-151">RELATED LINKS</span></span>

[<span data-ttu-id="bdb7e-152">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdb7e-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="bdb7e-153">Özgeçmiş-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdb7e-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="bdb7e-154">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdb7e-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
