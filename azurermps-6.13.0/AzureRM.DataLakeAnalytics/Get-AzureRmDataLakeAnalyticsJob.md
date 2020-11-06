---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 59ec07b253b30d9cc7f03153706afba20331022c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593269"
---
# <span data-ttu-id="14854-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="14854-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="14854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14854-102">SYNOPSIS</span></span>
<span data-ttu-id="14854-103">Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="14854-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14854-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14854-104">SYNTAX</span></span>

### <span data-ttu-id="14854-105">GetAllInResourceGroupAndAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="14854-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14854-106">Getbyspecificjobınformation</span><span class="sxs-lookup"><span data-stu-id="14854-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14854-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="14854-107">DESCRIPTION</span></span>
<span data-ttu-id="14854-108">**Get-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="14854-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="14854-109">İş belirtmezseniz, bu cmdlet tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="14854-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="14854-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14854-110">EXAMPLES</span></span>

### <span data-ttu-id="14854-111">Örnek 1: belirtilen işi edinme</span><span class="sxs-lookup"><span data-stu-id="14854-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="14854-112">Bu komut belirtilen KIMLIĞE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="14854-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="14854-113">Örnek 2: geçen hafta gönderilen işleri alma</span><span class="sxs-lookup"><span data-stu-id="14854-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="14854-114">Bu komut, geçen hafta gönderilen işleri alır.</span><span class="sxs-lookup"><span data-stu-id="14854-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="14854-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14854-115">PARAMETERS</span></span>

### <span data-ttu-id="14854-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="14854-116">-Account</span></span>
<span data-ttu-id="14854-117">Veri Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="14854-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14854-118">-DefaultProfile</span></span>
<span data-ttu-id="14854-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="14854-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14854-120">-Include</span><span class="sxs-lookup"><span data-stu-id="14854-120">-Include</span></span>
<span data-ttu-id="14854-121">İş hakkında alınacak ek bilgi türünü belirten seçenekleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="14854-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="14854-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14854-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14854-123">None</span></span>
- <span data-ttu-id="14854-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="14854-124">DebugInfo</span></span>
- <span data-ttu-id="14854-125">İstatistik</span><span class="sxs-lookup"><span data-stu-id="14854-125">Statistics</span></span>
- <span data-ttu-id="14854-126">Tüm</span><span class="sxs-lookup"><span data-stu-id="14854-126">All</span></span>

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

### <span data-ttu-id="14854-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="14854-127">-JobId</span></span>
<span data-ttu-id="14854-128">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="14854-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="14854-129">-Name</span></span>
<span data-ttu-id="14854-130">İş listesi sonuçlarını filtrelemek için kullanılacak bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="14854-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="14854-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14854-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14854-132">None</span></span>
- <span data-ttu-id="14854-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="14854-133">DebugInfo</span></span>
- <span data-ttu-id="14854-134">İstatistik</span><span class="sxs-lookup"><span data-stu-id="14854-134">Statistics</span></span>
- <span data-ttu-id="14854-135">Tüm</span><span class="sxs-lookup"><span data-stu-id="14854-135">All</span></span>

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

### <span data-ttu-id="14854-136">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="14854-136">-PipelineId</span></span>
<span data-ttu-id="14854-137">Belirtilen ardışık düzenin yalnızca işlerin bir bölümünü gösteren isteğe bağlı KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="14854-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="14854-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="14854-138">-RecurrenceId</span></span>
<span data-ttu-id="14854-139">Yalnızca belirtilen yinelenme işlerinin bir bölümünü gösteren isteğe bağlı bir KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="14854-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="14854-140">-Sonuç</span><span class="sxs-lookup"><span data-stu-id="14854-140">-Result</span></span>
<span data-ttu-id="14854-141">İş sonuçları için bir sonuç filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="14854-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="14854-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14854-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14854-143">None</span></span>
- <span data-ttu-id="14854-144">İptal</span><span class="sxs-lookup"><span data-stu-id="14854-144">Cancelled</span></span>
- <span data-ttu-id="14854-145">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="14854-145">Failed</span></span>
- <span data-ttu-id="14854-146">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="14854-146">Succeeded</span></span>

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

### <span data-ttu-id="14854-147">Durumlu</span><span class="sxs-lookup"><span data-stu-id="14854-147">-State</span></span>
<span data-ttu-id="14854-148">İş sonuçları için bir durum filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="14854-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="14854-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14854-150">Benimsen</span><span class="sxs-lookup"><span data-stu-id="14854-150">Accepted</span></span>
- <span data-ttu-id="14854-151">Yeni</span><span class="sxs-lookup"><span data-stu-id="14854-151">New</span></span>
- <span data-ttu-id="14854-152">Derleyip</span><span class="sxs-lookup"><span data-stu-id="14854-152">Compiling</span></span>
- <span data-ttu-id="14854-153">Planlamayı</span><span class="sxs-lookup"><span data-stu-id="14854-153">Scheduling</span></span>
- <span data-ttu-id="14854-154">Sıradan</span><span class="sxs-lookup"><span data-stu-id="14854-154">Queued</span></span>
- <span data-ttu-id="14854-155">Başlarken</span><span class="sxs-lookup"><span data-stu-id="14854-155">Starting</span></span>
- <span data-ttu-id="14854-156">Dığında</span><span class="sxs-lookup"><span data-stu-id="14854-156">Paused</span></span>
- <span data-ttu-id="14854-157">Çalışması</span><span class="sxs-lookup"><span data-stu-id="14854-157">Running</span></span>
- <span data-ttu-id="14854-158">Sonlandırdı</span><span class="sxs-lookup"><span data-stu-id="14854-158">Ended</span></span>

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

### <span data-ttu-id="14854-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="14854-159">-SubmittedAfter</span></span>
<span data-ttu-id="14854-160">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-160">Specifies a date filter.</span></span>
<span data-ttu-id="14854-161">İş listesi sonucuna belirtilen tarihten sonra gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="14854-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="14854-162">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="14854-162">-SubmittedBefore</span></span>
<span data-ttu-id="14854-163">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-163">Specifies a date filter.</span></span>
<span data-ttu-id="14854-164">İş listesi sonucuna belirtilen tarihten önce gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="14854-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="14854-165">-Gönderenin</span><span class="sxs-lookup"><span data-stu-id="14854-165">-Submitter</span></span>
<span data-ttu-id="14854-166">Bir kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="14854-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="14854-167">İş listesi sonuçlarını belirli bir kullanıcı tarafından gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="14854-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="14854-168">-Üst</span><span class="sxs-lookup"><span data-stu-id="14854-168">-Top</span></span>
<span data-ttu-id="14854-169">Döndürülecek iş sayısını belirten isteğe bağlı bir değer.</span><span class="sxs-lookup"><span data-stu-id="14854-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="14854-170">Varsayılan değer 500</span><span class="sxs-lookup"><span data-stu-id="14854-170">Default value is 500</span></span>

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

### <span data-ttu-id="14854-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14854-171">CommonParameters</span></span>
<span data-ttu-id="14854-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14854-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14854-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14854-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14854-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14854-174">INPUTS</span></span>

### <span data-ttu-id="14854-175">System. String</span><span class="sxs-lookup"><span data-stu-id="14854-175">System.String</span></span>

### <span data-ttu-id="14854-176">System. Guid</span><span class="sxs-lookup"><span data-stu-id="14854-176">System.Guid</span></span>

### <span data-ttu-id="14854-177">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanalizleri Ticsenums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="14854-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="14854-178">System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="14854-178">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="14854-179">Microsoft. Azure. Management. DataLake. Analytics. modeller. JobState []</span><span class="sxs-lookup"><span data-stu-id="14854-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="14854-180">Microsoft. Azure. Management. DataLake. Analytics. modeller. JobResult []</span><span class="sxs-lookup"><span data-stu-id="14854-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="14854-181">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="14854-181">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="14854-182">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="14854-182">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="14854-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14854-183">OUTPUTS</span></span>

### <span data-ttu-id="14854-184">Microsoft. Azure. Management. DataLake. Analytics. modeller. Jobınformation</span><span class="sxs-lookup"><span data-stu-id="14854-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="14854-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14854-185">NOTES</span></span>

## <span data-ttu-id="14854-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14854-186">RELATED LINKS</span></span>

[<span data-ttu-id="14854-187">Stop-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="14854-187">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="14854-188">Submit-Azurermdatalakeanalyzer Ticsjob</span><span class="sxs-lookup"><span data-stu-id="14854-188">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="14854-189">Wait-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="14854-189">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


