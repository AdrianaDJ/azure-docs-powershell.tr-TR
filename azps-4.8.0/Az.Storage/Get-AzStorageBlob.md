---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266262"
---
# <span data-ttu-id="42abc-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="42abc-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="42abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42abc-102">SYNOPSIS</span></span>
<span data-ttu-id="42abc-103">Kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="42abc-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="42abc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42abc-104">SYNTAX</span></span>

### <span data-ttu-id="42abc-105">BlobName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42abc-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="42abc-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="42abc-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="42abc-107">Singleblobversionıd</span><span class="sxs-lookup"><span data-stu-id="42abc-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="42abc-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="42abc-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="42abc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="42abc-109">DESCRIPTION</span></span>
<span data-ttu-id="42abc-110">**Get-AzStorageBlob** cmdlet 'ı bir Azure depolama hesabında belirtilen kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="42abc-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="42abc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42abc-111">EXAMPLES</span></span>

### <span data-ttu-id="42abc-112">Örnek 1: blob adına göre blob alma</span><span class="sxs-lookup"><span data-stu-id="42abc-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="42abc-113">Bu komut, blob almak için blob adı ve joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="42abc-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="42abc-114">Örnek 2: ardışık düzeni kullanarak kapsayıcıda blob alma</span><span class="sxs-lookup"><span data-stu-id="42abc-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="42abc-115">Bu komut, bir kapsayıcıya tüm blob 'ları (silinmiş durumda blob 'ları ekleme) almak için ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="42abc-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="42abc-116">Örnek 3: ad önekine göre blob alma</span><span class="sxs-lookup"><span data-stu-id="42abc-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="42abc-117">Bu komut, blob almak için bir ad öneki kullanır.</span><span class="sxs-lookup"><span data-stu-id="42abc-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="42abc-118">Örnek 4: çoklu toplu işlemlerdeki blob 'ları listeleme</span><span class="sxs-lookup"><span data-stu-id="42abc-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="42abc-119">Bu örnekte, Azure depolama bloblarını birden çok toplu işlem halinde listelemek için *maxCount* ve *continuationtoken* parametreleri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="42abc-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="42abc-120">İlk dört komut, örnekte kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="42abc-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="42abc-121">Beşinci komut, blob almak için **Get-AzStorageBlob** cmdlet 'Ini kullanan **do-while** deyimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="42abc-122">Bu ifadede $Token değişkeninde depolanan devam belirteci yer alır.</span><span class="sxs-lookup"><span data-stu-id="42abc-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="42abc-123">Döngü çalışırken $Token değişir.</span><span class="sxs-lookup"><span data-stu-id="42abc-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="42abc-124">Daha fazla bilgi için yazın `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="42abc-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="42abc-125">Final komutu, toplam görüntülemek için **echo** komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="42abc-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="42abc-126">Örnek 5: kapsayıcıdaki tüm blob 'ları alma blob sürümünü içerir</span><span class="sxs-lookup"><span data-stu-id="42abc-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="42abc-127">Bu komut, bir kapsayıcıdaki tüm blob 'ları blob sürümü içerir.</span><span class="sxs-lookup"><span data-stu-id="42abc-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="42abc-128">Örnek 6: tek blob sürümü alma</span><span class="sxs-lookup"><span data-stu-id="42abc-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="42abc-129">Bu komut, VersionId ile tek bir blob veri'si alır.</span><span class="sxs-lookup"><span data-stu-id="42abc-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="42abc-130">Örnek 7: tek bir blob anlık görüntüsü alın</span><span class="sxs-lookup"><span data-stu-id="42abc-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="42abc-131">Bu komut, SnapshotTime ile tek bir blob anlık görüntüsü alır.</span><span class="sxs-lookup"><span data-stu-id="42abc-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="42abc-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42abc-132">PARAMETERS</span></span>

### <span data-ttu-id="42abc-133">-Blob</span><span class="sxs-lookup"><span data-stu-id="42abc-133">-Blob</span></span>
<span data-ttu-id="42abc-134">Joker karakter aramasında kullanılabilecek ad veya ad desenini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="42abc-135">Blob adı belirtilmezse cmdlet, belirtilen kapsayıcıdaki tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="42abc-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="42abc-136">Bu parametre için bir değer belirtilmişse cmdlet, Bu parametreyle eşleşen adlara sahip tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="42abc-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="42abc-137">Bu parametre, dizede herhangi bir yerde joker karakterini destekler.</span><span class="sxs-lookup"><span data-stu-id="42abc-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="42abc-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="42abc-139">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="42abc-140">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="42abc-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="42abc-141">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="42abc-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="42abc-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="42abc-143">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="42abc-144">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42abc-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="42abc-145">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="42abc-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="42abc-146">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="42abc-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="42abc-147">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="42abc-147">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-148">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="42abc-148">-Container</span></span>
<span data-ttu-id="42abc-149">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-149">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-150">-Context</span><span class="sxs-lookup"><span data-stu-id="42abc-150">-Context</span></span>
<span data-ttu-id="42abc-151">Blob listesi almak istediğiniz Azure Depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="42abc-152">Depolama bağlamı oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42abc-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="42abc-153">-ContinuationToken</span></span>
<span data-ttu-id="42abc-154">Blob listesi için bir devam belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="42abc-155">Birden çok toplu işlemdeki blob 'ları listelemek için bu parametreyi ve *maxCount* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="42abc-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42abc-156">-DefaultProfile</span></span>
<span data-ttu-id="42abc-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42abc-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-158">-Includedeleted</span><span class="sxs-lookup"><span data-stu-id="42abc-158">-IncludeDeleted</span></span>
<span data-ttu-id="42abc-159">Silinmiş blob 'u içer varsayılan olarak blob silinmiş blob 'u içermez.</span><span class="sxs-lookup"><span data-stu-id="42abc-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-160">-Includeversion</span><span class="sxs-lookup"><span data-stu-id="42abc-160">-IncludeVersion</span></span>
<span data-ttu-id="42abc-161">Blob sürümleri yalnızca bu parametre mevcutsa, varsayılan olarak blob 'un blob sürümlerini içermeyecektir.</span><span class="sxs-lookup"><span data-stu-id="42abc-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="42abc-162">-MaxCount</span></span>
<span data-ttu-id="42abc-163">Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-164">-Önek</span><span class="sxs-lookup"><span data-stu-id="42abc-164">-Prefix</span></span>
<span data-ttu-id="42abc-165">Almak istediğiniz blob adları için bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="42abc-166">Bu parametre, aramada normal ifadeler veya joker karakterler kullanılmasını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="42abc-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="42abc-167">Bu, kapsayıcıda yalnızca "My", "MyBlob1" ve "MyBlob2" adlı blob varsa ve "-prefix My \*" ifadesini belirtirseniz, cmdlet hiçbir blob döndürmez.</span><span class="sxs-lookup"><span data-stu-id="42abc-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="42abc-168">Ancak, "-önek" ifadesini belirtirseniz cmdlet, "benim", "MyBlob1" ve "MyBlob2" döndürür.</span><span class="sxs-lookup"><span data-stu-id="42abc-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="42abc-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="42abc-170">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42abc-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="42abc-171">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="42abc-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="42abc-172">-SnapshotTime</span></span>
<span data-ttu-id="42abc-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="42abc-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="42abc-174">-VersionId</span></span>
<span data-ttu-id="42abc-175">Blob VersionId 'Si</span><span class="sxs-lookup"><span data-stu-id="42abc-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42abc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42abc-176">CommonParameters</span></span>
<span data-ttu-id="42abc-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42abc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42abc-178">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42abc-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42abc-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42abc-179">INPUTS</span></span>

### <span data-ttu-id="42abc-180">System. String</span><span class="sxs-lookup"><span data-stu-id="42abc-180">System.String</span></span>

### <span data-ttu-id="42abc-181">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="42abc-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="42abc-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42abc-182">OUTPUTS</span></span>

### <span data-ttu-id="42abc-183">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="42abc-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="42abc-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42abc-184">NOTES</span></span>

## <span data-ttu-id="42abc-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42abc-185">RELATED LINKS</span></span>

[<span data-ttu-id="42abc-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42abc-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="42abc-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="42abc-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="42abc-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42abc-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


