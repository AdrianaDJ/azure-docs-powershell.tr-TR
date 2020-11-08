---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: ed2701a5cdb15b02a2627fc3bacc42861a1fdbb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936195"
---
# <span data-ttu-id="3af51-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3af51-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="3af51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af51-102">SYNOPSIS</span></span>
<span data-ttu-id="3af51-103">Belirtilen depolama blobunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3af51-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="3af51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3af51-104">SYNTAX</span></span>

### <span data-ttu-id="3af51-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3af51-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3af51-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="3af51-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3af51-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="3af51-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3af51-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3af51-108">DESCRIPTION</span></span>
<span data-ttu-id="3af51-109">**Remove-AzStorageBlob** cmdlet 'i, belirtilen blob 'u Azure 'daki bir depolama hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3af51-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="3af51-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3af51-110">EXAMPLES</span></span>

### <span data-ttu-id="3af51-111">Örnek 1: depolama blob 'unu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="3af51-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="3af51-112">Bu komut adıyla tanımlanan bir blob 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3af51-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="3af51-113">Örnek 2: ardışık düzeni kullanarak depolama blobunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="3af51-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="3af51-114">Bu komut ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="3af51-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="3af51-115">Örnek 3: ardışık düzeni kullanarak depolama bloblarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3af51-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="3af51-116">Bu komut, blob veya blob 'ları almak için yıldız (\*) joker karakterini ve ardışık düzeni kullanır ve sonra bunları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3af51-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="3af51-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3af51-117">PARAMETERS</span></span>

### <span data-ttu-id="3af51-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="3af51-118">-Blob</span></span>
<span data-ttu-id="3af51-119">Kaldırmak istediğiniz Blobun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="3af51-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3af51-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3af51-121">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3af51-122">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="3af51-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3af51-123">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="3af51-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3af51-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3af51-124">-CloudBlob</span></span>
<span data-ttu-id="3af51-125">Bulut blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="3af51-126">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3af51-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af51-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3af51-127">-CloudBlobContainer</span></span>
<span data-ttu-id="3af51-128">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="3af51-129">Get-AzStorageContainer cmdlet 'ini kullanarak edinin.</span><span class="sxs-lookup"><span data-stu-id="3af51-129">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af51-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3af51-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3af51-131">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3af51-132">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3af51-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3af51-133">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="3af51-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3af51-134">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="3af51-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3af51-135">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="3af51-135">The default value is 10.</span></span>

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

### <span data-ttu-id="3af51-136">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="3af51-136">-Container</span></span>
<span data-ttu-id="3af51-137">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="3af51-138">-Context</span><span class="sxs-lookup"><span data-stu-id="3af51-138">-Context</span></span>
<span data-ttu-id="3af51-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3af51-140">New-AzStorageContext cmdlet 'ini oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3af51-140">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="3af51-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af51-141">-DefaultProfile</span></span>
<span data-ttu-id="3af51-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3af51-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3af51-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="3af51-143">-DeleteSnapshot</span></span>
<span data-ttu-id="3af51-144">Tüm anlık görüntülerin silineceğini, ancak temel blob 'un silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="3af51-145">Bu parametre belirtilmezse, temel blob ve onun anlık görüntüleri birlikte silinir.</span><span class="sxs-lookup"><span data-stu-id="3af51-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="3af51-146">Kullanıcıdan silme işlemini onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="3af51-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="3af51-147">-Force</span><span class="sxs-lookup"><span data-stu-id="3af51-147">-Force</span></span>
<span data-ttu-id="3af51-148">Bu cmdlet 'in blob 'u ve anlık görüntüsünü onaysız olarak kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3af51-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="3af51-149">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3af51-149">-PassThru</span></span>
<span data-ttu-id="3af51-150">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3af51-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3af51-151">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3af51-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3af51-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3af51-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3af51-153">Kullanılacak cmdlet için Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3af51-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="3af51-154">Belirtilmezse, cmdlet varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3af51-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="3af51-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="3af51-155">-Confirm</span></span>
<span data-ttu-id="3af51-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3af51-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af51-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af51-157">-WhatIf</span></span>
<span data-ttu-id="3af51-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3af51-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af51-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3af51-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af51-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af51-160">CommonParameters</span></span>
<span data-ttu-id="3af51-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3af51-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af51-162">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af51-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af51-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3af51-163">INPUTS</span></span>

### <span data-ttu-id="3af51-164">Microsoft. WindowsAz. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3af51-164">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="3af51-165">Microsoft. WindowsAz. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3af51-165">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="3af51-166">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="3af51-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3af51-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3af51-167">OUTPUTS</span></span>

### <span data-ttu-id="3af51-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3af51-168">System.Boolean</span></span>

## <span data-ttu-id="3af51-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3af51-169">NOTES</span></span>

## <span data-ttu-id="3af51-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3af51-170">RELATED LINKS</span></span>

[<span data-ttu-id="3af51-171">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3af51-171">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="3af51-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3af51-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="3af51-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3af51-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)