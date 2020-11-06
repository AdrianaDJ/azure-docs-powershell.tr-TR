---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: 28727ed903030c360b436edfac3d4cfb2a5d38ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590576"
---
# <span data-ttu-id="76b2a-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="76b2a-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="76b2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="76b2a-103">Azure Storage Services özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="76b2a-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76b2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76b2a-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="76b2a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76b2a-105">DESCRIPTION</span></span>
<span data-ttu-id="76b2a-106">**Get-AzureStorageServiceProperty** cmdlet 'ı, Azure Storage Services özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="76b2a-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="76b2a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76b2a-107">EXAMPLES</span></span>

### <span data-ttu-id="76b2a-108">Örnek 1: Blob hizmetinin Azure Storage Services özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="76b2a-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29

```

<span data-ttu-id="76b2a-109">Bu komut, Blob hizmetinin DefaultServiceVersion özelliğini alır.</span><span class="sxs-lookup"><span data-stu-id="76b2a-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="76b2a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76b2a-110">PARAMETERS</span></span>

### <span data-ttu-id="76b2a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="76b2a-111">-Context</span></span>
<span data-ttu-id="76b2a-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76b2a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="76b2a-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="76b2a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="76b2a-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="76b2a-114">-ServiceType</span></span>
<span data-ttu-id="76b2a-115">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="76b2a-115">Specifies the storage service type.</span></span>
<span data-ttu-id="76b2a-116">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="76b2a-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="76b2a-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="76b2a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76b2a-118">'Unu</span><span class="sxs-lookup"><span data-stu-id="76b2a-118">Blob</span></span> 
- <span data-ttu-id="76b2a-119">Tablo</span><span class="sxs-lookup"><span data-stu-id="76b2a-119">Table</span></span>
- <span data-ttu-id="76b2a-120">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="76b2a-120">Queue</span></span>
- <span data-ttu-id="76b2a-121">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="76b2a-121">File</span></span>

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

### <span data-ttu-id="76b2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b2a-122">CommonParameters</span></span>
<span data-ttu-id="76b2a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76b2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b2a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b2a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b2a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76b2a-125">INPUTS</span></span>

### <span data-ttu-id="76b2a-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="76b2a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="76b2a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76b2a-127">OUTPUTS</span></span>

### <span data-ttu-id="76b2a-128">Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="76b2a-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="76b2a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76b2a-129">NOTES</span></span>

## <span data-ttu-id="76b2a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76b2a-130">RELATED LINKS</span></span>

