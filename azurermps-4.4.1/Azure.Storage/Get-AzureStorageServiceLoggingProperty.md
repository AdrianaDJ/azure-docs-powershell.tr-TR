---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762084"
---
# <span data-ttu-id="21ee6-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="21ee6-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="21ee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="21ee6-103">Azure depolama hizmetleri için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="21ee6-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ee6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21ee6-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="21ee6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21ee6-105">DESCRIPTION</span></span>
<span data-ttu-id="21ee6-106">**Get-AzureStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="21ee6-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="21ee6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21ee6-107">EXAMPLES</span></span>

### <span data-ttu-id="21ee6-108">Örnek 1: blob hizmeti için günlük özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="21ee6-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="21ee6-109">Bu komut, BLOB depolama için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="21ee6-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="21ee6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21ee6-110">PARAMETERS</span></span>

### <span data-ttu-id="21ee6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="21ee6-111">-Context</span></span>
<span data-ttu-id="21ee6-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21ee6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="21ee6-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="21ee6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="21ee6-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="21ee6-114">-ServiceType</span></span>
<span data-ttu-id="21ee6-115">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="21ee6-115">Specifies the storage service type.</span></span>
<span data-ttu-id="21ee6-116">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="21ee6-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="21ee6-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="21ee6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21ee6-118">'Unu</span><span class="sxs-lookup"><span data-stu-id="21ee6-118">Blob</span></span> 
- <span data-ttu-id="21ee6-119">Tablo</span><span class="sxs-lookup"><span data-stu-id="21ee6-119">Table</span></span>
- <span data-ttu-id="21ee6-120">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="21ee6-120">Queue</span></span>
- <span data-ttu-id="21ee6-121">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="21ee6-121">File</span></span>

<span data-ttu-id="21ee6-122">Dosya değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="21ee6-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="21ee6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ee6-123">CommonParameters</span></span>
<span data-ttu-id="21ee6-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21ee6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ee6-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ee6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ee6-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21ee6-126">INPUTS</span></span>

### <span data-ttu-id="21ee6-127">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="21ee6-127">IStorageContext</span></span>

<span data-ttu-id="21ee6-128">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="21ee6-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="21ee6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21ee6-129">OUTPUTS</span></span>

### <span data-ttu-id="21ee6-130">Microsoft. Windowsazde. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="21ee6-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="21ee6-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21ee6-131">NOTES</span></span>

## <span data-ttu-id="21ee6-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21ee6-132">RELATED LINKS</span></span>

[<span data-ttu-id="21ee6-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="21ee6-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="21ee6-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="21ee6-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)

