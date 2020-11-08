---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106050"
---
# <span data-ttu-id="17b66-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="17b66-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="17b66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b66-102">SYNOPSIS</span></span>
<span data-ttu-id="17b66-103">Depolama eylemi olan bir zamanlayıcı işini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="17b66-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="17b66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17b66-104">SYNTAX</span></span>

### <span data-ttu-id="17b66-105">Gerekli</span><span class="sxs-lookup"><span data-stu-id="17b66-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="17b66-106">Günlük</span><span class="sxs-lookup"><span data-stu-id="17b66-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="17b66-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="17b66-107">DESCRIPTION</span></span>
<span data-ttu-id="17b66-108">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="17b66-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="17b66-109">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="17b66-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="17b66-110">**Set-AzureSchedulerStorageQueueJob** cmdlet 'ı, Azure depolama eylemi olan bir zamanlayıcı işini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="17b66-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="17b66-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17b66-111">EXAMPLES</span></span>

### <span data-ttu-id="17b66-112">Örnek 1: depolama sırası iletisini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="17b66-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="17b66-113">Bu komut, Job12 adındaki depolama işinin sıra iletisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="17b66-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="17b66-114">Komut, iş koleksiyonu adını ve konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="17b66-115">Örnek 2: depolama sırası işini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="17b66-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="17b66-116">Bu komut, Job16 adlı işi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="17b66-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="17b66-117">Komut, *JobState* parametresi için bu değeri belirterek Işin durumunu etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="17b66-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="17b66-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17b66-118">PARAMETERS</span></span>

### <span data-ttu-id="17b66-119">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="17b66-119">-EndTime</span></span>
<span data-ttu-id="17b66-120">Zamanlayıcı işinin başlatılmasına engel olacak şekilde **bir saat**</span><span class="sxs-lookup"><span data-stu-id="17b66-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="17b66-121">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17b66-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="17b66-122">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="17b66-122">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="17b66-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="17b66-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="17b66-124">Üst bilgileri karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-124">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="17b66-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="17b66-125">-ErrorActionMethod</span></span>
<span data-ttu-id="17b66-126">HTTP ve HTTPS eylem türleri için yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="17b66-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="17b66-127">Valid values are:</span></span> 

- <span data-ttu-id="17b66-128">Al</span><span class="sxs-lookup"><span data-stu-id="17b66-128">GET</span></span>
- <span data-ttu-id="17b66-129">KOYUL</span><span class="sxs-lookup"><span data-stu-id="17b66-129">PUT</span></span>
- <span data-ttu-id="17b66-130">Yayınla</span><span class="sxs-lookup"><span data-stu-id="17b66-130">POST</span></span>
- <span data-ttu-id="17b66-131">IMıN</span><span class="sxs-lookup"><span data-stu-id="17b66-131">HEAD</span></span>
- <span data-ttu-id="17b66-132">SILME</span><span class="sxs-lookup"><span data-stu-id="17b66-132">DELETE</span></span>

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

### <span data-ttu-id="17b66-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="17b66-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="17b66-134">Depolama iş eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-134">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="17b66-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="17b66-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="17b66-136">İş gönderme ve gönderme eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-136">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="17b66-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="17b66-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="17b66-138">Depolama sırasının paylaşılan erişim Imzası (SAS) belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="17b66-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17b66-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="17b66-140">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-140">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="17b66-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="17b66-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="17b66-142">Depolama sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-142">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="17b66-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="17b66-143">-ErrorActionURI</span></span>
<span data-ttu-id="17b66-144">Hata işi eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-144">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="17b66-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="17b66-145">-ExecutionCount</span></span>
<span data-ttu-id="17b66-146">Çalışan bir işin numara yinelenme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="17b66-147">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="17b66-147">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="17b66-148">Frekans</span><span class="sxs-lookup"><span data-stu-id="17b66-148">-Frequency</span></span>
<span data-ttu-id="17b66-149">Bu Zamanlayıcı işinin en yüksek frekansını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-149">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="17b66-150">-Aralık</span><span class="sxs-lookup"><span data-stu-id="17b66-150">-Interval</span></span>
<span data-ttu-id="17b66-151">*Sıklık* parametresini kullanarak belirtilen sıklıkta yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="17b66-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="17b66-152">-JobCollectionName</span></span>
<span data-ttu-id="17b66-153">Zamanlayıcı işini içerecek koleksiyonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-153">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="17b66-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="17b66-154">-JobName</span></span>
<span data-ttu-id="17b66-155">Güncelleştirilecek zamanlayıcı işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-155">Specifies the name of the scheduler job to update.</span></span>

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

### <span data-ttu-id="17b66-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="17b66-156">-JobState</span></span>
<span data-ttu-id="17b66-157">Zamanlayıcı işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-157">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="17b66-158">-Konum</span><span class="sxs-lookup"><span data-stu-id="17b66-158">-Location</span></span>
<span data-ttu-id="17b66-159">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="17b66-160">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="17b66-160">Valid values are:</span></span> 

- <span data-ttu-id="17b66-161">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="17b66-161">Anywhere Asia</span></span>
- <span data-ttu-id="17b66-162">Her yerde</span><span class="sxs-lookup"><span data-stu-id="17b66-162">Anywhere Europe</span></span>
- <span data-ttu-id="17b66-163">Her yerde</span><span class="sxs-lookup"><span data-stu-id="17b66-163">Anywhere US</span></span>
- <span data-ttu-id="17b66-164">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="17b66-164">East Asia</span></span>
- <span data-ttu-id="17b66-165">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="17b66-165">East US</span></span>
- <span data-ttu-id="17b66-166">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="17b66-166">North Central US</span></span>
- <span data-ttu-id="17b66-167">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="17b66-167">North Europe</span></span>
- <span data-ttu-id="17b66-168">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="17b66-168">South Central US</span></span>
- <span data-ttu-id="17b66-169">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="17b66-169">Southeast Asia</span></span>
- <span data-ttu-id="17b66-170">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="17b66-170">West Europe</span></span>
- <span data-ttu-id="17b66-171">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="17b66-171">West US</span></span>

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

### <span data-ttu-id="17b66-172">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="17b66-172">-PassThru</span></span>
<span data-ttu-id="17b66-173">Bu cmdlet 'in, üzerinde işlem yaptığı öğeyi temsil eden bir nesne döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="17b66-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="17b66-174">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="17b66-174">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b66-175">-Profil</span><span class="sxs-lookup"><span data-stu-id="17b66-175">-Profile</span></span>
<span data-ttu-id="17b66-176">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17b66-177">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="17b66-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17b66-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="17b66-178">-SASToken</span></span>
<span data-ttu-id="17b66-179">Depolama sırasının SAS belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-179">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="17b66-180">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="17b66-180">-StartTime</span></span>
<span data-ttu-id="17b66-181">İşin başlaması için bir **saat bir saat** değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="17b66-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="17b66-182">-StorageQueueAccount</span></span>
<span data-ttu-id="17b66-183">Depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-183">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="17b66-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="17b66-184">-StorageQueueMessage</span></span>
<span data-ttu-id="17b66-185">Depolama işinin sıra iletisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-185">Specifies the queue message for the Storage job.</span></span>

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

### <span data-ttu-id="17b66-186">-Storagesıraadı</span><span class="sxs-lookup"><span data-stu-id="17b66-186">-StorageQueueName</span></span>
<span data-ttu-id="17b66-187">Depolama sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17b66-187">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="17b66-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b66-188">CommonParameters</span></span>
<span data-ttu-id="17b66-189">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17b66-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b66-190">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b66-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b66-191">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17b66-191">INPUTS</span></span>

## <span data-ttu-id="17b66-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17b66-192">OUTPUTS</span></span>

## <span data-ttu-id="17b66-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17b66-193">NOTES</span></span>

## <span data-ttu-id="17b66-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17b66-194">RELATED LINKS</span></span>

[<span data-ttu-id="17b66-195">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="17b66-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


