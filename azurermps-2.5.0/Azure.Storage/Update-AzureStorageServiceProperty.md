---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: 2f0c59acba56fb80a12df0c5df6c8168ebc91000
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939955"
---
# <span data-ttu-id="37861-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="37861-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="37861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37861-102">SYNOPSIS</span></span>
<span data-ttu-id="37861-103">Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="37861-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37861-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37861-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37861-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="37861-105">DESCRIPTION</span></span>
<span data-ttu-id="37861-106">**Update-AzureStorageServiceProperty** cmdlet 'ı Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="37861-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="37861-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37861-107">EXAMPLES</span></span>

### <span data-ttu-id="37861-108">Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2017-04-17 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="37861-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="37861-109">Bu komut Blob hizmetinin Defaultservicesürümünü 2017-04-17 olarak ayarladı</span><span class="sxs-lookup"><span data-stu-id="37861-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="37861-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37861-110">PARAMETERS</span></span>

### <span data-ttu-id="37861-111">-Context</span><span class="sxs-lookup"><span data-stu-id="37861-111">-Context</span></span>
<span data-ttu-id="37861-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37861-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="37861-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="37861-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="37861-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37861-114">-DefaultProfile</span></span>
<span data-ttu-id="37861-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37861-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37861-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="37861-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="37861-117">DefaultServiceVersion, gelen isteğin sürümü belirtilmemişse, blob hizmetine yapılan isteklerde kullanılacak varsayılan sürümü gösterir.</span><span class="sxs-lookup"><span data-stu-id="37861-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="37861-118">Olası değerler sürüm 2008-10-27 ve tüm yeni sürümleri içerir.</span><span class="sxs-lookup"><span data-stu-id="37861-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="37861-119">Diğer ayrıntılara bakın https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="37861-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

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

### <span data-ttu-id="37861-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="37861-120">-PassThru</span></span>
<span data-ttu-id="37861-121">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="37861-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="37861-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="37861-122">-ServiceType</span></span>
<span data-ttu-id="37861-123">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="37861-123">Specifies the storage service type.</span></span>
<span data-ttu-id="37861-124">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="37861-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="37861-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="37861-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37861-126">'Unu</span><span class="sxs-lookup"><span data-stu-id="37861-126">Blob</span></span> 
- <span data-ttu-id="37861-127">Tablo</span><span class="sxs-lookup"><span data-stu-id="37861-127">Table</span></span>
- <span data-ttu-id="37861-128">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="37861-128">Queue</span></span>
- <span data-ttu-id="37861-129">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="37861-129">File</span></span>

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

### <span data-ttu-id="37861-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="37861-130">-Confirm</span></span>
<span data-ttu-id="37861-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37861-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37861-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37861-132">-WhatIf</span></span>
<span data-ttu-id="37861-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37861-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37861-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37861-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37861-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37861-135">CommonParameters</span></span>
<span data-ttu-id="37861-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37861-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37861-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37861-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37861-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37861-138">INPUTS</span></span>

### <span data-ttu-id="37861-139">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="37861-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="37861-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37861-140">OUTPUTS</span></span>

### <span data-ttu-id="37861-141">Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="37861-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="37861-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37861-142">NOTES</span></span>

## <span data-ttu-id="37861-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37861-143">RELATED LINKS</span></span>
