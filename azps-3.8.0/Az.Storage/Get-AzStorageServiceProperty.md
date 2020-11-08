---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097758"
---
# <span data-ttu-id="52289-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="52289-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="52289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52289-102">SYNOPSIS</span></span>
<span data-ttu-id="52289-103">Azure Storage Services özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="52289-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="52289-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52289-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52289-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52289-105">DESCRIPTION</span></span>
<span data-ttu-id="52289-106">**Get-AzStorageServiceProperty** cmdlet 'ı, Azure Storage Services özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="52289-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="52289-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52289-107">EXAMPLES</span></span>

### <span data-ttu-id="52289-108">Örnek 1: Blob hizmetinin Azure Storage Services özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="52289-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="52289-109">Bu komut, Blob hizmetinin DefaultServiceVersion özelliğini alır.</span><span class="sxs-lookup"><span data-stu-id="52289-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="52289-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52289-110">PARAMETERS</span></span>

### <span data-ttu-id="52289-111">-Context</span><span class="sxs-lookup"><span data-stu-id="52289-111">-Context</span></span>
<span data-ttu-id="52289-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52289-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="52289-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="52289-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="52289-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52289-114">-DefaultProfile</span></span>
<span data-ttu-id="52289-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52289-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52289-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="52289-116">-ServiceType</span></span>
<span data-ttu-id="52289-117">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52289-117">Specifies the storage service type.</span></span>
<span data-ttu-id="52289-118">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="52289-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="52289-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="52289-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52289-120">'Unu</span><span class="sxs-lookup"><span data-stu-id="52289-120">Blob</span></span> 
- <span data-ttu-id="52289-121">Tablo</span><span class="sxs-lookup"><span data-stu-id="52289-121">Table</span></span>
- <span data-ttu-id="52289-122">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="52289-122">Queue</span></span>
- <span data-ttu-id="52289-123">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="52289-123">File</span></span>

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

### <span data-ttu-id="52289-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52289-124">CommonParameters</span></span>
<span data-ttu-id="52289-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52289-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52289-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52289-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52289-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52289-127">INPUTS</span></span>

### <span data-ttu-id="52289-128">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="52289-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="52289-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52289-129">OUTPUTS</span></span>

### <span data-ttu-id="52289-130">Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="52289-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="52289-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52289-131">NOTES</span></span>

## <span data-ttu-id="52289-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52289-132">RELATED LINKS</span></span>