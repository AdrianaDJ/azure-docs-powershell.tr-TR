---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51921a7d67cd8a297f5cd61716362f13cef6cdc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572473"
---
# <span data-ttu-id="b5aff-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b5aff-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="b5aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5aff-102">SYNOPSIS</span></span>
<span data-ttu-id="b5aff-103">Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="b5aff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5aff-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="b5aff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5aff-105">DESCRIPTION</span></span>
<span data-ttu-id="b5aff-106">**Set-AzureStorageServiceMetricsProperty** cmdlet 'ı, Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="b5aff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5aff-107">EXAMPLES</span></span>

### <span data-ttu-id="b5aff-108">Örnek 1: blob hizmeti için ölçüm özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="b5aff-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="b5aff-109">Bu komut, BLOB depolama için sürüm 1,0 ölçümlerini bir hizmet düzeyine değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="b5aff-110">Azure depolama hizmeti ölçümleri 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="b5aff-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="b5aff-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş ölçüler özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b5aff-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="b5aff-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5aff-112">PARAMETERS</span></span>

### <span data-ttu-id="b5aff-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b5aff-113">-Context</span></span>
<span data-ttu-id="b5aff-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b5aff-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5aff-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b5aff-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="b5aff-116">-MetricsLevel</span></span>
<span data-ttu-id="b5aff-117">Azure Storage 'un hizmet için kullandığı ölçü düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="b5aff-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b5aff-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5aff-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b5aff-119">None</span></span>
- <span data-ttu-id="b5aff-120">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="b5aff-120">Service</span></span>
- <span data-ttu-id="b5aff-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="b5aff-121">ServiceAndApi</span></span>

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

### <span data-ttu-id="b5aff-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="b5aff-122">-MetricsType</span></span>
<span data-ttu-id="b5aff-123">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-123">Specifies a metrics type.</span></span>
<span data-ttu-id="b5aff-124">Bu cmldet, Azure depolama hizmeti ölçümleri türünü bu parametrenin belirttiği değere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b5aff-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="b5aff-125">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="b5aff-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="b5aff-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b5aff-126">-PassThru</span></span>
<span data-ttu-id="b5aff-127">Bu cmdlet 'lerin güncelleştirilmiş ölçüm özelliklerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="b5aff-128">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b5aff-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b5aff-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="b5aff-129">-RetentionDays</span></span>
<span data-ttu-id="b5aff-130">Azure depolama hizmeti 'nin ölçüm bilgilerini koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="b5aff-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b5aff-131">-ServiceType</span></span>
<span data-ttu-id="b5aff-132">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-132">Specifies the storage service type.</span></span>
<span data-ttu-id="b5aff-133">Bu cmdlet, bu parametrenin belirttiği hizmet türünün ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b5aff-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b5aff-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5aff-135">'Unu</span><span class="sxs-lookup"><span data-stu-id="b5aff-135">Blob</span></span> 
- <span data-ttu-id="b5aff-136">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5aff-136">Table</span></span>
- <span data-ttu-id="b5aff-137">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="b5aff-137">Queue</span></span>
- <span data-ttu-id="b5aff-138">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="b5aff-138">File</span></span>

<span data-ttu-id="b5aff-139">Dosya değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="b5aff-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="b5aff-140">-Version</span><span class="sxs-lookup"><span data-stu-id="b5aff-140">-Version</span></span>
<span data-ttu-id="b5aff-141">Azure depolama alanı ölçümlerinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5aff-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="b5aff-142">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b5aff-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="b5aff-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5aff-143">CommonParameters</span></span>
<span data-ttu-id="b5aff-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5aff-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5aff-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5aff-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5aff-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5aff-146">INPUTS</span></span>

## <span data-ttu-id="b5aff-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5aff-147">OUTPUTS</span></span>

## <span data-ttu-id="b5aff-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5aff-148">NOTES</span></span>

## <span data-ttu-id="b5aff-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5aff-149">RELATED LINKS</span></span>

[<span data-ttu-id="b5aff-150">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b5aff-150">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="b5aff-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5aff-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


