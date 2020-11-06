---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572362"
---
# <span data-ttu-id="71c58-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="71c58-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="71c58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71c58-102">SYNOPSIS</span></span>
<span data-ttu-id="71c58-103">Azure depolama hizmetleri için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="71c58-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="71c58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71c58-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="71c58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71c58-105">DESCRIPTION</span></span>
<span data-ttu-id="71c58-106">**Get-AzureStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="71c58-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="71c58-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71c58-107">EXAMPLES</span></span>

### <span data-ttu-id="71c58-108">Örnek 1: blob hizmeti için günlük özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="71c58-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="71c58-109">Bu komut, BLOB depolama için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="71c58-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="71c58-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71c58-110">PARAMETERS</span></span>

### <span data-ttu-id="71c58-111">-Context</span><span class="sxs-lookup"><span data-stu-id="71c58-111">-Context</span></span>
<span data-ttu-id="71c58-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71c58-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="71c58-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="71c58-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="71c58-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="71c58-114">-ServiceType</span></span>
<span data-ttu-id="71c58-115">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="71c58-115">Specifies the storage service type.</span></span>
<span data-ttu-id="71c58-116">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="71c58-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="71c58-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="71c58-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71c58-118">'Unu</span><span class="sxs-lookup"><span data-stu-id="71c58-118">Blob</span></span> 
- <span data-ttu-id="71c58-119">Tablo</span><span class="sxs-lookup"><span data-stu-id="71c58-119">Table</span></span>
- <span data-ttu-id="71c58-120">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="71c58-120">Queue</span></span>
- <span data-ttu-id="71c58-121">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="71c58-121">File</span></span>

<span data-ttu-id="71c58-122">Dosya değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="71c58-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="71c58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c58-123">CommonParameters</span></span>
<span data-ttu-id="71c58-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71c58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c58-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c58-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c58-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71c58-126">INPUTS</span></span>

## <span data-ttu-id="71c58-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71c58-127">OUTPUTS</span></span>

## <span data-ttu-id="71c58-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71c58-128">NOTES</span></span>

## <span data-ttu-id="71c58-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71c58-129">RELATED LINKS</span></span>

[<span data-ttu-id="71c58-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="71c58-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="71c58-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="71c58-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


