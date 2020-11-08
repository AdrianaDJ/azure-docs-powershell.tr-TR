---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266734"
---
# <span data-ttu-id="c76b1-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c76b1-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="c76b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c76b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c76b1-103">Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c76b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c76b1-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c76b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c76b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c76b1-106">**Set-AzStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c76b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c76b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c76b1-108">Örnek 1: blob hizmeti için ölçüm özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c76b1-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="c76b1-109">Bu komut, BLOB depolama için sürüm 1,0 ölçümlerini bir hizmet düzeyine değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="c76b1-110">Azure depolama hizmeti ölçümleri 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="c76b1-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="c76b1-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş ölçüler özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c76b1-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="c76b1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c76b1-112">PARAMETERS</span></span>

### <span data-ttu-id="c76b1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c76b1-113">-Context</span></span>
<span data-ttu-id="c76b1-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c76b1-115">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c76b1-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c76b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76b1-116">-DefaultProfile</span></span>
<span data-ttu-id="c76b1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c76b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c76b1-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="c76b1-118">-MetricsLevel</span></span>
<span data-ttu-id="c76b1-119">Azure Storage 'un hizmet için kullandığı ölçü düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="c76b1-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c76b1-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c76b1-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c76b1-121">None</span></span>
- <span data-ttu-id="c76b1-122">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="c76b1-122">Service</span></span>
- <span data-ttu-id="c76b1-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="c76b1-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="c76b1-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="c76b1-124">-MetricsType</span></span>
<span data-ttu-id="c76b1-125">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-125">Specifies a metrics type.</span></span>
<span data-ttu-id="c76b1-126">Bu cmdlet, Azure depolama hizmeti ölçümü türünü bu parametrenin belirttiği değere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c76b1-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="c76b1-127">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="c76b1-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="c76b1-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c76b1-128">-PassThru</span></span>
<span data-ttu-id="c76b1-129">Bu cmdlet 'lerin güncelleştirilmiş ölçüm özelliklerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="c76b1-130">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c76b1-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c76b1-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c76b1-131">-RetentionDays</span></span>
<span data-ttu-id="c76b1-132">Azure depolama hizmeti 'nin ölçüm bilgilerini koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="c76b1-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c76b1-133">-ServiceType</span></span>
<span data-ttu-id="c76b1-134">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-134">Specifies the storage service type.</span></span>
<span data-ttu-id="c76b1-135">Bu cmdlet, bu parametrenin belirttiği hizmet türünün ölçüm özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c76b1-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c76b1-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c76b1-137">'Unu</span><span class="sxs-lookup"><span data-stu-id="c76b1-137">Blob</span></span> 
- <span data-ttu-id="c76b1-138">Tablo</span><span class="sxs-lookup"><span data-stu-id="c76b1-138">Table</span></span>
- <span data-ttu-id="c76b1-139">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="c76b1-139">Queue</span></span>
- <span data-ttu-id="c76b1-140">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c76b1-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c76b1-141">-Version</span><span class="sxs-lookup"><span data-stu-id="c76b1-141">-Version</span></span>
<span data-ttu-id="c76b1-142">Azure depolama alanı ölçümlerinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c76b1-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="c76b1-143">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="c76b1-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="c76b1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76b1-144">CommonParameters</span></span>
<span data-ttu-id="c76b1-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c76b1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76b1-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c76b1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76b1-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c76b1-147">INPUTS</span></span>

### <span data-ttu-id="c76b1-148">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="c76b1-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c76b1-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c76b1-149">OUTPUTS</span></span>

### <span data-ttu-id="c76b1-150">Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="c76b1-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="c76b1-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c76b1-151">NOTES</span></span>

## <span data-ttu-id="c76b1-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c76b1-152">RELATED LINKS</span></span>

[<span data-ttu-id="c76b1-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c76b1-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="c76b1-154">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c76b1-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


