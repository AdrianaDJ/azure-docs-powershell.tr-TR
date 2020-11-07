---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 7bca28da7b4729a414fafc5268bc4e0e02ee3c72
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936251"
---
# <span data-ttu-id="30dd3-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="30dd3-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="30dd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="30dd3-103">Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="30dd3-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="30dd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30dd3-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30dd3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30dd3-105">DESCRIPTION</span></span>
<span data-ttu-id="30dd3-106">**Get-AzStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti için ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="30dd3-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="30dd3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30dd3-107">EXAMPLES</span></span>

### <span data-ttu-id="30dd3-108">Örnek 1: blob hizmeti için ölçüm özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="30dd3-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="30dd3-109">Bu komut, saat ölçümü türü için BLOB depolama alanının ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="30dd3-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="30dd3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30dd3-110">PARAMETERS</span></span>

### <span data-ttu-id="30dd3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="30dd3-111">-Context</span></span>
<span data-ttu-id="30dd3-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30dd3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="30dd3-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="30dd3-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="30dd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30dd3-114">-DefaultProfile</span></span>
<span data-ttu-id="30dd3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30dd3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30dd3-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="30dd3-116">-MetricsType</span></span>
<span data-ttu-id="30dd3-117">Ölçüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="30dd3-117">Specifies a metrics type.</span></span>
<span data-ttu-id="30dd3-118">Bu cmdlet, bu parametrenin belirttiği ölçüm türü için Azure depolama hizmeti ölçümleri özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="30dd3-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="30dd3-119">Bu parametre için kabul edilebilir değerler: Hour ve Minute.</span><span class="sxs-lookup"><span data-stu-id="30dd3-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="30dd3-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="30dd3-120">-ServiceType</span></span>
<span data-ttu-id="30dd3-121">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="30dd3-121">Specifies the storage service type.</span></span>
<span data-ttu-id="30dd3-122">Bu cmdlet, bu parametrenin belirttiği türün ölçüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="30dd3-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="30dd3-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="30dd3-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30dd3-124">'Unu</span><span class="sxs-lookup"><span data-stu-id="30dd3-124">Blob</span></span> 
- <span data-ttu-id="30dd3-125">Tablo</span><span class="sxs-lookup"><span data-stu-id="30dd3-125">Table</span></span>
- <span data-ttu-id="30dd3-126">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="30dd3-126">Queue</span></span>
- <span data-ttu-id="30dd3-127">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="30dd3-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="30dd3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30dd3-128">CommonParameters</span></span>
<span data-ttu-id="30dd3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30dd3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30dd3-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30dd3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30dd3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30dd3-131">INPUTS</span></span>

### <span data-ttu-id="30dd3-132">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="30dd3-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="30dd3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30dd3-133">OUTPUTS</span></span>

### <span data-ttu-id="30dd3-134">Microsoft. WindowsAz. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="30dd3-134">Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="30dd3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30dd3-135">NOTES</span></span>

## <span data-ttu-id="30dd3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30dd3-136">RELATED LINKS</span></span>

[<span data-ttu-id="30dd3-137">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="30dd3-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="30dd3-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="30dd3-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


