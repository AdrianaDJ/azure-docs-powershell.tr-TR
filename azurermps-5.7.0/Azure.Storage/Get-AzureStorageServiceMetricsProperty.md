---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 9d7e8f5d69d2f0e570cd7ce7fb21b29eb7f11648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590578"
---
# <span data-ttu-id="fcb49-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fcb49-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="fcb49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcb49-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb49-103">Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcb49-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcb49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcb49-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="fcb49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcb49-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb49-106">**Get-AzureStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcb49-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="fcb49-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcb49-107">EXAMPLES</span></span>

### <span data-ttu-id="fcb49-108">Örnek 1: blob hizmeti için ölçüm özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="fcb49-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="fcb49-109">Bu komut, saat ölçümü türü için BLOB depolama alanının ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcb49-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="fcb49-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcb49-110">PARAMETERS</span></span>

### <span data-ttu-id="fcb49-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fcb49-111">-Context</span></span>
<span data-ttu-id="fcb49-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcb49-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fcb49-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fcb49-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fcb49-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="fcb49-114">-MetricsType</span></span>
<span data-ttu-id="fcb49-115">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcb49-115">Specifies a metrics type.</span></span>
<span data-ttu-id="fcb49-116">Bu cmdlet, bu parametrenin belirttiği ölçüm türü için Azure depolama hizmeti ölçümleri özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcb49-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="fcb49-117">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="fcb49-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="fcb49-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fcb49-118">-ServiceType</span></span>
<span data-ttu-id="fcb49-119">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcb49-119">Specifies the storage service type.</span></span>
<span data-ttu-id="fcb49-120">Bu cmdlet, bu parametrenin belirttiği türün ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcb49-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="fcb49-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fcb49-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcb49-122">'Unu</span><span class="sxs-lookup"><span data-stu-id="fcb49-122">Blob</span></span> 
- <span data-ttu-id="fcb49-123">Tablo</span><span class="sxs-lookup"><span data-stu-id="fcb49-123">Table</span></span>
- <span data-ttu-id="fcb49-124">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="fcb49-124">Queue</span></span>
- <span data-ttu-id="fcb49-125">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="fcb49-125">File</span></span> 

<span data-ttu-id="fcb49-126">Dosya değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="fcb49-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="fcb49-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb49-127">CommonParameters</span></span>
<span data-ttu-id="fcb49-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcb49-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb49-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb49-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb49-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcb49-130">INPUTS</span></span>

### <span data-ttu-id="fcb49-131">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="fcb49-131">IStorageContext</span></span>

<span data-ttu-id="fcb49-132">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fcb49-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="fcb49-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcb49-133">OUTPUTS</span></span>

### <span data-ttu-id="fcb49-134">Microsoft. Windowsazme. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="fcb49-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="fcb49-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcb49-135">NOTES</span></span>

## <span data-ttu-id="fcb49-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcb49-136">RELATED LINKS</span></span>

[<span data-ttu-id="fcb49-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fcb49-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fcb49-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fcb49-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


