---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
ms.openlocfilehash: b9d987dad0542f7637f7d061ee510c1601dc6e6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589007"
---
# <span data-ttu-id="ea8a8-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ea8a8-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="ea8a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8a8-103">Belirtilen depolama blobunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-103">Removes the specified storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea8a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea8a8-104">SYNTAX</span></span>

### <span data-ttu-id="ea8a8-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea8a8-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8a8-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="ea8a8-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8a8-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="ea8a8-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea8a8-108">DESCRIPTION</span></span>
<span data-ttu-id="ea8a8-109">**Remove-AzureStorageBlob** cmdlet 'i, belirtilen blob 'u Azure 'daki bir depolama hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="ea8a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea8a8-110">EXAMPLES</span></span>

### <span data-ttu-id="ea8a8-111">Örnek 1: depolama blob 'unu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="ea8a8-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="ea8a8-112">Bu komut adıyla tanımlanan bir blob 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="ea8a8-113">Örnek 2: ardışık düzeni kullanarak depolama blobunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="ea8a8-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="ea8a8-114">Bu komut ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="ea8a8-115">Örnek 3: ardışık düzeni kullanarak depolama bloblarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ea8a8-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="ea8a8-116">Bu komut, blob veya blob 'ları almak için yıldız (\*) joker karakterini ve ardışık düzeni kullanır ve sonra bunları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="ea8a8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea8a8-117">PARAMETERS</span></span>

### <span data-ttu-id="ea8a8-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="ea8a8-118">-Blob</span></span>
<span data-ttu-id="ea8a8-119">Kaldırmak istediğiniz Blobun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="ea8a8-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ea8a8-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ea8a8-121">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ea8a8-122">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ea8a8-123">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ea8a8-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ea8a8-124">-CloudBlob</span></span>
<span data-ttu-id="ea8a8-125">Bulut blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="ea8a8-126">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ea8a8-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ea8a8-127">-CloudBlobContainer</span></span>
<span data-ttu-id="ea8a8-128">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="ea8a8-129">Get-AzureStorageContainer cmdlet 'ini kullanarak edinin.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="ea8a8-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ea8a8-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ea8a8-131">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ea8a8-132">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ea8a8-133">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ea8a8-134">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ea8a8-135">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-135">The default value is 10.</span></span>

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

### <span data-ttu-id="ea8a8-136">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ea8a8-136">-Container</span></span>
<span data-ttu-id="ea8a8-137">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="ea8a8-138">-Context</span><span class="sxs-lookup"><span data-stu-id="ea8a8-138">-Context</span></span>
<span data-ttu-id="ea8a8-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ea8a8-140">New-AzureStorageContext cmdlet 'ini oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="ea8a8-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="ea8a8-141">-DeleteSnapshot</span></span>
<span data-ttu-id="ea8a8-142">Tüm anlık görüntülerin silineceğini, ancak temel blob 'un silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="ea8a8-143">Bu parametre belirtilmezse, temel blob ve onun anlık görüntüleri birlikte silinir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="ea8a8-144">Kullanıcıdan silme işlemini onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-144">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="ea8a8-145">-Force</span><span class="sxs-lookup"><span data-stu-id="ea8a8-145">-Force</span></span>
<span data-ttu-id="ea8a8-146">Bu cmdlet 'in blob 'u ve anlık görüntüsünü onaysız olarak kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="ea8a8-147">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ea8a8-147">-PassThru</span></span>
<span data-ttu-id="ea8a8-148">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ea8a8-149">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-149">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ea8a8-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ea8a8-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ea8a8-151">Kullanılacak cmdlet için Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="ea8a8-152">Belirtilmezse, cmdlet varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-152">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="ea8a8-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea8a8-153">-Confirm</span></span>
<span data-ttu-id="ea8a8-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8a8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8a8-155">-WhatIf</span></span>
<span data-ttu-id="ea8a8-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8a8-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8a8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8a8-158">CommonParameters</span></span>
<span data-ttu-id="ea8a8-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8a8-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8a8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8a8-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea8a8-161">INPUTS</span></span>

### <span data-ttu-id="ea8a8-162">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="ea8a8-162">IStorageContext</span></span>

<span data-ttu-id="ea8a8-163">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ea8a8-163">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ea8a8-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea8a8-164">OUTPUTS</span></span>

### <span data-ttu-id="ea8a8-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea8a8-165">System.Boolean</span></span>

## <span data-ttu-id="ea8a8-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea8a8-166">NOTES</span></span>

## <span data-ttu-id="ea8a8-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea8a8-167">RELATED LINKS</span></span>

[<span data-ttu-id="ea8a8-168">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ea8a8-168">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="ea8a8-169">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ea8a8-169">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="ea8a8-170">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ea8a8-170">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
