---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572357"
---
# <span data-ttu-id="ba1e6-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ba1e6-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="ba1e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1e6-103">Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ba1e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba1e6-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ba1e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba1e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ba1e6-106">**Get-AzureStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ba1e6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba1e6-107">EXAMPLES</span></span>

### <span data-ttu-id="ba1e6-108">Örnek 1: blob hizmeti için ölçüm özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="ba1e6-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="ba1e6-109">Bu komut, saat ölçümü türü için BLOB depolama alanının ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="ba1e6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba1e6-110">PARAMETERS</span></span>

### <span data-ttu-id="ba1e6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ba1e6-111">-Context</span></span>
<span data-ttu-id="ba1e6-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ba1e6-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ba1e6-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="ba1e6-114">-MetricsType</span></span>
<span data-ttu-id="ba1e6-115">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-115">Specifies a metrics type.</span></span>
<span data-ttu-id="ba1e6-116">Bu cmdlet, bu parametrenin belirttiği ölçüm türü için Azure depolama hizmeti ölçümleri özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="ba1e6-117">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="ba1e6-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ba1e6-118">-ServiceType</span></span>
<span data-ttu-id="ba1e6-119">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-119">Specifies the storage service type.</span></span>
<span data-ttu-id="ba1e6-120">Bu cmdlet, bu parametrenin belirttiği türün ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="ba1e6-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ba1e6-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba1e6-122">'Unu</span><span class="sxs-lookup"><span data-stu-id="ba1e6-122">Blob</span></span> 
- <span data-ttu-id="ba1e6-123">Tablo</span><span class="sxs-lookup"><span data-stu-id="ba1e6-123">Table</span></span>
- <span data-ttu-id="ba1e6-124">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="ba1e6-124">Queue</span></span>
- <span data-ttu-id="ba1e6-125">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="ba1e6-125">File</span></span> 

<span data-ttu-id="ba1e6-126">Dosya değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ba1e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1e6-127">CommonParameters</span></span>
<span data-ttu-id="ba1e6-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba1e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1e6-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1e6-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba1e6-130">INPUTS</span></span>

## <span data-ttu-id="ba1e6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba1e6-131">OUTPUTS</span></span>

## <span data-ttu-id="ba1e6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba1e6-132">NOTES</span></span>

## <span data-ttu-id="ba1e6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba1e6-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba1e6-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ba1e6-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ba1e6-135">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ba1e6-135">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


