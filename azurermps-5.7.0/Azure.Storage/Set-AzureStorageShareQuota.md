---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
ms.openlocfilehash: 54636c226d3e8eb7ca9572a8f2e6c95e96981875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765013"
---
# <span data-ttu-id="486ad-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="486ad-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="486ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="486ad-102">SYNOPSIS</span></span>
<span data-ttu-id="486ad-103">Bir paylaşımın depolama kapasitesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="486ad-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="486ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="486ad-104">SYNTAX</span></span>

### <span data-ttu-id="486ad-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="486ad-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="486ad-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="486ad-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="486ad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="486ad-107">DESCRIPTION</span></span>
<span data-ttu-id="486ad-108">**Set-AzureStorageShareQuota** cmdlet 'i belirtilen paylaşımın depolama kapasitesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="486ad-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="486ad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="486ad-109">EXAMPLES</span></span>

### <span data-ttu-id="486ad-110">Örnek 1: paylaşımın depolama kapasitesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="486ad-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="486ad-111">Bu komut, ContosoShare01 adlı paylaşımın depolama kapasitesini 1024 GB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="486ad-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="486ad-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="486ad-112">PARAMETERS</span></span>

### <span data-ttu-id="486ad-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="486ad-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="486ad-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="486ad-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="486ad-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="486ad-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="486ad-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="486ad-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="486ad-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="486ad-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="486ad-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="486ad-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="486ad-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="486ad-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="486ad-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="486ad-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="486ad-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="486ad-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="486ad-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="486ad-122">The default value is 10.</span></span>

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

### <span data-ttu-id="486ad-123">-Context</span><span class="sxs-lookup"><span data-stu-id="486ad-123">-Context</span></span>
<span data-ttu-id="486ad-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="486ad-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="486ad-125">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="486ad-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-126">-Kota</span><span class="sxs-lookup"><span data-stu-id="486ad-126">-Quota</span></span>
<span data-ttu-id="486ad-127">Kota değerini gigabayt (GB) cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="486ad-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="486ad-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="486ad-129">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="486ad-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="486ad-130">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="486ad-130">-Share</span></span>
<span data-ttu-id="486ad-131">Bu cmdlet 'lerin kota ayarladığı paylaşımı temsil eden bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="486ad-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="486ad-132">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="486ad-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-133">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="486ad-133">-ShareName</span></span>
<span data-ttu-id="486ad-134">Kota ayarlanacak dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="486ad-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486ad-135">CommonParameters</span></span>
<span data-ttu-id="486ad-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="486ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486ad-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="486ad-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486ad-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="486ad-138">INPUTS</span></span>

### <span data-ttu-id="486ad-139">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="486ad-139">IStorageContext</span></span>

<span data-ttu-id="486ad-140">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="486ad-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="486ad-141">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="486ad-141">CloudFileShare</span></span>

<span data-ttu-id="486ad-142">' Share ' parametresi ardışık düzenin ' CloudFileShare ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="486ad-142">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

### <span data-ttu-id="486ad-143">Dizisi</span><span class="sxs-lookup"><span data-stu-id="486ad-143">String</span></span>

<span data-ttu-id="486ad-144">' PaylaşımAdı ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="486ad-144">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="486ad-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="486ad-145">OUTPUTS</span></span>

### <span data-ttu-id="486ad-146">Microsoft. Windowsazde. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="486ad-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="486ad-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="486ad-147">NOTES</span></span>

## <span data-ttu-id="486ad-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="486ad-148">RELATED LINKS</span></span>

[<span data-ttu-id="486ad-149">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="486ad-149">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="486ad-150">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="486ad-150">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="486ad-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="486ad-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
