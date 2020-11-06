---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594738"
---
# <span data-ttu-id="eeb3c-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eeb3c-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="eeb3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb3c-103">Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeb3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eeb3c-104">SYNTAX</span></span>

### <span data-ttu-id="eeb3c-105">Tümü kaynak grubu ve hesabında (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eeb3c-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeb3c-106">Belirli Jobınformation</span><span class="sxs-lookup"><span data-stu-id="eeb3c-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eeb3c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eeb3c-107">DESCRIPTION</span></span>
<span data-ttu-id="eeb3c-108">**Get-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="eeb3c-109">İş belirtmezseniz, bu cmdlet tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="eeb3c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eeb3c-110">EXAMPLES</span></span>

### <span data-ttu-id="eeb3c-111">Örnek 1: belirtilen işi edinme</span><span class="sxs-lookup"><span data-stu-id="eeb3c-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="eeb3c-112">Bu komut belirtilen KIMLIĞE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="eeb3c-113">Örnek 2: geçen hafta gönderilen işleri alma</span><span class="sxs-lookup"><span data-stu-id="eeb3c-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="eeb3c-114">Bu komut, geçen hafta gönderilen işleri alır.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="eeb3c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eeb3c-115">PARAMETERS</span></span>

### <span data-ttu-id="eeb3c-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="eeb3c-116">-Account</span></span>
<span data-ttu-id="eeb3c-117">Veri Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-118">-Include</span><span class="sxs-lookup"><span data-stu-id="eeb3c-118">-Include</span></span>
<span data-ttu-id="eeb3c-119">İş hakkında alınacak ek bilgi türünü belirten seçenekleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="eeb3c-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eeb3c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eeb3c-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eeb3c-121">None</span></span>
- <span data-ttu-id="eeb3c-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="eeb3c-122">DebugInfo</span></span>
- <span data-ttu-id="eeb3c-123">İstatistik</span><span class="sxs-lookup"><span data-stu-id="eeb3c-123">Statistics</span></span>
- <span data-ttu-id="eeb3c-124">Tüm</span><span class="sxs-lookup"><span data-stu-id="eeb3c-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="eeb3c-125">-JobId</span></span>
<span data-ttu-id="eeb3c-126">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="eeb3c-127">-Name</span></span>
<span data-ttu-id="eeb3c-128">İş listesi sonuçlarını filtrelemek için kullanılacak bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="eeb3c-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eeb3c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eeb3c-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eeb3c-130">None</span></span>
- <span data-ttu-id="eeb3c-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="eeb3c-131">DebugInfo</span></span>
- <span data-ttu-id="eeb3c-132">İstatistik</span><span class="sxs-lookup"><span data-stu-id="eeb3c-132">Statistics</span></span>
- <span data-ttu-id="eeb3c-133">Tüm</span><span class="sxs-lookup"><span data-stu-id="eeb3c-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-134">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="eeb3c-134">-PipelineId</span></span>
<span data-ttu-id="eeb3c-135">Belirtilen ardışık düzenin yalnızca işlerin bir bölümünü gösteren isteğe bağlı KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="eeb3c-136">-RecurrenceId</span></span>
<span data-ttu-id="eeb3c-137">Yalnızca belirtilen yinelenme işlerinin bir bölümünü gösteren isteğe bağlı bir KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-138">-Sonuç</span><span class="sxs-lookup"><span data-stu-id="eeb3c-138">-Result</span></span>
<span data-ttu-id="eeb3c-139">İş sonuçları için bir sonuç filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="eeb3c-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eeb3c-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eeb3c-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eeb3c-141">None</span></span>
- <span data-ttu-id="eeb3c-142">İptal</span><span class="sxs-lookup"><span data-stu-id="eeb3c-142">Cancelled</span></span>
- <span data-ttu-id="eeb3c-143">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="eeb3c-143">Failed</span></span>
- <span data-ttu-id="eeb3c-144">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="eeb3c-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-145">Durumlu</span><span class="sxs-lookup"><span data-stu-id="eeb3c-145">-State</span></span>
<span data-ttu-id="eeb3c-146">İş sonuçları için bir durum filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="eeb3c-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eeb3c-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eeb3c-148">Benimsen</span><span class="sxs-lookup"><span data-stu-id="eeb3c-148">Accepted</span></span>
- <span data-ttu-id="eeb3c-149">Yeni</span><span class="sxs-lookup"><span data-stu-id="eeb3c-149">New</span></span>
- <span data-ttu-id="eeb3c-150">Derleyip</span><span class="sxs-lookup"><span data-stu-id="eeb3c-150">Compiling</span></span>
- <span data-ttu-id="eeb3c-151">Planlamayı</span><span class="sxs-lookup"><span data-stu-id="eeb3c-151">Scheduling</span></span>
- <span data-ttu-id="eeb3c-152">Sıradan</span><span class="sxs-lookup"><span data-stu-id="eeb3c-152">Queued</span></span>
- <span data-ttu-id="eeb3c-153">Başlarken</span><span class="sxs-lookup"><span data-stu-id="eeb3c-153">Starting</span></span>
- <span data-ttu-id="eeb3c-154">Dığında</span><span class="sxs-lookup"><span data-stu-id="eeb3c-154">Paused</span></span>
- <span data-ttu-id="eeb3c-155">Çalışması</span><span class="sxs-lookup"><span data-stu-id="eeb3c-155">Running</span></span>
- <span data-ttu-id="eeb3c-156">Sonlandırdı</span><span class="sxs-lookup"><span data-stu-id="eeb3c-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="eeb3c-157">-SubmittedAfter</span></span>
<span data-ttu-id="eeb3c-158">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-158">Specifies a date filter.</span></span>
<span data-ttu-id="eeb3c-159">İş listesi sonucuna belirtilen tarihten sonra gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-160">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="eeb3c-160">-SubmittedBefore</span></span>
<span data-ttu-id="eeb3c-161">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-161">Specifies a date filter.</span></span>
<span data-ttu-id="eeb3c-162">İş listesi sonucuna belirtilen tarihten önce gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-163">-Gönderenin</span><span class="sxs-lookup"><span data-stu-id="eeb3c-163">-Submitter</span></span>
<span data-ttu-id="eeb3c-164">Bir kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="eeb3c-165">İş listesi sonuçlarını belirli bir kullanıcı tarafından gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-166">-Üst</span><span class="sxs-lookup"><span data-stu-id="eeb3c-166">-Top</span></span>
<span data-ttu-id="eeb3c-167">Döndürülecek iş sayısını belirten isteğe bağlı bir değer.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="eeb3c-168">Varsayılan değer 500</span><span class="sxs-lookup"><span data-stu-id="eeb3c-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb3c-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb3c-169">-DefaultProfile</span></span>
<span data-ttu-id="eeb3c-170">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeb3c-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb3c-171">CommonParameters</span></span>
<span data-ttu-id="eeb3c-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb3c-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb3c-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb3c-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eeb3c-174">INPUTS</span></span>

### <span data-ttu-id="eeb3c-175">'Sine</span><span class="sxs-lookup"><span data-stu-id="eeb3c-175">Guid</span></span>
<span data-ttu-id="eeb3c-176">' JobId ' parametresi ardışık düzenin ' Guid ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="eeb3c-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="eeb3c-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eeb3c-177">OUTPUTS</span></span>

### <span data-ttu-id="eeb3c-178">Jobınformation</span><span class="sxs-lookup"><span data-stu-id="eeb3c-178">JobInformation</span></span>
<span data-ttu-id="eeb3c-179">Belirtilen iş bilgileri ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="eeb3c-179">The specified job information details</span></span>

### <span data-ttu-id="eeb3c-180">Listeniz<JobInformation></span><span class="sxs-lookup"><span data-stu-id="eeb3c-180">List<JobInformation></span></span>
<span data-ttu-id="eeb3c-181">Belirtilen veri Lake Analytics hesabındaki işlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="eeb3c-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eeb3c-182">NOTES</span></span>

## <span data-ttu-id="eeb3c-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eeb3c-183">RELATED LINKS</span></span>

[<span data-ttu-id="eeb3c-184">Stop-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="eeb3c-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="eeb3c-185">Submit-Azurermdatalakeanalyzer Ticsjob</span><span class="sxs-lookup"><span data-stu-id="eeb3c-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="eeb3c-186">Wait-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="eeb3c-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


