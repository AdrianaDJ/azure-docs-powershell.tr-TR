---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593865"
---
# <span data-ttu-id="6f1b2-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6f1b2-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="6f1b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1b2-103">Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f1b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f1b2-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="6f1b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f1b2-105">DESCRIPTION</span></span>
<span data-ttu-id="6f1b2-106">**Set-AzureStorageServiceMetricsProperty** cmdlet 'ı, Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6f1b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f1b2-107">EXAMPLES</span></span>

### <span data-ttu-id="6f1b2-108">Örnek 1: blob hizmeti için ölçüm özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="6f1b2-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="6f1b2-109">Bu komut, BLOB depolama için sürüm 1,0 ölçümlerini bir hizmet düzeyine değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="6f1b2-110">Azure depolama hizmeti ölçümleri 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="6f1b2-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş ölçüler özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="6f1b2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f1b2-112">PARAMETERS</span></span>

### <span data-ttu-id="6f1b2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="6f1b2-113">-Context</span></span>
<span data-ttu-id="6f1b2-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6f1b2-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6f1b2-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="6f1b2-116">-MetricsLevel</span></span>
<span data-ttu-id="6f1b2-117">Azure Storage 'un hizmet için kullandığı ölçü düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="6f1b2-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6f1b2-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f1b2-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f1b2-119">None</span></span>
- <span data-ttu-id="6f1b2-120">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="6f1b2-120">Service</span></span>
- <span data-ttu-id="6f1b2-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="6f1b2-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1b2-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="6f1b2-122">-MetricsType</span></span>
<span data-ttu-id="6f1b2-123">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-123">Specifies a metrics type.</span></span>
<span data-ttu-id="6f1b2-124">Bu cmldet, Azure depolama hizmeti ölçümleri türünü bu parametrenin belirttiği değere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="6f1b2-125">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1b2-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6f1b2-126">-PassThru</span></span>
<span data-ttu-id="6f1b2-127">Bu cmdlet 'lerin güncelleştirilmiş ölçüm özelliklerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="6f1b2-128">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6f1b2-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6f1b2-129">-RetentionDays</span></span>
<span data-ttu-id="6f1b2-130">Azure depolama hizmeti 'nin ölçüm bilgilerini koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="6f1b2-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6f1b2-131">-ServiceType</span></span>
<span data-ttu-id="6f1b2-132">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-132">Specifies the storage service type.</span></span>
<span data-ttu-id="6f1b2-133">Bu cmdlet, bu parametrenin belirttiği hizmet türünün ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6f1b2-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6f1b2-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f1b2-135">'Unu</span><span class="sxs-lookup"><span data-stu-id="6f1b2-135">Blob</span></span> 
- <span data-ttu-id="6f1b2-136">Tablo</span><span class="sxs-lookup"><span data-stu-id="6f1b2-136">Table</span></span>
- <span data-ttu-id="6f1b2-137">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="6f1b2-137">Queue</span></span>
- <span data-ttu-id="6f1b2-138">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="6f1b2-138">File</span></span>

<span data-ttu-id="6f1b2-139">Dosya değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-139">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1b2-140">-Version</span><span class="sxs-lookup"><span data-stu-id="6f1b2-140">-Version</span></span>
<span data-ttu-id="6f1b2-141">Azure depolama alanı ölçümlerinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="6f1b2-142">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-142">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1b2-143">CommonParameters</span></span>
<span data-ttu-id="6f1b2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f1b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1b2-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1b2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1b2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f1b2-146">INPUTS</span></span>

### <span data-ttu-id="6f1b2-147">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="6f1b2-147">IStorageContext</span></span>

<span data-ttu-id="6f1b2-148">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6f1b2-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="6f1b2-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f1b2-149">OUTPUTS</span></span>

### <span data-ttu-id="6f1b2-150">Microsoft. Windowsazme. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="6f1b2-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="6f1b2-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f1b2-151">NOTES</span></span>

## <span data-ttu-id="6f1b2-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f1b2-152">RELATED LINKS</span></span>

[<span data-ttu-id="6f1b2-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6f1b2-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="6f1b2-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f1b2-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


