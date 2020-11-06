---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586710"
---
# <span data-ttu-id="67661-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="67661-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="67661-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67661-102">SYNOPSIS</span></span>
<span data-ttu-id="67661-103">Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="67661-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67661-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67661-104">SYNTAX</span></span>

### <span data-ttu-id="67661-105">GetAllInResourceGroupAndAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67661-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67661-106">Getbyspecificjobınformation</span><span class="sxs-lookup"><span data-stu-id="67661-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67661-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="67661-107">DESCRIPTION</span></span>
<span data-ttu-id="67661-108">**Get-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics işini alır.</span><span class="sxs-lookup"><span data-stu-id="67661-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="67661-109">İş belirtmezseniz, bu cmdlet tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="67661-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="67661-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67661-110">EXAMPLES</span></span>

### <span data-ttu-id="67661-111">Örnek 1: belirtilen işi edinme</span><span class="sxs-lookup"><span data-stu-id="67661-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="67661-112">Bu komut belirtilen KIMLIĞE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="67661-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="67661-113">Örnek 2: geçen hafta gönderilen işleri alma</span><span class="sxs-lookup"><span data-stu-id="67661-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="67661-114">Bu komut, geçen hafta gönderilen işleri alır.</span><span class="sxs-lookup"><span data-stu-id="67661-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="67661-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67661-115">PARAMETERS</span></span>

### <span data-ttu-id="67661-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="67661-116">-Account</span></span>
<span data-ttu-id="67661-117">Veri Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67661-118">-DefaultProfile</span></span>
<span data-ttu-id="67661-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="67661-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67661-120">-Include</span><span class="sxs-lookup"><span data-stu-id="67661-120">-Include</span></span>
<span data-ttu-id="67661-121">İş hakkında alınacak ek bilgi türünü belirten seçenekleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="67661-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="67661-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67661-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67661-123">None</span></span>
- <span data-ttu-id="67661-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="67661-124">DebugInfo</span></span>
- <span data-ttu-id="67661-125">İstatistik</span><span class="sxs-lookup"><span data-stu-id="67661-125">Statistics</span></span>
- <span data-ttu-id="67661-126">Tüm</span><span class="sxs-lookup"><span data-stu-id="67661-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="67661-127">-JobId</span></span>
<span data-ttu-id="67661-128">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="67661-129">-Name</span></span>
<span data-ttu-id="67661-130">İş listesi sonuçlarını filtrelemek için kullanılacak bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="67661-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="67661-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67661-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67661-132">None</span></span>
- <span data-ttu-id="67661-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="67661-133">DebugInfo</span></span>
- <span data-ttu-id="67661-134">İstatistik</span><span class="sxs-lookup"><span data-stu-id="67661-134">Statistics</span></span>
- <span data-ttu-id="67661-135">Tüm</span><span class="sxs-lookup"><span data-stu-id="67661-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-136">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="67661-136">-PipelineId</span></span>
<span data-ttu-id="67661-137">Belirtilen ardışık düzenin yalnızca işlerin bir bölümünü gösteren isteğe bağlı KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="67661-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="67661-138">-RecurrenceId</span></span>
<span data-ttu-id="67661-139">Yalnızca belirtilen yinelenme işlerinin bir bölümünü gösteren isteğe bağlı bir KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="67661-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-140">-Sonuç</span><span class="sxs-lookup"><span data-stu-id="67661-140">-Result</span></span>
<span data-ttu-id="67661-141">İş sonuçları için bir sonuç filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="67661-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="67661-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67661-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67661-143">None</span></span>
- <span data-ttu-id="67661-144">İptal</span><span class="sxs-lookup"><span data-stu-id="67661-144">Cancelled</span></span>
- <span data-ttu-id="67661-145">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="67661-145">Failed</span></span>
- <span data-ttu-id="67661-146">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="67661-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-147">Durumlu</span><span class="sxs-lookup"><span data-stu-id="67661-147">-State</span></span>
<span data-ttu-id="67661-148">İş sonuçları için bir durum filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="67661-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="67661-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67661-150">Benimsen</span><span class="sxs-lookup"><span data-stu-id="67661-150">Accepted</span></span>
- <span data-ttu-id="67661-151">Yeni</span><span class="sxs-lookup"><span data-stu-id="67661-151">New</span></span>
- <span data-ttu-id="67661-152">Derleyip</span><span class="sxs-lookup"><span data-stu-id="67661-152">Compiling</span></span>
- <span data-ttu-id="67661-153">Planlamayı</span><span class="sxs-lookup"><span data-stu-id="67661-153">Scheduling</span></span>
- <span data-ttu-id="67661-154">Sıradan</span><span class="sxs-lookup"><span data-stu-id="67661-154">Queued</span></span>
- <span data-ttu-id="67661-155">Başlarken</span><span class="sxs-lookup"><span data-stu-id="67661-155">Starting</span></span>
- <span data-ttu-id="67661-156">Dığında</span><span class="sxs-lookup"><span data-stu-id="67661-156">Paused</span></span>
- <span data-ttu-id="67661-157">Çalışması</span><span class="sxs-lookup"><span data-stu-id="67661-157">Running</span></span>
- <span data-ttu-id="67661-158">Sonlandırdı</span><span class="sxs-lookup"><span data-stu-id="67661-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="67661-159">-SubmittedAfter</span></span>
<span data-ttu-id="67661-160">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-160">Specifies a date filter.</span></span>
<span data-ttu-id="67661-161">İş listesi sonucuna belirtilen tarihten sonra gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="67661-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-162">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="67661-162">-SubmittedBefore</span></span>
<span data-ttu-id="67661-163">Bir tarih filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-163">Specifies a date filter.</span></span>
<span data-ttu-id="67661-164">İş listesi sonucuna belirtilen tarihten önce gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="67661-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-165">-Gönderenin</span><span class="sxs-lookup"><span data-stu-id="67661-165">-Submitter</span></span>
<span data-ttu-id="67661-166">Bir kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67661-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="67661-167">İş listesi sonuçlarını belirli bir kullanıcı tarafından gönderilen işlere filtre uygulamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="67661-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-168">-Üst</span><span class="sxs-lookup"><span data-stu-id="67661-168">-Top</span></span>
<span data-ttu-id="67661-169">Döndürülecek iş sayısını belirten isteğe bağlı bir değer.</span><span class="sxs-lookup"><span data-stu-id="67661-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="67661-170">Varsayılan değer 500</span><span class="sxs-lookup"><span data-stu-id="67661-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67661-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67661-171">CommonParameters</span></span>
<span data-ttu-id="67661-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67661-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67661-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67661-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67661-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67661-174">INPUTS</span></span>

### <span data-ttu-id="67661-175">'Sine</span><span class="sxs-lookup"><span data-stu-id="67661-175">Guid</span></span>
<span data-ttu-id="67661-176">' JobId ' parametresi ardışık düzenin ' Guid ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="67661-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="67661-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67661-177">OUTPUTS</span></span>

### <span data-ttu-id="67661-178">Jobınformation</span><span class="sxs-lookup"><span data-stu-id="67661-178">JobInformation</span></span>
<span data-ttu-id="67661-179">Belirtilen iş bilgileri ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="67661-179">The specified job information details</span></span>

### <span data-ttu-id="67661-180">Listeniz<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="67661-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="67661-181">Belirtilen veri Lake Analytics hesabındaki işlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="67661-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="67661-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67661-182">NOTES</span></span>

## <span data-ttu-id="67661-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67661-183">RELATED LINKS</span></span>

[<span data-ttu-id="67661-184">Stop-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="67661-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="67661-185">Submit-Azurermdatalakeanalyzer Ticsjob</span><span class="sxs-lookup"><span data-stu-id="67661-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="67661-186">Wait-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="67661-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


