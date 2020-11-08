---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105902"
---
# <span data-ttu-id="79689-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="79689-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="79689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79689-102">SYNOPSIS</span></span>
<span data-ttu-id="79689-103">Depolama eylemi olan bir zamanlayıcı işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79689-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="79689-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79689-104">SYNTAX</span></span>

### <span data-ttu-id="79689-105">Gerekli</span><span class="sxs-lookup"><span data-stu-id="79689-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="79689-106">Günlük</span><span class="sxs-lookup"><span data-stu-id="79689-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="79689-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79689-107">DESCRIPTION</span></span>
<span data-ttu-id="79689-108">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="79689-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="79689-109">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="79689-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="79689-110">**New-AzureSchedulerStorageQueueJob** cmdlet 'ı Azure depolama eylemi olan bir zamanlayıcı işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79689-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="79689-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79689-111">EXAMPLES</span></span>

### <span data-ttu-id="79689-112">Örnek 1: bir kez çalışan bir depolama işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="79689-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="79689-113">Bu komut, JobCollection01 adlı koleksiyonun bir parçası olarak bir Zamanlayıcı depolama işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79689-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="79689-114">Bu komut depolama hesabını, kuyruk adını ve SAS belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="79689-115">İş, hemen bir kez çalışır.</span><span class="sxs-lookup"><span data-stu-id="79689-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="79689-116">Örnek 2: belirtilen sayıda çalışan bir depolama işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="79689-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="79689-117">Bu komut, JobCollection01 adlı koleksiyonun bir parçası olarak bir Zamanlayıcı depolama işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79689-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="79689-118">Bu komut depolama hesabını, kuyruk adını ve SAS belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="79689-119">İş her saatte iki kez 20 kez çalışır.</span><span class="sxs-lookup"><span data-stu-id="79689-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="79689-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79689-120">PARAMETERS</span></span>

### <span data-ttu-id="79689-121">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="79689-121">-EndTime</span></span>
<span data-ttu-id="79689-122">Zamanlayıcı işinin başlatılmasına engel olacak şekilde **bir saat**</span><span class="sxs-lookup"><span data-stu-id="79689-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="79689-123">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79689-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="79689-124">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="79689-124">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="79689-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="79689-126">Üst bilgileri karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-126">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="79689-127">-ErrorActionMethod</span></span>
<span data-ttu-id="79689-128">HTTP ve HTTPS eylem türleri için yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="79689-129">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="79689-129">Valid values are:</span></span> 

- <span data-ttu-id="79689-130">Al</span><span class="sxs-lookup"><span data-stu-id="79689-130">GET</span></span>
- <span data-ttu-id="79689-131">KOYUL</span><span class="sxs-lookup"><span data-stu-id="79689-131">PUT</span></span>
- <span data-ttu-id="79689-132">Yayınla</span><span class="sxs-lookup"><span data-stu-id="79689-132">POST</span></span>
- <span data-ttu-id="79689-133">IMıN</span><span class="sxs-lookup"><span data-stu-id="79689-133">HEAD</span></span>
- <span data-ttu-id="79689-134">SILME</span><span class="sxs-lookup"><span data-stu-id="79689-134">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="79689-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="79689-136">Depolama iş eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-136">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="79689-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="79689-138">İş gönderme ve gönderme eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-138">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="79689-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="79689-140">Depolama sırasının paylaşılan erişim Imzası (SAS) belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79689-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="79689-142">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-142">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="79689-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="79689-144">Depolama sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-144">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="79689-145">-ErrorActionURI</span></span>
<span data-ttu-id="79689-146">Hata işi eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-146">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="79689-147">-ExecutionCount</span></span>
<span data-ttu-id="79689-148">Çalışan bir işin numara yinelenme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="79689-149">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="79689-149">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-150">Frekans</span><span class="sxs-lookup"><span data-stu-id="79689-150">-Frequency</span></span>
<span data-ttu-id="79689-151">Bu Zamanlayıcı işinin en yüksek frekansını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="79689-152">-Aralık</span><span class="sxs-lookup"><span data-stu-id="79689-152">-Interval</span></span>
<span data-ttu-id="79689-153">*Sıklık* parametresini kullanarak belirtilen sıklıkta yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="79689-154">-JobCollectionName</span></span>
<span data-ttu-id="79689-155">Zamanlayıcı işini içerecek koleksiyonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-155">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="79689-156">-JobName</span></span>
<span data-ttu-id="79689-157">Zamanlayıcı işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-157">Specifies the name for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="79689-158">-JobState</span></span>
<span data-ttu-id="79689-159">Zamanlayıcı işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-159">Specifies the state for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-160">-Konum</span><span class="sxs-lookup"><span data-stu-id="79689-160">-Location</span></span>
<span data-ttu-id="79689-161">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="79689-162">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="79689-162">Valid values are:</span></span> 

- <span data-ttu-id="79689-163">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="79689-163">Anywhere Asia</span></span>
- <span data-ttu-id="79689-164">Her yerde</span><span class="sxs-lookup"><span data-stu-id="79689-164">Anywhere Europe</span></span>
- <span data-ttu-id="79689-165">Her yerde</span><span class="sxs-lookup"><span data-stu-id="79689-165">Anywhere US</span></span>
- <span data-ttu-id="79689-166">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="79689-166">East Asia</span></span>
- <span data-ttu-id="79689-167">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="79689-167">East US</span></span>
- <span data-ttu-id="79689-168">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="79689-168">North Central US</span></span>
- <span data-ttu-id="79689-169">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="79689-169">North Europe</span></span>
- <span data-ttu-id="79689-170">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="79689-170">South Central US</span></span>
- <span data-ttu-id="79689-171">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="79689-171">Southeast Asia</span></span>
- <span data-ttu-id="79689-172">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="79689-172">West Europe</span></span>
- <span data-ttu-id="79689-173">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="79689-173">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-174">-Profil</span><span class="sxs-lookup"><span data-stu-id="79689-174">-Profile</span></span>
<span data-ttu-id="79689-175">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79689-176">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="79689-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79689-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="79689-177">-SASToken</span></span>
<span data-ttu-id="79689-178">Depolama sırasının SAS belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-178">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-179">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="79689-179">-StartTime</span></span>
<span data-ttu-id="79689-180">İşin başlaması için bir **saat bir saat** değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79689-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="79689-181">-StorageQueueAccount</span></span>
<span data-ttu-id="79689-182">Depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-182">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="79689-183">-StorageQueueMessage</span></span>
<span data-ttu-id="79689-184">Depolama işinin kuyruk iletisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="79689-185">-Storagesıraadı</span><span class="sxs-lookup"><span data-stu-id="79689-185">-StorageQueueName</span></span>
<span data-ttu-id="79689-186">Depolama sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79689-186">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79689-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79689-187">CommonParameters</span></span>
<span data-ttu-id="79689-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79689-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79689-189">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79689-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79689-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79689-190">INPUTS</span></span>

## <span data-ttu-id="79689-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79689-191">OUTPUTS</span></span>

## <span data-ttu-id="79689-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79689-192">NOTES</span></span>

## <span data-ttu-id="79689-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79689-193">RELATED LINKS</span></span>

[<span data-ttu-id="79689-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="79689-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


