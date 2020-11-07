---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
ms.openlocfilehash: 3d2fd2ae65ff343bbe5faeece41194c768bec8c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940207"
---
# <span data-ttu-id="a5a0d-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a5a0d-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="a5a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a0d-103">Bir paylaşımın depolama kapasitesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5a0d-104">SYNTAX</span></span>

### <span data-ttu-id="a5a0d-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="a5a0d-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a5a0d-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="a5a0d-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5a0d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a0d-108">**Set-AzureStorageShareQuota** cmdlet 'i belirtilen paylaşımın depolama kapasitesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="a5a0d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5a0d-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a0d-110">Örnek 1: paylaşımın depolama kapasitesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="a5a0d-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="a5a0d-111">Bu komut, ContosoShare01 adlı paylaşımın depolama kapasitesini 1024 GB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="a5a0d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5a0d-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a0d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a5a0d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a5a0d-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a5a0d-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a5a0d-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a5a0d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a5a0d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a5a0d-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a5a0d-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a5a0d-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a5a0d-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a5a0d-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a5a0d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="a5a0d-123">-Context</span></span>
<span data-ttu-id="a5a0d-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a5a0d-125">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a5a0d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a0d-126">-DefaultProfile</span></span>
<span data-ttu-id="a5a0d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a0d-128">-Kota</span><span class="sxs-lookup"><span data-stu-id="a5a0d-128">-Quota</span></span>
<span data-ttu-id="a5a0d-129">Kota değerini gigabayt (GB) cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="a5a0d-130">Uygulamasındaki kota sınırlamasını görün https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="a5a0d-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="a5a0d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a5a0d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a5a0d-132">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a5a0d-133">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="a5a0d-133">-Share</span></span>
<span data-ttu-id="a5a0d-134">Bu cmdlet 'lerin kota ayarladığı paylaşımı temsil eden bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="a5a0d-135">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-135">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="a5a0d-136">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="a5a0d-136">-ShareName</span></span>
<span data-ttu-id="a5a0d-137">Kota ayarlanacak dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="a5a0d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a0d-138">CommonParameters</span></span>
<span data-ttu-id="a5a0d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5a0d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a0d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a0d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a0d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5a0d-141">INPUTS</span></span>

### <span data-ttu-id="a5a0d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a0d-142">System.String</span></span>

### <span data-ttu-id="a5a0d-143">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a5a0d-143">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="a5a0d-144">Parametreler: paylaşma (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5a0d-144">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="a5a0d-145">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="a5a0d-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a5a0d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5a0d-146">OUTPUTS</span></span>

### <span data-ttu-id="a5a0d-147">Microsoft. Windowsazde. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="a5a0d-147">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="a5a0d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5a0d-148">NOTES</span></span>

## <span data-ttu-id="a5a0d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5a0d-149">RELATED LINKS</span></span>

[<span data-ttu-id="a5a0d-150">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a5a0d-150">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="a5a0d-151">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="a5a0d-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a5a0d-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5a0d-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
