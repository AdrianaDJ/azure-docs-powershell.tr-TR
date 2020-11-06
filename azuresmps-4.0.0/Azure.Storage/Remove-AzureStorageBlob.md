---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b40585f584cc8c2634acab54e6862e4163c6b7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572093"
---
# <span data-ttu-id="e7d14-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e7d14-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="e7d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d14-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d14-103">Belirtilen depolama blobunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7d14-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="e7d14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7d14-104">SYNTAX</span></span>

### <span data-ttu-id="e7d14-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7d14-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7d14-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="e7d14-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7d14-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="e7d14-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d14-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7d14-108">DESCRIPTION</span></span>
<span data-ttu-id="e7d14-109">**Remove-AzureStorageBlob** cmdlet 'i, belirtilen blob 'u Azure 'daki bir depolama hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7d14-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="e7d14-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7d14-110">EXAMPLES</span></span>

### <span data-ttu-id="e7d14-111">Örnek 1: depolama blob 'unu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="e7d14-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="e7d14-112">Bu komut adıyla tanımlanan bir blob 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7d14-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="e7d14-113">Örnek 2: ardışık düzeni kullanarak depolama blobunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="e7d14-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="e7d14-114">Bu komut ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="e7d14-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="e7d14-115">Örnek 3: ardışık düzeni kullanarak depolama bloblarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e7d14-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="e7d14-116">Bu komut, blob veya blob 'ları almak için yıldız (\*) joker karakterini ve ardışık düzeni kullanır ve sonra bunları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7d14-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="e7d14-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7d14-117">PARAMETERS</span></span>

### <span data-ttu-id="e7d14-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="e7d14-118">-Blob</span></span>
<span data-ttu-id="e7d14-119">Kaldırmak istediğiniz Blobun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-119">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d14-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7d14-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e7d14-121">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e7d14-122">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="e7d14-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e7d14-123">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7d14-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e7d14-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e7d14-124">-CloudBlob</span></span>
<span data-ttu-id="e7d14-125">Bulut blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="e7d14-126">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7d14-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d14-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e7d14-127">-CloudBlobContainer</span></span>
<span data-ttu-id="e7d14-128">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="e7d14-129">Get-AzureStorageContainer cmdlet 'ini kullanarak edinin.</span><span class="sxs-lookup"><span data-stu-id="e7d14-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d14-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e7d14-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e7d14-131">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e7d14-132">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7d14-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e7d14-133">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="e7d14-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e7d14-134">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="e7d14-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e7d14-135">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e7d14-135">The default value is 10.</span></span>

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

### <span data-ttu-id="e7d14-136">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="e7d14-136">-Container</span></span>
<span data-ttu-id="e7d14-137">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d14-138">-Context</span><span class="sxs-lookup"><span data-stu-id="e7d14-138">-Context</span></span>
<span data-ttu-id="e7d14-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e7d14-140">New-AzureStorageContext cmdlet 'ini oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7d14-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d14-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="e7d14-141">-DeleteSnapshot</span></span>
<span data-ttu-id="e7d14-142">Tüm anlık görüntülerin silineceğini, ancak temel blob 'un silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="e7d14-143">Bu parametre belirtilmezse, temel blob ve onun anlık görüntüleri birlikte silinir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="e7d14-144">Kullanıcıdan silme işlemini onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-144">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="e7d14-145">-Force</span><span class="sxs-lookup"><span data-stu-id="e7d14-145">-Force</span></span>
<span data-ttu-id="e7d14-146">Bu cmdlet 'in blob 'u ve anlık görüntüsünü onaysız olarak kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="e7d14-147">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e7d14-147">-PassThru</span></span>
<span data-ttu-id="e7d14-148">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e7d14-149">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="e7d14-149">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e7d14-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7d14-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e7d14-151">Kullanılacak cmdlet için Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="e7d14-152">Belirtilmezse, cmdlet varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e7d14-152">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="e7d14-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7d14-153">-Confirm</span></span>
<span data-ttu-id="e7d14-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7d14-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d14-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d14-155">-WhatIf</span></span>
<span data-ttu-id="e7d14-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7d14-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d14-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7d14-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d14-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d14-158">CommonParameters</span></span>
<span data-ttu-id="e7d14-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7d14-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d14-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d14-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d14-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7d14-161">INPUTS</span></span>

## <span data-ttu-id="e7d14-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7d14-162">OUTPUTS</span></span>

## <span data-ttu-id="e7d14-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7d14-163">NOTES</span></span>

## <span data-ttu-id="e7d14-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7d14-164">RELATED LINKS</span></span>

[<span data-ttu-id="e7d14-165">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e7d14-165">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="e7d14-166">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e7d14-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="e7d14-167">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e7d14-167">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
