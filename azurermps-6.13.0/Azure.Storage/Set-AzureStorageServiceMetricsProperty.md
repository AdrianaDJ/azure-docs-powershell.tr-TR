---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 1b32fbf01b22c365384190c6530a649a06664219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591494"
---
# <span data-ttu-id="148c8-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="148c8-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="148c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="148c8-102">SYNOPSIS</span></span>
<span data-ttu-id="148c8-103">Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="148c8-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="148c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="148c8-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="148c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="148c8-105">DESCRIPTION</span></span>
<span data-ttu-id="148c8-106">**Set-AzureStorageServiceMetricsProperty** cmdlet 'ı, Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="148c8-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="148c8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="148c8-107">EXAMPLES</span></span>

### <span data-ttu-id="148c8-108">Örnek 1: blob hizmeti için ölçüm özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="148c8-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="148c8-109">Bu komut, BLOB depolama için sürüm 1,0 ölçümlerini bir hizmet düzeyine değiştirir.</span><span class="sxs-lookup"><span data-stu-id="148c8-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="148c8-110">Azure depolama hizmeti ölçümleri 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="148c8-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="148c8-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş ölçüler özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="148c8-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="148c8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="148c8-112">PARAMETERS</span></span>

### <span data-ttu-id="148c8-113">-Context</span><span class="sxs-lookup"><span data-stu-id="148c8-113">-Context</span></span>
<span data-ttu-id="148c8-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="148c8-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="148c8-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="148c8-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="148c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148c8-116">-DefaultProfile</span></span>
<span data-ttu-id="148c8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="148c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="148c8-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="148c8-118">-MetricsLevel</span></span>
<span data-ttu-id="148c8-119">Azure Storage 'un hizmet için kullandığı ölçü düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="148c8-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="148c8-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="148c8-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="148c8-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="148c8-121">None</span></span>
- <span data-ttu-id="148c8-122">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="148c8-122">Service</span></span>
- <span data-ttu-id="148c8-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="148c8-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148c8-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="148c8-124">-MetricsType</span></span>
<span data-ttu-id="148c8-125">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="148c8-125">Specifies a metrics type.</span></span>
<span data-ttu-id="148c8-126">Bu cmldet, Azure depolama hizmeti ölçümleri türünü bu parametrenin belirttiği değere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="148c8-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="148c8-127">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="148c8-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148c8-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="148c8-128">-PassThru</span></span>
<span data-ttu-id="148c8-129">Bu cmdlet 'lerin güncelleştirilmiş ölçüm özelliklerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="148c8-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="148c8-130">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="148c8-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="148c8-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="148c8-131">-RetentionDays</span></span>
<span data-ttu-id="148c8-132">Azure depolama hizmeti 'nin ölçüm bilgilerini koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="148c8-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="148c8-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="148c8-133">-ServiceType</span></span>
<span data-ttu-id="148c8-134">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="148c8-134">Specifies the storage service type.</span></span>
<span data-ttu-id="148c8-135">Bu cmdlet, bu parametrenin belirttiği hizmet türünün ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="148c8-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="148c8-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="148c8-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="148c8-137">'Unu</span><span class="sxs-lookup"><span data-stu-id="148c8-137">Blob</span></span> 
- <span data-ttu-id="148c8-138">Tablo</span><span class="sxs-lookup"><span data-stu-id="148c8-138">Table</span></span>
- <span data-ttu-id="148c8-139">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="148c8-139">Queue</span></span>
- <span data-ttu-id="148c8-140">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="148c8-140">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148c8-141">-Version</span><span class="sxs-lookup"><span data-stu-id="148c8-141">-Version</span></span>
<span data-ttu-id="148c8-142">Azure depolama alanı ölçümlerinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="148c8-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="148c8-143">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="148c8-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148c8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148c8-144">CommonParameters</span></span>
<span data-ttu-id="148c8-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="148c8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148c8-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="148c8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148c8-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="148c8-147">INPUTS</span></span>

### <span data-ttu-id="148c8-148">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="148c8-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="148c8-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="148c8-149">OUTPUTS</span></span>

### <span data-ttu-id="148c8-150">Microsoft. Windowsazme. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="148c8-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="148c8-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="148c8-151">NOTES</span></span>

## <span data-ttu-id="148c8-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="148c8-152">RELATED LINKS</span></span>

[<span data-ttu-id="148c8-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="148c8-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="148c8-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="148c8-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


