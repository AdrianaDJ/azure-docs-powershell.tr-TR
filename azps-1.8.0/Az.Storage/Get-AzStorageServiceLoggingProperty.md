---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: ba82dcc5cae9b0ea8fa8bfa097c10da95cd91b15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758655"
---
# <span data-ttu-id="934de-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="934de-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="934de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="934de-102">SYNOPSIS</span></span>
<span data-ttu-id="934de-103">Azure depolama hizmetleri için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="934de-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="934de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="934de-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="934de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="934de-105">DESCRIPTION</span></span>
<span data-ttu-id="934de-106">**Get-AzStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="934de-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="934de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="934de-107">EXAMPLES</span></span>

### <span data-ttu-id="934de-108">Örnek 1: blob hizmeti için günlük özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="934de-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="934de-109">Bu komut, BLOB depolama için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="934de-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="934de-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="934de-110">PARAMETERS</span></span>

### <span data-ttu-id="934de-111">-Context</span><span class="sxs-lookup"><span data-stu-id="934de-111">-Context</span></span>
<span data-ttu-id="934de-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="934de-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="934de-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="934de-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="934de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934de-114">-DefaultProfile</span></span>
<span data-ttu-id="934de-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="934de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="934de-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="934de-116">-ServiceType</span></span>
<span data-ttu-id="934de-117">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="934de-117">Specifies the storage service type.</span></span>
<span data-ttu-id="934de-118">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="934de-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="934de-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="934de-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="934de-120">'Unu</span><span class="sxs-lookup"><span data-stu-id="934de-120">Blob</span></span> 
- <span data-ttu-id="934de-121">Tablo</span><span class="sxs-lookup"><span data-stu-id="934de-121">Table</span></span>
- <span data-ttu-id="934de-122">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="934de-122">Queue</span></span>
- <span data-ttu-id="934de-123">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="934de-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="934de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934de-124">CommonParameters</span></span>
<span data-ttu-id="934de-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="934de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934de-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="934de-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934de-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="934de-127">INPUTS</span></span>

### <span data-ttu-id="934de-128">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="934de-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="934de-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="934de-129">OUTPUTS</span></span>

### <span data-ttu-id="934de-130">Microsoft. Windowsazde. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="934de-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="934de-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="934de-131">NOTES</span></span>

## <span data-ttu-id="934de-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="934de-132">RELATED LINKS</span></span>

[<span data-ttu-id="934de-133">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="934de-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="934de-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="934de-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


