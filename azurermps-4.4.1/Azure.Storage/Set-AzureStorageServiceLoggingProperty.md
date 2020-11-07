---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: baba161c849918c95d5e1df91330dfd96a4c5629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593869"
---
# <span data-ttu-id="27265-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="27265-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="27265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27265-102">SYNOPSIS</span></span>
<span data-ttu-id="27265-103">Azure Depolama hizmetlerinin günlüğe kaydedilmesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="27265-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27265-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27265-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="27265-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27265-105">DESCRIPTION</span></span>
<span data-ttu-id="27265-106">**Set-AzureStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlüğe kaydetmeyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="27265-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="27265-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27265-107">EXAMPLES</span></span>

### <span data-ttu-id="27265-108">Örnek 1: blob hizmeti için günlük özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="27265-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="27265-109">Bu komut, BLOB depolama için sürüm 1,0 günlüğünü okuma ve yazma işlemlerini içerecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="27265-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="27265-110">Azure depolama hizmeti günlüğü 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="27265-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="27265-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş günlük özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="27265-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="27265-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27265-112">PARAMETERS</span></span>

### <span data-ttu-id="27265-113">-Context</span><span class="sxs-lookup"><span data-stu-id="27265-113">-Context</span></span>
<span data-ttu-id="27265-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27265-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="27265-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="27265-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="27265-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="27265-116">-LoggingOperations</span></span>
<span data-ttu-id="27265-117">Azure depolama hizmeti işlemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27265-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="27265-118">Azure depolama hizmetleri, bu parametrenin belirttiği işlemleri günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="27265-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="27265-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27265-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27265-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="27265-120">None</span></span>
- <span data-ttu-id="27265-121">Okuması</span><span class="sxs-lookup"><span data-stu-id="27265-121">Read</span></span>
- <span data-ttu-id="27265-122">Yazmaktır</span><span class="sxs-lookup"><span data-stu-id="27265-122">Write</span></span>
- <span data-ttu-id="27265-123">Silme</span><span class="sxs-lookup"><span data-stu-id="27265-123">Delete</span></span>
- <span data-ttu-id="27265-124">Tüm</span><span class="sxs-lookup"><span data-stu-id="27265-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27265-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="27265-125">-PassThru</span></span>
<span data-ttu-id="27265-126">Bu cmdlet 'in güncelleştirilmiş günlüğe kaydetme özelliklerini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27265-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="27265-127">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="27265-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="27265-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="27265-128">-RetentionDays</span></span>
<span data-ttu-id="27265-129">Azure depolama hizmeti 'nin günlüğe kaydedilen bilgileri koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27265-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="27265-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="27265-130">-ServiceType</span></span>
<span data-ttu-id="27265-131">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="27265-131">Specifies the storage service type.</span></span>
<span data-ttu-id="27265-132">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlük özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="27265-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="27265-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27265-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27265-134">'Unu</span><span class="sxs-lookup"><span data-stu-id="27265-134">Blob</span></span> 
- <span data-ttu-id="27265-135">Tablo</span><span class="sxs-lookup"><span data-stu-id="27265-135">Table</span></span>
- <span data-ttu-id="27265-136">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="27265-136">Queue</span></span>
- <span data-ttu-id="27265-137">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="27265-137">File</span></span>

<span data-ttu-id="27265-138">Dosya değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="27265-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="27265-139">-Version</span><span class="sxs-lookup"><span data-stu-id="27265-139">-Version</span></span>
<span data-ttu-id="27265-140">Azure depolama hizmeti günlüğünün sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="27265-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="27265-141">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="27265-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="27265-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27265-142">CommonParameters</span></span>
<span data-ttu-id="27265-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27265-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27265-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27265-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27265-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27265-145">INPUTS</span></span>

### <span data-ttu-id="27265-146">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="27265-146">IStorageContext</span></span>

<span data-ttu-id="27265-147">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="27265-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="27265-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27265-148">OUTPUTS</span></span>

### <span data-ttu-id="27265-149">Microsoft. Windowsazde. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="27265-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="27265-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27265-150">NOTES</span></span>

## <span data-ttu-id="27265-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27265-151">RELATED LINKS</span></span>

[<span data-ttu-id="27265-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="27265-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="27265-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="27265-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

