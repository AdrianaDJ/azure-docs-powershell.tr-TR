---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: b622f117549a77c54a24964240cd6d17a084993d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762823"
---
# <span data-ttu-id="a9def-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a9def-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="a9def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9def-102">SYNOPSIS</span></span>
<span data-ttu-id="a9def-103">Azure depolama hizmetleri için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="a9def-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9def-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9def-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9def-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9def-105">DESCRIPTION</span></span>
<span data-ttu-id="a9def-106">**Get-AzureStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="a9def-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="a9def-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9def-107">EXAMPLES</span></span>

### <span data-ttu-id="a9def-108">Örnek 1: blob hizmeti için günlük özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="a9def-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="a9def-109">Bu komut, BLOB depolama için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="a9def-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="a9def-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9def-110">PARAMETERS</span></span>

### <span data-ttu-id="a9def-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a9def-111">-Context</span></span>
<span data-ttu-id="a9def-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9def-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a9def-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9def-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a9def-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9def-114">-DefaultProfile</span></span>
<span data-ttu-id="a9def-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9def-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9def-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a9def-116">-ServiceType</span></span>
<span data-ttu-id="a9def-117">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9def-117">Specifies the storage service type.</span></span>
<span data-ttu-id="a9def-118">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="a9def-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="a9def-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a9def-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9def-120">'Unu</span><span class="sxs-lookup"><span data-stu-id="a9def-120">Blob</span></span> 
- <span data-ttu-id="a9def-121">Tablo</span><span class="sxs-lookup"><span data-stu-id="a9def-121">Table</span></span>
- <span data-ttu-id="a9def-122">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="a9def-122">Queue</span></span>
- <span data-ttu-id="a9def-123">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="a9def-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="a9def-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9def-124">CommonParameters</span></span>
<span data-ttu-id="a9def-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9def-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9def-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9def-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9def-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9def-127">INPUTS</span></span>

### <span data-ttu-id="a9def-128">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="a9def-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9def-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9def-129">OUTPUTS</span></span>

### <span data-ttu-id="a9def-130">Microsoft. Windowsazde. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="a9def-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="a9def-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9def-131">NOTES</span></span>

## <span data-ttu-id="a9def-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9def-132">RELATED LINKS</span></span>

[<span data-ttu-id="a9def-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9def-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a9def-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a9def-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


