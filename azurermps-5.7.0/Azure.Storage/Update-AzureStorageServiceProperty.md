---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592989"
---
# <span data-ttu-id="48fea-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="48fea-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="48fea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48fea-102">SYNOPSIS</span></span>
<span data-ttu-id="48fea-103">Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="48fea-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48fea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48fea-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48fea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48fea-105">DESCRIPTION</span></span>
<span data-ttu-id="48fea-106">**Update-AzureStorageServiceProperty** cmdlet 'ı Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="48fea-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="48fea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48fea-107">EXAMPLES</span></span>

### <span data-ttu-id="48fea-108">Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2017-04-17 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="48fea-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="48fea-109">Bu komut Blob hizmetinin Defaultservicesürümünü 2017-04-17 olarak ayarladı</span><span class="sxs-lookup"><span data-stu-id="48fea-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="48fea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48fea-110">PARAMETERS</span></span>

### <span data-ttu-id="48fea-111">-Context</span><span class="sxs-lookup"><span data-stu-id="48fea-111">-Context</span></span>
<span data-ttu-id="48fea-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48fea-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="48fea-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="48fea-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="48fea-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="48fea-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="48fea-115">DefaultServiceVersion, gelen isteğin sürümü belirtilmemişse, blob hizmetine yapılan isteklerde kullanılacak varsayılan sürümü gösterir.</span><span class="sxs-lookup"><span data-stu-id="48fea-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="48fea-116">Olası değerler sürüm 2008-10-27 ve tüm yeni sürümleri içerir.</span><span class="sxs-lookup"><span data-stu-id="48fea-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="48fea-117">Diğer ayrıntılara bakın https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="48fea-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48fea-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="48fea-118">-PassThru</span></span>
<span data-ttu-id="48fea-119">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="48fea-119">Display ServiceProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48fea-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="48fea-120">-ServiceType</span></span>
<span data-ttu-id="48fea-121">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="48fea-121">Specifies the storage service type.</span></span>
<span data-ttu-id="48fea-122">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="48fea-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="48fea-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48fea-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48fea-124">'Unu</span><span class="sxs-lookup"><span data-stu-id="48fea-124">Blob</span></span> 
- <span data-ttu-id="48fea-125">Tablo</span><span class="sxs-lookup"><span data-stu-id="48fea-125">Table</span></span>
- <span data-ttu-id="48fea-126">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="48fea-126">Queue</span></span>
- <span data-ttu-id="48fea-127">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="48fea-127">File</span></span>

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

### <span data-ttu-id="48fea-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="48fea-128">-Confirm</span></span>
<span data-ttu-id="48fea-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48fea-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48fea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48fea-130">-WhatIf</span></span>
<span data-ttu-id="48fea-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48fea-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48fea-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48fea-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48fea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fea-133">CommonParameters</span></span>
<span data-ttu-id="48fea-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48fea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fea-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48fea-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fea-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48fea-136">INPUTS</span></span>

### <span data-ttu-id="48fea-137">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="48fea-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="48fea-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48fea-138">OUTPUTS</span></span>

### <span data-ttu-id="48fea-139">Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="48fea-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="48fea-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48fea-140">NOTES</span></span>

## <span data-ttu-id="48fea-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48fea-141">RELATED LINKS</span></span>

