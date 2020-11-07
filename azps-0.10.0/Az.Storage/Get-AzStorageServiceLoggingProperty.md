---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: fc1cbddd59d52816b0f7ef3bd664405a98ead518
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936253"
---
# <span data-ttu-id="6078b-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6078b-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="6078b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6078b-102">SYNOPSIS</span></span>
<span data-ttu-id="6078b-103">Azure depolama hizmetleri için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6078b-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="6078b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6078b-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6078b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6078b-105">DESCRIPTION</span></span>
<span data-ttu-id="6078b-106">**Get-AzStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6078b-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="6078b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6078b-107">EXAMPLES</span></span>

### <span data-ttu-id="6078b-108">Örnek 1: blob hizmeti için günlük özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6078b-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="6078b-109">Bu komut, BLOB depolama için günlük özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6078b-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="6078b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6078b-110">PARAMETERS</span></span>

### <span data-ttu-id="6078b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6078b-111">-Context</span></span>
<span data-ttu-id="6078b-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6078b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6078b-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6078b-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6078b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6078b-114">-DefaultProfile</span></span>
<span data-ttu-id="6078b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6078b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6078b-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6078b-116">-ServiceType</span></span>
<span data-ttu-id="6078b-117">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6078b-117">Specifies the storage service type.</span></span>
<span data-ttu-id="6078b-118">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6078b-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6078b-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6078b-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6078b-120">'Unu</span><span class="sxs-lookup"><span data-stu-id="6078b-120">Blob</span></span> 
- <span data-ttu-id="6078b-121">Tablo</span><span class="sxs-lookup"><span data-stu-id="6078b-121">Table</span></span>
- <span data-ttu-id="6078b-122">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="6078b-122">Queue</span></span>
- <span data-ttu-id="6078b-123">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="6078b-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="6078b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6078b-124">CommonParameters</span></span>
<span data-ttu-id="6078b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6078b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6078b-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6078b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6078b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6078b-127">INPUTS</span></span>

### <span data-ttu-id="6078b-128">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="6078b-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6078b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6078b-129">OUTPUTS</span></span>

### <span data-ttu-id="6078b-130">Microsoft. WindowsAz. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="6078b-130">Microsoft.WindowsAz.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="6078b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6078b-131">NOTES</span></span>

## <span data-ttu-id="6078b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6078b-132">RELATED LINKS</span></span>

[<span data-ttu-id="6078b-133">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6078b-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="6078b-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6078b-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


