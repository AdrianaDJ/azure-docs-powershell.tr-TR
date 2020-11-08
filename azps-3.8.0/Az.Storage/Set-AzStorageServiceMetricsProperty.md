---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098410"
---
# <span data-ttu-id="75718-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="75718-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="75718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75718-102">SYNOPSIS</span></span>
<span data-ttu-id="75718-103">Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="75718-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="75718-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75718-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75718-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75718-105">DESCRIPTION</span></span>
<span data-ttu-id="75718-106">**Set-AzStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="75718-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="75718-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75718-107">EXAMPLES</span></span>

### <span data-ttu-id="75718-108">Örnek 1: blob hizmeti için ölçüm özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="75718-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="75718-109">Bu komut, BLOB depolama için sürüm 1,0 ölçümlerini bir hizmet düzeyine değiştirir.</span><span class="sxs-lookup"><span data-stu-id="75718-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="75718-110">Azure depolama hizmeti ölçümleri 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="75718-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="75718-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş ölçüler özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="75718-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="75718-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75718-112">PARAMETERS</span></span>

### <span data-ttu-id="75718-113">-Context</span><span class="sxs-lookup"><span data-stu-id="75718-113">-Context</span></span>
<span data-ttu-id="75718-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75718-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="75718-115">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="75718-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="75718-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75718-116">-DefaultProfile</span></span>
<span data-ttu-id="75718-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75718-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75718-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="75718-118">-MetricsLevel</span></span>
<span data-ttu-id="75718-119">Azure Storage 'un hizmet için kullandığı ölçü düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75718-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="75718-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="75718-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75718-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="75718-121">None</span></span>
- <span data-ttu-id="75718-122">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="75718-122">Service</span></span>
- <span data-ttu-id="75718-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="75718-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75718-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="75718-124">-MetricsType</span></span>
<span data-ttu-id="75718-125">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="75718-125">Specifies a metrics type.</span></span>
<span data-ttu-id="75718-126">Bu cmdlet, Azure depolama hizmeti ölçümü türünü bu parametrenin belirttiği değere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75718-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="75718-127">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="75718-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="75718-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="75718-128">-PassThru</span></span>
<span data-ttu-id="75718-129">Bu cmdlet 'lerin güncelleştirilmiş ölçüm özelliklerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75718-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="75718-130">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="75718-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="75718-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="75718-131">-RetentionDays</span></span>
<span data-ttu-id="75718-132">Azure depolama hizmeti 'nin ölçüm bilgilerini koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75718-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="75718-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="75718-133">-ServiceType</span></span>
<span data-ttu-id="75718-134">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="75718-134">Specifies the storage service type.</span></span>
<span data-ttu-id="75718-135">Bu cmdlet, bu parametrenin belirttiği hizmet türünün ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="75718-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="75718-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="75718-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75718-137">'Unu</span><span class="sxs-lookup"><span data-stu-id="75718-137">Blob</span></span> 
- <span data-ttu-id="75718-138">Tablo</span><span class="sxs-lookup"><span data-stu-id="75718-138">Table</span></span>
- <span data-ttu-id="75718-139">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="75718-139">Queue</span></span>
- <span data-ttu-id="75718-140">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="75718-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="75718-141">-Version</span><span class="sxs-lookup"><span data-stu-id="75718-141">-Version</span></span>
<span data-ttu-id="75718-142">Azure depolama alanı ölçümlerinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="75718-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="75718-143">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="75718-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="75718-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75718-144">CommonParameters</span></span>
<span data-ttu-id="75718-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75718-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75718-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75718-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75718-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75718-147">INPUTS</span></span>

### <span data-ttu-id="75718-148">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="75718-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="75718-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75718-149">OUTPUTS</span></span>

### <span data-ttu-id="75718-150">Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="75718-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="75718-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75718-151">NOTES</span></span>

## <span data-ttu-id="75718-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75718-152">RELATED LINKS</span></span>

[<span data-ttu-id="75718-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="75718-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="75718-154">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="75718-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


