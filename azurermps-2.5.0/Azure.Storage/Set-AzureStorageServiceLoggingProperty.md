---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: 810dc3246e1b1d49db491c030446117dbabfb548
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940210"
---
# <span data-ttu-id="5dff5-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5dff5-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="5dff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dff5-102">SYNOPSIS</span></span>
<span data-ttu-id="5dff5-103">Azure Depolama hizmetlerinin günlüğe kaydedilmesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dff5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5dff5-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dff5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5dff5-105">DESCRIPTION</span></span>
<span data-ttu-id="5dff5-106">**Set-AzureStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlüğe kaydetmeyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="5dff5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5dff5-107">EXAMPLES</span></span>

### <span data-ttu-id="5dff5-108">Örnek 1: blob hizmeti için günlük özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="5dff5-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="5dff5-109">Bu komut, BLOB depolama için sürüm 1,0 günlüğünü okuma ve yazma işlemlerini içerecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="5dff5-110">Azure depolama hizmeti günlüğü 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="5dff5-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="5dff5-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş günlük özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="5dff5-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="5dff5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5dff5-112">PARAMETERS</span></span>

### <span data-ttu-id="5dff5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5dff5-113">-Context</span></span>
<span data-ttu-id="5dff5-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5dff5-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5dff5-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5dff5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dff5-116">-DefaultProfile</span></span>
<span data-ttu-id="5dff5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5dff5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dff5-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="5dff5-118">-LoggingOperations</span></span>
<span data-ttu-id="5dff5-119">Azure depolama hizmeti işlemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="5dff5-120">Azure depolama hizmetleri, bu parametrenin belirttiği işlemleri günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5dff5-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="5dff5-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5dff5-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5dff5-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5dff5-122">None</span></span>
- <span data-ttu-id="5dff5-123">Okuması</span><span class="sxs-lookup"><span data-stu-id="5dff5-123">Read</span></span>
- <span data-ttu-id="5dff5-124">Yazmaktır</span><span class="sxs-lookup"><span data-stu-id="5dff5-124">Write</span></span>
- <span data-ttu-id="5dff5-125">Silme</span><span class="sxs-lookup"><span data-stu-id="5dff5-125">Delete</span></span>
- <span data-ttu-id="5dff5-126">Tüm</span><span class="sxs-lookup"><span data-stu-id="5dff5-126">All</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dff5-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5dff5-127">-PassThru</span></span>
<span data-ttu-id="5dff5-128">Bu cmdlet 'in güncelleştirilmiş günlüğe kaydetme özelliklerini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="5dff5-129">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="5dff5-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5dff5-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="5dff5-130">-RetentionDays</span></span>
<span data-ttu-id="5dff5-131">Azure depolama hizmeti 'nin günlüğe kaydedilen bilgileri koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="5dff5-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5dff5-132">-ServiceType</span></span>
<span data-ttu-id="5dff5-133">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-133">Specifies the storage service type.</span></span>
<span data-ttu-id="5dff5-134">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlük özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="5dff5-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5dff5-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5dff5-136">'Unu</span><span class="sxs-lookup"><span data-stu-id="5dff5-136">Blob</span></span> 
- <span data-ttu-id="5dff5-137">Tablo</span><span class="sxs-lookup"><span data-stu-id="5dff5-137">Table</span></span>
- <span data-ttu-id="5dff5-138">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="5dff5-138">Queue</span></span>
- <span data-ttu-id="5dff5-139">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="5dff5-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="5dff5-140">-Version</span><span class="sxs-lookup"><span data-stu-id="5dff5-140">-Version</span></span>
<span data-ttu-id="5dff5-141">Azure depolama hizmeti günlüğünün sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5dff5-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="5dff5-142">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5dff5-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="5dff5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dff5-143">CommonParameters</span></span>
<span data-ttu-id="5dff5-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5dff5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dff5-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dff5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dff5-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5dff5-146">INPUTS</span></span>

### <span data-ttu-id="5dff5-147">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="5dff5-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5dff5-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5dff5-148">OUTPUTS</span></span>

### <span data-ttu-id="5dff5-149">Microsoft. Windowsazde. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="5dff5-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="5dff5-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5dff5-150">NOTES</span></span>

## <span data-ttu-id="5dff5-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5dff5-151">RELATED LINKS</span></span>

[<span data-ttu-id="5dff5-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5dff5-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="5dff5-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5dff5-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


