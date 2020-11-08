---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105904"
---
# <span data-ttu-id="8b67d-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8b67d-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="8b67d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b67d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b67d-103">HTTP eylemi olan bir zamanlayıcı işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b67d-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="8b67d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b67d-104">SYNTAX</span></span>

### <span data-ttu-id="8b67d-105">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8b67d-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b67d-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="8b67d-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8b67d-107">Günlük</span><span class="sxs-lookup"><span data-stu-id="8b67d-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8b67d-108">Doðrulamasý</span><span class="sxs-lookup"><span data-stu-id="8b67d-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8b67d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b67d-109">DESCRIPTION</span></span>
<span data-ttu-id="8b67d-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8b67d-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8b67d-111">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8b67d-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8b67d-112">**New-AzureSchedulerHttpJob** CMDLET 'i http eylemi olan bir zamanlayıcı işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b67d-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="8b67d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b67d-113">EXAMPLES</span></span>

### <span data-ttu-id="8b67d-114">Örnek 1: HTTP işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b67d-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="8b67d-115">Bu komut, JobCollection01 adlı iş koleksiyonunda bir Zamanlayıcı HTTP işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b67d-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="8b67d-116">Komut bir URI belirtir ve yöntem olarak GET ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="8b67d-117">Örnek 2: belirli bir çalışma sayısı için bir HTTP işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b67d-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="8b67d-118">Bu komut, JobCollection01 adlı iş koleksiyonunda Scheduler http işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b67d-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="8b67d-119">Komut bir URI belirtir ve yöntem olarak GET ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="8b67d-120">Bu komut, işin 20 kez çalışmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="8b67d-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="8b67d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b67d-121">PARAMETERS</span></span>

### <span data-ttu-id="8b67d-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8b67d-122">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="8b67d-123">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-124">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="8b67d-124">-EndTime</span></span>
<span data-ttu-id="8b67d-125">Zamanlayıcı 'nın işleri başlatma işlemini durdurması için bir saat **Tarih saat** değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="8b67d-126">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8b67d-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="8b67d-127">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8b67d-127">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="8b67d-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="8b67d-129">Üst bilgileri bir Hashtable olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="8b67d-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="8b67d-130">-ErrorActionMethod</span></span>
<span data-ttu-id="8b67d-131">HTTP ve HTTPS eylem türleri için yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="8b67d-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8b67d-132">Valid values are:</span></span> 

- <span data-ttu-id="8b67d-133">Al</span><span class="sxs-lookup"><span data-stu-id="8b67d-133">GET</span></span>
- <span data-ttu-id="8b67d-134">KOYUL</span><span class="sxs-lookup"><span data-stu-id="8b67d-134">PUT</span></span>
- <span data-ttu-id="8b67d-135">Yayınla</span><span class="sxs-lookup"><span data-stu-id="8b67d-135">POST</span></span>
- <span data-ttu-id="8b67d-136">IMıN</span><span class="sxs-lookup"><span data-stu-id="8b67d-136">HEAD</span></span>
- <span data-ttu-id="8b67d-137">SILME</span><span class="sxs-lookup"><span data-stu-id="8b67d-137">DELETE</span></span>

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

### <span data-ttu-id="8b67d-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="8b67d-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="8b67d-139">Depolama iş eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="8b67d-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="8b67d-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="8b67d-141">İş gönderme ve gönderme eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="8b67d-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="8b67d-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="8b67d-143">Depolama sırasının paylaşılan erişim Imzası (SAS) belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="8b67d-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b67d-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="8b67d-145">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="8b67d-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8b67d-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="8b67d-147">Depolama sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="8b67d-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="8b67d-148">-ErrorActionURI</span></span>
<span data-ttu-id="8b67d-149">Hata işi eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="8b67d-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="8b67d-150">-ExecutionCount</span></span>
<span data-ttu-id="8b67d-151">Çalışan bir işin numara yinelenme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="8b67d-152">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-152">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-153">Frekans</span><span class="sxs-lookup"><span data-stu-id="8b67d-153">-Frequency</span></span>
<span data-ttu-id="8b67d-154">Bu Zamanlayıcı işinin en yüksek frekansını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-154">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-155">-Üstbilgiler</span><span class="sxs-lookup"><span data-stu-id="8b67d-155">-Headers</span></span>
<span data-ttu-id="8b67d-156">Üst bilgileri karma olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="8b67d-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8b67d-157">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-158">-Aralık</span><span class="sxs-lookup"><span data-stu-id="8b67d-158">-Interval</span></span>
<span data-ttu-id="8b67d-159">*Sıklık* parametresini kullanarak belirtilen sıklıkta yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8b67d-160">-JobCollectionName</span></span>
<span data-ttu-id="8b67d-161">Zamanlayıcı işini içerecek koleksiyonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="8b67d-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="8b67d-162">-JobName</span></span>
<span data-ttu-id="8b67d-163">Zamanlayıcı işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="8b67d-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="8b67d-164">-JobState</span></span>
<span data-ttu-id="8b67d-165">Zamanlayıcı işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="8b67d-166">-Konum</span><span class="sxs-lookup"><span data-stu-id="8b67d-166">-Location</span></span>
<span data-ttu-id="8b67d-167">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="8b67d-168">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8b67d-168">Valid values are:</span></span> 

- <span data-ttu-id="8b67d-169">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="8b67d-169">Anywhere Asia</span></span>
- <span data-ttu-id="8b67d-170">Her yerde</span><span class="sxs-lookup"><span data-stu-id="8b67d-170">Anywhere Europe</span></span>
- <span data-ttu-id="8b67d-171">Her yerde</span><span class="sxs-lookup"><span data-stu-id="8b67d-171">Anywhere US</span></span>
- <span data-ttu-id="8b67d-172">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="8b67d-172">East Asia</span></span>
- <span data-ttu-id="8b67d-173">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="8b67d-173">East US</span></span>
- <span data-ttu-id="8b67d-174">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="8b67d-174">North Central US</span></span>
- <span data-ttu-id="8b67d-175">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="8b67d-175">North Europe</span></span>
- <span data-ttu-id="8b67d-176">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="8b67d-176">South Central US</span></span>
- <span data-ttu-id="8b67d-177">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="8b67d-177">Southeast Asia</span></span>
- <span data-ttu-id="8b67d-178">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="8b67d-178">West Europe</span></span>
- <span data-ttu-id="8b67d-179">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="8b67d-179">West US</span></span>

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

### <span data-ttu-id="8b67d-180">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="8b67d-180">-Method</span></span>
<span data-ttu-id="8b67d-181">HTTP ve HTTPS eylem türleri için yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="8b67d-182">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8b67d-182">Valid values are:</span></span> 

- <span data-ttu-id="8b67d-183">Al</span><span class="sxs-lookup"><span data-stu-id="8b67d-183">GET</span></span>
- <span data-ttu-id="8b67d-184">KOYUL</span><span class="sxs-lookup"><span data-stu-id="8b67d-184">PUT</span></span>
- <span data-ttu-id="8b67d-185">Yayınla</span><span class="sxs-lookup"><span data-stu-id="8b67d-185">POST</span></span>
- <span data-ttu-id="8b67d-186">IMıN</span><span class="sxs-lookup"><span data-stu-id="8b67d-186">HEAD</span></span>
- <span data-ttu-id="8b67d-187">SILME</span><span class="sxs-lookup"><span data-stu-id="8b67d-187">DELETE</span></span>

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

### <span data-ttu-id="8b67d-188">-Profil</span><span class="sxs-lookup"><span data-stu-id="8b67d-188">-Profile</span></span>
<span data-ttu-id="8b67d-189">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8b67d-190">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8b67d-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8b67d-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="8b67d-191">-RequestBody</span></span>
<span data-ttu-id="8b67d-192">İş gönderme ve gönderme eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-192">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-193">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="8b67d-193">-StartTime</span></span>
<span data-ttu-id="8b67d-194">İşin başlaması için bir **saat bir saat** değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="8b67d-195">-URI</span><span class="sxs-lookup"><span data-stu-id="8b67d-195">-URI</span></span>
<span data-ttu-id="8b67d-196">İş eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b67d-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b67d-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b67d-197">CommonParameters</span></span>
<span data-ttu-id="8b67d-198">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b67d-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b67d-199">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b67d-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b67d-200">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b67d-200">INPUTS</span></span>

## <span data-ttu-id="8b67d-201">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b67d-201">OUTPUTS</span></span>

## <span data-ttu-id="8b67d-202">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b67d-202">NOTES</span></span>

## <span data-ttu-id="8b67d-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b67d-203">RELATED LINKS</span></span>

[<span data-ttu-id="8b67d-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8b67d-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


