---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 1d7d536d7815206f942a89da4458f4669c0c9fd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939008"
---
# <span data-ttu-id="5bbea-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5bbea-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="5bbea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bbea-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbea-103">Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5bbea-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bbea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bbea-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bbea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bbea-105">DESCRIPTION</span></span>
<span data-ttu-id="5bbea-106">**Get-AzureStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5bbea-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="5bbea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bbea-107">EXAMPLES</span></span>

### <span data-ttu-id="5bbea-108">Örnek 1: blob hizmeti için ölçüm özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="5bbea-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="5bbea-109">Bu komut, saat ölçümü türü için BLOB depolama alanının ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5bbea-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="5bbea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bbea-110">PARAMETERS</span></span>

### <span data-ttu-id="5bbea-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5bbea-111">-Context</span></span>
<span data-ttu-id="5bbea-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bbea-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5bbea-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5bbea-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5bbea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbea-114">-DefaultProfile</span></span>
<span data-ttu-id="5bbea-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bbea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bbea-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="5bbea-116">-MetricsType</span></span>
<span data-ttu-id="5bbea-117">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bbea-117">Specifies a metrics type.</span></span>
<span data-ttu-id="5bbea-118">Bu cmdlet, bu parametrenin belirttiği ölçüm türü için Azure depolama hizmeti ölçümleri özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5bbea-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="5bbea-119">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="5bbea-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbea-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5bbea-120">-ServiceType</span></span>
<span data-ttu-id="5bbea-121">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bbea-121">Specifies the storage service type.</span></span>
<span data-ttu-id="5bbea-122">Bu cmdlet, bu parametrenin belirttiği türün ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5bbea-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="5bbea-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5bbea-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5bbea-124">'Unu</span><span class="sxs-lookup"><span data-stu-id="5bbea-124">Blob</span></span> 
- <span data-ttu-id="5bbea-125">Tablo</span><span class="sxs-lookup"><span data-stu-id="5bbea-125">Table</span></span>
- <span data-ttu-id="5bbea-126">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="5bbea-126">Queue</span></span>
- <span data-ttu-id="5bbea-127">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="5bbea-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="5bbea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbea-128">CommonParameters</span></span>
<span data-ttu-id="5bbea-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bbea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbea-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbea-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bbea-131">INPUTS</span></span>

### <span data-ttu-id="5bbea-132">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="5bbea-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5bbea-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bbea-133">OUTPUTS</span></span>

### <span data-ttu-id="5bbea-134">Microsoft. Windowsazme. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="5bbea-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="5bbea-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bbea-135">NOTES</span></span>

## <span data-ttu-id="5bbea-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bbea-136">RELATED LINKS</span></span>

[<span data-ttu-id="5bbea-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5bbea-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5bbea-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5bbea-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


