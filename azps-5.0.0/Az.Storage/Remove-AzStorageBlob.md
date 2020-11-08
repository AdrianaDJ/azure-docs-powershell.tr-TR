---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279322"
---
# <span data-ttu-id="accd0-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="accd0-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="accd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="accd0-102">SYNOPSIS</span></span>
<span data-ttu-id="accd0-103">Belirtilen depolama blobunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="accd0-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="accd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="accd0-104">SYNTAX</span></span>

### <span data-ttu-id="accd0-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="accd0-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="accd0-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="accd0-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="accd0-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="accd0-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="accd0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="accd0-108">DESCRIPTION</span></span>
<span data-ttu-id="accd0-109">**Remove-AzStorageBlob** cmdlet 'i, belirtilen blob 'u Azure 'daki bir depolama hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="accd0-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="accd0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="accd0-110">EXAMPLES</span></span>

### <span data-ttu-id="accd0-111">Örnek 1: depolama blob 'unu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="accd0-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="accd0-112">Bu komut adıyla tanımlanan bir blob 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="accd0-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="accd0-113">Örnek 2: ardışık düzeni kullanarak depolama blobunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="accd0-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="accd0-114">Bu komut ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="accd0-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="accd0-115">Örnek 3: ardışık düzeni kullanarak depolama bloblarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="accd0-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="accd0-116">Bu komut, blob veya blob 'ları almak için yıldız (\*) joker karakterini ve ardışık düzeni kullanır ve sonra bunları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="accd0-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="accd0-117">Örnek 4: tek bir blob sürümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="accd0-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="accd0-118">Bu komut, VersionId ile tek bir blob Veri'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="accd0-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="accd0-119">Örnek 5: tek bir blob anlık görüntüsünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="accd0-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="accd0-120">Bu komut, SnapshotTime ile tek bir blob anlık görüntüsünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="accd0-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="accd0-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="accd0-121">PARAMETERS</span></span>

### <span data-ttu-id="accd0-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="accd0-122">-Blob</span></span>
<span data-ttu-id="accd0-123">Kaldırmak istediğiniz Blobun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-123">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="accd0-124">-BlobBaseClient</span></span>
<span data-ttu-id="accd0-125">BlobBaseClient nesnesi</span><span class="sxs-lookup"><span data-stu-id="accd0-125">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="accd0-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="accd0-127">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="accd0-128">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="accd0-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="accd0-129">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="accd0-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="accd0-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="accd0-130">-CloudBlob</span></span>
<span data-ttu-id="accd0-131">Bulut blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="accd0-132">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="accd0-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="accd0-133">-CloudBlobContainer</span></span>
<span data-ttu-id="accd0-134">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="accd0-135">Get-AzStorageContainer cmdlet 'ini kullanarak edinin.</span><span class="sxs-lookup"><span data-stu-id="accd0-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="accd0-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="accd0-137">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="accd0-138">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="accd0-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="accd0-139">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="accd0-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="accd0-140">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="accd0-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="accd0-141">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="accd0-141">The default value is 10.</span></span>

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

### <span data-ttu-id="accd0-142">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="accd0-142">-Container</span></span>
<span data-ttu-id="accd0-143">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-143">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-144">-Context</span><span class="sxs-lookup"><span data-stu-id="accd0-144">-Context</span></span>
<span data-ttu-id="accd0-145">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="accd0-146">New-AzStorageContext cmdlet 'ini oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="accd0-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="accd0-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="accd0-147">-DefaultProfile</span></span>
<span data-ttu-id="accd0-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="accd0-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="accd0-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="accd0-149">-DeleteSnapshot</span></span>
<span data-ttu-id="accd0-150">Tüm anlık görüntülerin silineceğini, ancak temel blob 'un silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="accd0-151">Bu parametre belirtilmezse, temel blob ve onun anlık görüntüleri birlikte silinir.</span><span class="sxs-lookup"><span data-stu-id="accd0-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="accd0-152">Kullanıcıdan silme işlemini onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="accd0-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="accd0-153">-Force</span><span class="sxs-lookup"><span data-stu-id="accd0-153">-Force</span></span>
<span data-ttu-id="accd0-154">Bu cmdlet 'in blob 'u ve anlık görüntüsünü onaysız olarak kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="accd0-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="accd0-155">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="accd0-155">-PassThru</span></span>
<span data-ttu-id="accd0-156">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="accd0-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="accd0-157">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="accd0-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="accd0-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="accd0-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="accd0-159">Kullanılacak cmdlet için Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="accd0-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="accd0-160">Belirtilmezse, cmdlet varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="accd0-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="accd0-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="accd0-161">-SnapshotTime</span></span>
<span data-ttu-id="accd0-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="accd0-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="accd0-163">-VersionId</span></span>
<span data-ttu-id="accd0-164">Blob VersionId 'Si</span><span class="sxs-lookup"><span data-stu-id="accd0-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="accd0-165">-Confirm</span></span>
<span data-ttu-id="accd0-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="accd0-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="accd0-167">-WhatIf</span></span>
<span data-ttu-id="accd0-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="accd0-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="accd0-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="accd0-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accd0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="accd0-170">CommonParameters</span></span>
<span data-ttu-id="accd0-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="accd0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="accd0-172">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="accd0-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="accd0-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="accd0-173">INPUTS</span></span>

### <span data-ttu-id="accd0-174">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="accd0-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="accd0-175">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="accd0-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="accd0-176">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="accd0-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="accd0-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="accd0-177">OUTPUTS</span></span>

### <span data-ttu-id="accd0-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="accd0-178">System.Boolean</span></span>

## <span data-ttu-id="accd0-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="accd0-179">NOTES</span></span>

## <span data-ttu-id="accd0-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="accd0-180">RELATED LINKS</span></span>

[<span data-ttu-id="accd0-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="accd0-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="accd0-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="accd0-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="accd0-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="accd0-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
