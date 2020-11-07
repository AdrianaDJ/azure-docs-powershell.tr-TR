---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 73a9325ea4f1bc45eaaf2fb81796d526c7b95fea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752399"
---
# <span data-ttu-id="eb8cd-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eb8cd-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="eb8cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8cd-103">Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="eb8cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb8cd-104">SYNTAX</span></span>

### <span data-ttu-id="eb8cd-105">GetAllInResourceGroupAndAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb8cd-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb8cd-106">Getbyspecificjobınformation</span><span class="sxs-lookup"><span data-stu-id="eb8cd-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb8cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb8cd-107">DESCRIPTION</span></span>
<span data-ttu-id="eb8cd-108">**Get-Azdatalakeanaliz Ticsjob** cmdlet 'ı bir Azure Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="eb8cd-109">İş belirtmezseniz, bu cmdlet tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="eb8cd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb8cd-110">EXAMPLES</span></span>

### <span data-ttu-id="eb8cd-111">Örnek 1: belirtilen işi edinme</span><span class="sxs-lookup"><span data-stu-id="eb8cd-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="eb8cd-112">Bu komut belirtilen KIMLIĞE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="eb8cd-113">Örnek 2: geçen hafta gönderilen işleri alma</span><span class="sxs-lookup"><span data-stu-id="eb8cd-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="eb8cd-114">Bu komut, geçen hafta gönderilen işleri alır.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="eb8cd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb8cd-115">PARAMETERS</span></span>

### <span data-ttu-id="eb8cd-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="eb8cd-116">-Account</span></span>
<span data-ttu-id="eb8cd-117">Veri Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="eb8cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8cd-118">-DefaultProfile</span></span>
<span data-ttu-id="eb8cd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eb8cd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb8cd-120">-Include</span><span class="sxs-lookup"><span data-stu-id="eb8cd-120">-Include</span></span>
<span data-ttu-id="eb8cd-121">İş hakkında alınacak ek bilgi türünü belirten seçenekleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="eb8cd-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eb8cd-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb8cd-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eb8cd-123">None</span></span>
- <span data-ttu-id="eb8cd-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="eb8cd-124">DebugInfo</span></span>
- <span data-ttu-id="eb8cd-125">İstatistik</span><span class="sxs-lookup"><span data-stu-id="eb8cd-125">Statistics</span></span>
- <span data-ttu-id="eb8cd-126">Tüm</span><span class="sxs-lookup"><span data-stu-id="eb8cd-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="eb8cd-127">-JobId</span></span>
<span data-ttu-id="eb8cd-128">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb8cd-129">-Name</span></span>
<span data-ttu-id="eb8cd-130">İş listesi sonuçlarını filtrelemek için kullanılacak bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="eb8cd-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eb8cd-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb8cd-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eb8cd-132">None</span></span>
- <span data-ttu-id="eb8cd-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="eb8cd-133">DebugInfo</span></span>
- <span data-ttu-id="eb8cd-134">İstatistik</span><span class="sxs-lookup"><span data-stu-id="eb8cd-134">Statistics</span></span>
- <span data-ttu-id="eb8cd-135">Tüm</span><span class="sxs-lookup"><span data-stu-id="eb8cd-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-136">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="eb8cd-136">-PipelineId</span></span>
<span data-ttu-id="eb8cd-137">Belirtilen ardışık düzenin yalnızca işlerin bir bölümünü gösteren isteğe bağlı KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="eb8cd-138">-RecurrenceId</span></span>
<span data-ttu-id="eb8cd-139">Yalnızca belirtilen yinelenme işlerinin bir bölümünü gösteren isteğe bağlı bir KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-140">-Sonuç</span><span class="sxs-lookup"><span data-stu-id="eb8cd-140">-Result</span></span>
<span data-ttu-id="eb8cd-141">İş sonuçları için bir sonuç filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="eb8cd-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eb8cd-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb8cd-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eb8cd-143">None</span></span>
- <span data-ttu-id="eb8cd-144">İptal</span><span class="sxs-lookup"><span data-stu-id="eb8cd-144">Cancelled</span></span>
- <span data-ttu-id="eb8cd-145">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="eb8cd-145">Failed</span></span>
- <span data-ttu-id="eb8cd-146">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="eb8cd-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-147">Durumlu</span><span class="sxs-lookup"><span data-stu-id="eb8cd-147">-State</span></span>
<span data-ttu-id="eb8cd-148">İş sonuçları için bir durum filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="eb8cd-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eb8cd-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb8cd-150">Benimsen</span><span class="sxs-lookup"><span data-stu-id="eb8cd-150">Accepted</span></span>
- <span data-ttu-id="eb8cd-151">Yeni</span><span class="sxs-lookup"><span data-stu-id="eb8cd-151">New</span></span>
- <span data-ttu-id="eb8cd-152">Derleyip</span><span class="sxs-lookup"><span data-stu-id="eb8cd-152">Compiling</span></span>
- <span data-ttu-id="eb8cd-153">Planlamayı</span><span class="sxs-lookup"><span data-stu-id="eb8cd-153">Scheduling</span></span>
- <span data-ttu-id="eb8cd-154">Sıradan</span><span class="sxs-lookup"><span data-stu-id="eb8cd-154">Queued</span></span>
- <span data-ttu-id="eb8cd-155">Başlarken</span><span class="sxs-lookup"><span data-stu-id="eb8cd-155">Starting</span></span>
- <span data-ttu-id="eb8cd-156">Dığında</span><span class="sxs-lookup"><span data-stu-id="eb8cd-156">Paused</span></span>
- <span data-ttu-id="eb8cd-157">Çalışması</span><span class="sxs-lookup"><span data-stu-id="eb8cd-157">Running</span></span>
- <span data-ttu-id="eb8cd-158">Sonlandırdı</span><span class="sxs-lookup"><span data-stu-id="eb8cd-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="eb8cd-159">-SubmittedAfter</span></span>
<span data-ttu-id="eb8cd-160">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-160">Specifies a date filter.</span></span>
<span data-ttu-id="eb8cd-161">İş listesi sonucuna belirtilen tarihten sonra gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-162">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="eb8cd-162">-SubmittedBefore</span></span>
<span data-ttu-id="eb8cd-163">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-163">Specifies a date filter.</span></span>
<span data-ttu-id="eb8cd-164">İş listesi sonucuna belirtilen tarihten önce gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-165">-Gönderenin</span><span class="sxs-lookup"><span data-stu-id="eb8cd-165">-Submitter</span></span>
<span data-ttu-id="eb8cd-166">Bir kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="eb8cd-167">İş listesi sonuçlarını belirli bir kullanıcı tarafından gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-168">-Üst</span><span class="sxs-lookup"><span data-stu-id="eb8cd-168">-Top</span></span>
<span data-ttu-id="eb8cd-169">Döndürülecek iş sayısını belirten isteğe bağlı bir değer.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="eb8cd-170">Varsayılan değer 500</span><span class="sxs-lookup"><span data-stu-id="eb8cd-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8cd-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8cd-171">CommonParameters</span></span>
<span data-ttu-id="eb8cd-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8cd-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8cd-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8cd-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb8cd-174">INPUTS</span></span>

### <span data-ttu-id="eb8cd-175">System. String</span><span class="sxs-lookup"><span data-stu-id="eb8cd-175">System.String</span></span>

### <span data-ttu-id="eb8cd-176">System. Guid</span><span class="sxs-lookup"><span data-stu-id="eb8cd-176">System.Guid</span></span>

### <span data-ttu-id="eb8cd-177">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanalizleri Ticsenums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="eb8cd-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="eb8cd-178">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb8cd-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eb8cd-179">Microsoft. Azure. Management. DataLake. Analytics. modeller. JobState []</span><span class="sxs-lookup"><span data-stu-id="eb8cd-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="eb8cd-180">Microsoft. Azure. Management. DataLake. Analytics. modeller. JobResult []</span><span class="sxs-lookup"><span data-stu-id="eb8cd-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="eb8cd-181">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb8cd-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eb8cd-182">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb8cd-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eb8cd-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb8cd-183">OUTPUTS</span></span>

### <span data-ttu-id="eb8cd-184">Microsoft. Azure. Management. DataLake. Analytics. modeller. Jobınformation</span><span class="sxs-lookup"><span data-stu-id="eb8cd-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="eb8cd-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb8cd-185">NOTES</span></span>

## <span data-ttu-id="eb8cd-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb8cd-186">RELATED LINKS</span></span>

[<span data-ttu-id="eb8cd-187">Stop-Azdatalakeanaliz Ticsjob</span><span class="sxs-lookup"><span data-stu-id="eb8cd-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="eb8cd-188">Submit-Azdatalakeanaliz Ticsjob</span><span class="sxs-lookup"><span data-stu-id="eb8cd-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="eb8cd-189">Wait-Azdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="eb8cd-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


