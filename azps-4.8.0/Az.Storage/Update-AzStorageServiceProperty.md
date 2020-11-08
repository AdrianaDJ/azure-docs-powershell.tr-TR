---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266236"
---
# <span data-ttu-id="ba4bb-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ba4bb-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="ba4bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4bb-103">Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ba4bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba4bb-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba4bb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba4bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4bb-106">**Update-AzStorageServiceProperty** cmdlet 'ı Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ba4bb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba4bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4bb-108">Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2017-04-17 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="ba4bb-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="ba4bb-109">Bu komut Blob hizmetinin Defaultservicesürümünü 2017-04-17 olarak ayarladı</span><span class="sxs-lookup"><span data-stu-id="ba4bb-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="ba4bb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba4bb-110">PARAMETERS</span></span>

### <span data-ttu-id="ba4bb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ba4bb-111">-Context</span></span>
<span data-ttu-id="ba4bb-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ba4bb-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ba4bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4bb-114">-DefaultProfile</span></span>
<span data-ttu-id="ba4bb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba4bb-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="ba4bb-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="ba4bb-117">DefaultServiceVersion, gelen isteğin sürümü belirtilmemişse, blob hizmetine yapılan isteklerde kullanılacak varsayılan sürümü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="ba4bb-118">Olası değerler sürüm 2008-10-27 ve tüm yeni sürümleri içerir.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="ba4bb-119">Diğer ayrıntılara bakın https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="ba4bb-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4bb-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba4bb-120">-PassThru</span></span>
<span data-ttu-id="ba4bb-121">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ba4bb-121">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4bb-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ba4bb-122">-ServiceType</span></span>
<span data-ttu-id="ba4bb-123">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-123">Specifies the storage service type.</span></span>
<span data-ttu-id="ba4bb-124">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ba4bb-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ba4bb-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba4bb-126">'Unu</span><span class="sxs-lookup"><span data-stu-id="ba4bb-126">Blob</span></span> 
- <span data-ttu-id="ba4bb-127">Tablo</span><span class="sxs-lookup"><span data-stu-id="ba4bb-127">Table</span></span>
- <span data-ttu-id="ba4bb-128">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="ba4bb-128">Queue</span></span>
- <span data-ttu-id="ba4bb-129">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="ba4bb-129">File</span></span>

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

### <span data-ttu-id="ba4bb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba4bb-130">-Confirm</span></span>
<span data-ttu-id="ba4bb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba4bb-132">-WhatIf</span></span>
<span data-ttu-id="ba4bb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba4bb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4bb-135">CommonParameters</span></span>
<span data-ttu-id="ba4bb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4bb-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4bb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4bb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba4bb-138">INPUTS</span></span>

### <span data-ttu-id="ba4bb-139">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="ba4bb-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ba4bb-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba4bb-140">OUTPUTS</span></span>

### <span data-ttu-id="ba4bb-141">Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="ba4bb-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="ba4bb-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba4bb-142">NOTES</span></span>

## <span data-ttu-id="ba4bb-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba4bb-143">RELATED LINKS</span></span>
