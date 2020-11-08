---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105799"
---
# <span data-ttu-id="63d24-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="63d24-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="63d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d24-102">SYNOPSIS</span></span>
<span data-ttu-id="63d24-103">HTTP eylemine sahip bir zamanlayıcı işini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="63d24-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="63d24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63d24-104">SYNTAX</span></span>

### <span data-ttu-id="63d24-105">Gerekli</span><span class="sxs-lookup"><span data-stu-id="63d24-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="63d24-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="63d24-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63d24-107">Günlük</span><span class="sxs-lookup"><span data-stu-id="63d24-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63d24-108">Doðrulamasý</span><span class="sxs-lookup"><span data-stu-id="63d24-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63d24-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="63d24-109">DESCRIPTION</span></span>
<span data-ttu-id="63d24-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="63d24-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="63d24-111">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="63d24-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="63d24-112">**Set-AzureSchedulerHttpJob** cmdlet 'ı, http eylemi olan bir zamanlayıcı işini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="63d24-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="63d24-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63d24-113">EXAMPLES</span></span>

### <span data-ttu-id="63d24-114">Örnek 1: işin durumunu devre dışı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="63d24-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="63d24-115">Bu komut, Job01 adındaki işin durumunu devre dışı olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="63d24-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="63d24-116">Bu iş, belirtilen konum için JobColleciton01 adlı iş koleksiyonunun bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="63d24-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="63d24-117">Örnek 2: işin URI 'sini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="63d24-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="63d24-118">Bu komut, Job01 adındaki işin URI 'sini güncelleştirir http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="63d24-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="63d24-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63d24-119">PARAMETERS</span></span>

### <span data-ttu-id="63d24-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="63d24-120">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="63d24-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="63d24-121">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="63d24-122">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="63d24-122">-EndTime</span></span>
<span data-ttu-id="63d24-123">Zamanlayıcı 'nın işleri başlatma işlemini durdurması için bir saat **Tarih saat** değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="63d24-124">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="63d24-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="63d24-125">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="63d24-125">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="63d24-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="63d24-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="63d24-127">Üst bilgileri bir Hashtable olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="63d24-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="63d24-128">-ErrorActionMethod</span></span>
<span data-ttu-id="63d24-129">HTTP ve HTTPS eylem türleri için yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="63d24-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="63d24-130">Valid values are:</span></span> 

- <span data-ttu-id="63d24-131">Al</span><span class="sxs-lookup"><span data-stu-id="63d24-131">GET</span></span>
- <span data-ttu-id="63d24-132">KOYUL</span><span class="sxs-lookup"><span data-stu-id="63d24-132">PUT</span></span>
- <span data-ttu-id="63d24-133">Yayınla</span><span class="sxs-lookup"><span data-stu-id="63d24-133">POST</span></span>
- <span data-ttu-id="63d24-134">IMıN</span><span class="sxs-lookup"><span data-stu-id="63d24-134">HEAD</span></span>
- <span data-ttu-id="63d24-135">SILME</span><span class="sxs-lookup"><span data-stu-id="63d24-135">DELETE</span></span>

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

### <span data-ttu-id="63d24-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="63d24-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="63d24-137">Depolama iş eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="63d24-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="63d24-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="63d24-139">İş gönderme ve gönderme eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="63d24-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="63d24-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="63d24-141">Depolama sırasının paylaşılan erişim Imzası (SAS) belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="63d24-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63d24-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="63d24-143">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="63d24-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="63d24-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="63d24-145">Depolama sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="63d24-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="63d24-146">-ErrorActionURI</span></span>
<span data-ttu-id="63d24-147">Hata işi eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="63d24-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="63d24-148">-ExecutionCount</span></span>
<span data-ttu-id="63d24-149">Çalışan bir işin numara yinelenme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="63d24-150">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="63d24-150">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="63d24-151">Frekans</span><span class="sxs-lookup"><span data-stu-id="63d24-151">-Frequency</span></span>
<span data-ttu-id="63d24-152">Bu Zamanlayıcı işinin en yüksek frekansını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-152">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="63d24-153">-Üstbilgiler</span><span class="sxs-lookup"><span data-stu-id="63d24-153">-Headers</span></span>
<span data-ttu-id="63d24-154">Üst bilgileri karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="63d24-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="63d24-155">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="63d24-156">-Aralık</span><span class="sxs-lookup"><span data-stu-id="63d24-156">-Interval</span></span>
<span data-ttu-id="63d24-157">*Sıklık* parametresini kullanarak belirtilen sıklıkta yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="63d24-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="63d24-158">-JobCollectionName</span></span>
<span data-ttu-id="63d24-159">Değiştirilecek zamanlayıcı işini içeren koleksiyonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="63d24-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="63d24-160">-JobName</span></span>
<span data-ttu-id="63d24-161">Değiştirilecek zamanlayıcı işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="63d24-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="63d24-162">-JobState</span></span>
<span data-ttu-id="63d24-163">Zamanlayıcı işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="63d24-164">-Konum</span><span class="sxs-lookup"><span data-stu-id="63d24-164">-Location</span></span>
<span data-ttu-id="63d24-165">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="63d24-166">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="63d24-166">Valid values are:</span></span> 

- <span data-ttu-id="63d24-167">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="63d24-167">Anywhere Asia</span></span>
- <span data-ttu-id="63d24-168">Her yerde</span><span class="sxs-lookup"><span data-stu-id="63d24-168">Anywhere Europe</span></span>
- <span data-ttu-id="63d24-169">Her yerde</span><span class="sxs-lookup"><span data-stu-id="63d24-169">Anywhere US</span></span>
- <span data-ttu-id="63d24-170">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="63d24-170">East Asia</span></span>
- <span data-ttu-id="63d24-171">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="63d24-171">East US</span></span>
- <span data-ttu-id="63d24-172">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="63d24-172">North Central US</span></span>
- <span data-ttu-id="63d24-173">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="63d24-173">North Europe</span></span>
- <span data-ttu-id="63d24-174">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="63d24-174">South Central US</span></span>
- <span data-ttu-id="63d24-175">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="63d24-175">Southeast Asia</span></span>
- <span data-ttu-id="63d24-176">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="63d24-176">West Europe</span></span>
- <span data-ttu-id="63d24-177">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="63d24-177">West US</span></span>

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

### <span data-ttu-id="63d24-178">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="63d24-178">-Method</span></span>
<span data-ttu-id="63d24-179">HTTP ve HTTPS eylem türleri için yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="63d24-180">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="63d24-180">Valid values are:</span></span> 

- <span data-ttu-id="63d24-181">Al</span><span class="sxs-lookup"><span data-stu-id="63d24-181">GET</span></span>
- <span data-ttu-id="63d24-182">KOYUL</span><span class="sxs-lookup"><span data-stu-id="63d24-182">PUT</span></span>
- <span data-ttu-id="63d24-183">Yayınla</span><span class="sxs-lookup"><span data-stu-id="63d24-183">POST</span></span>
- <span data-ttu-id="63d24-184">IMıN</span><span class="sxs-lookup"><span data-stu-id="63d24-184">HEAD</span></span>
- <span data-ttu-id="63d24-185">SILME</span><span class="sxs-lookup"><span data-stu-id="63d24-185">DELETE</span></span>

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

### <span data-ttu-id="63d24-186">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="63d24-186">-PassThru</span></span>
<span data-ttu-id="63d24-187">Bu cmdlet 'in, üzerinde işlem yaptığı öğeyi temsil eden bir nesne döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="63d24-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="63d24-188">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="63d24-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63d24-189">-Profil</span><span class="sxs-lookup"><span data-stu-id="63d24-189">-Profile</span></span>
<span data-ttu-id="63d24-190">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63d24-191">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="63d24-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63d24-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="63d24-192">-RequestBody</span></span>
<span data-ttu-id="63d24-193">İş gönderme ve gönderme eylemlerinin gövdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-193">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="63d24-194">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="63d24-194">-StartTime</span></span>
<span data-ttu-id="63d24-195">İşin başlaması için bir **saat bir saat** değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="63d24-196">-URI</span><span class="sxs-lookup"><span data-stu-id="63d24-196">-URI</span></span>
<span data-ttu-id="63d24-197">İş eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63d24-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="63d24-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d24-198">CommonParameters</span></span>
<span data-ttu-id="63d24-199">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63d24-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d24-200">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63d24-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d24-201">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63d24-201">INPUTS</span></span>

## <span data-ttu-id="63d24-202">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63d24-202">OUTPUTS</span></span>

## <span data-ttu-id="63d24-203">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63d24-203">NOTES</span></span>

## <span data-ttu-id="63d24-204">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63d24-204">RELATED LINKS</span></span>

[<span data-ttu-id="63d24-205">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="63d24-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


