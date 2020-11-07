---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: e260ab25d2028fd970bf1c69e63a23e7dc190ce6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758528"
---
# <span data-ttu-id="55d6d-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="55d6d-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="55d6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="55d6d-103">Bir paylaşımın depolama kapasitesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55d6d-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="55d6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55d6d-104">SYNTAX</span></span>

### <span data-ttu-id="55d6d-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="55d6d-105">ShareName</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="55d6d-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="55d6d-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="55d6d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55d6d-107">DESCRIPTION</span></span>
<span data-ttu-id="55d6d-108">**Set-AzStorageShareQuota** cmdlet 'i belirtilen paylaşımın depolama kapasitesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55d6d-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="55d6d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55d6d-109">EXAMPLES</span></span>

### <span data-ttu-id="55d6d-110">Örnek 1: paylaşımın depolama kapasitesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="55d6d-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="55d6d-111">Bu komut, ContosoShare01 adlı paylaşımın depolama kapasitesini 1024 GB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55d6d-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="55d6d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55d6d-112">PARAMETERS</span></span>

### <span data-ttu-id="55d6d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="55d6d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="55d6d-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d6d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="55d6d-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="55d6d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="55d6d-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="55d6d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="55d6d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="55d6d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="55d6d-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d6d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="55d6d-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55d6d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="55d6d-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="55d6d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="55d6d-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="55d6d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="55d6d-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="55d6d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="55d6d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="55d6d-123">-Context</span></span>
<span data-ttu-id="55d6d-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d6d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="55d6d-125">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="55d6d-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55d6d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d6d-126">-DefaultProfile</span></span>
<span data-ttu-id="55d6d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55d6d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55d6d-128">-Kota</span><span class="sxs-lookup"><span data-stu-id="55d6d-128">-Quota</span></span>
<span data-ttu-id="55d6d-129">Kota değerini gigabayt (GB) cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d6d-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="55d6d-130">Uygulamasındaki kota sınırlamasını görün https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="55d6d-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d6d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="55d6d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="55d6d-132">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d6d-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="55d6d-133">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="55d6d-133">-Share</span></span>
<span data-ttu-id="55d6d-134">Bu cmdlet 'lerin kota ayarladığı paylaşımı temsil eden bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d6d-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="55d6d-135">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="55d6d-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55d6d-136">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="55d6d-136">-ShareName</span></span>
<span data-ttu-id="55d6d-137">Kota ayarlanacak dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d6d-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55d6d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d6d-138">CommonParameters</span></span>
<span data-ttu-id="55d6d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55d6d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d6d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d6d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d6d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55d6d-141">INPUTS</span></span>

### <span data-ttu-id="55d6d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="55d6d-142">System.String</span></span>

### <span data-ttu-id="55d6d-143">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="55d6d-143">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="55d6d-144">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="55d6d-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="55d6d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55d6d-145">OUTPUTS</span></span>

### <span data-ttu-id="55d6d-146">Microsoft. Windowsazde. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="55d6d-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="55d6d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55d6d-147">NOTES</span></span>

## <span data-ttu-id="55d6d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55d6d-148">RELATED LINKS</span></span>

[<span data-ttu-id="55d6d-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="55d6d-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="55d6d-150">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="55d6d-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="55d6d-151">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="55d6d-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
