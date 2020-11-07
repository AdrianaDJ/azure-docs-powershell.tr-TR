---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: dc7f579366956f8447ba64fc898e97f5c33b70f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934038"
---
# <span data-ttu-id="7e6e1-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7e6e1-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="7e6e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6e1-103">Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="7e6e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e6e1-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e6e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e6e1-106">**Update-AzStorageServiceProperty** cmdlet 'ı Azure depolama hizmeti özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="7e6e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e6e1-107">EXAMPLES</span></span>

### <span data-ttu-id="7e6e1-108">Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2017-04-17 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="7e6e1-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="7e6e1-109">Bu komut Blob hizmetinin Defaultservicesürümünü 2017-04-17 olarak ayarladı</span><span class="sxs-lookup"><span data-stu-id="7e6e1-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="7e6e1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e6e1-110">PARAMETERS</span></span>

### <span data-ttu-id="7e6e1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7e6e1-111">-Context</span></span>
<span data-ttu-id="7e6e1-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7e6e1-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7e6e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6e1-114">-DefaultProfile</span></span>
<span data-ttu-id="7e6e1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e6e1-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="7e6e1-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="7e6e1-117">DefaultServiceVersion, gelen isteğin sürümü belirtilmemişse, blob hizmetine yapılan isteklerde kullanılacak varsayılan sürümü gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="7e6e1-118">Olası değerler sürüm 2008-10-27 ve tüm yeni sürümleri içerir.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="7e6e1-119">Diğer ayrıntılara bakın https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="7e6e1-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="7e6e1-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7e6e1-120">-PassThru</span></span>
<span data-ttu-id="7e6e1-121">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="7e6e1-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="7e6e1-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="7e6e1-122">-ServiceType</span></span>
<span data-ttu-id="7e6e1-123">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-123">Specifies the storage service type.</span></span>
<span data-ttu-id="7e6e1-124">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlüğe kaydetme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="7e6e1-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7e6e1-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e6e1-126">'Unu</span><span class="sxs-lookup"><span data-stu-id="7e6e1-126">Blob</span></span> 
- <span data-ttu-id="7e6e1-127">Tablo</span><span class="sxs-lookup"><span data-stu-id="7e6e1-127">Table</span></span>
- <span data-ttu-id="7e6e1-128">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="7e6e1-128">Queue</span></span>
- <span data-ttu-id="7e6e1-129">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="7e6e1-129">File</span></span>

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

### <span data-ttu-id="7e6e1-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e6e1-130">-Confirm</span></span>
<span data-ttu-id="7e6e1-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e6e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e6e1-132">-WhatIf</span></span>
<span data-ttu-id="7e6e1-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e6e1-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e6e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6e1-135">CommonParameters</span></span>
<span data-ttu-id="7e6e1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e6e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6e1-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e6e1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6e1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e6e1-138">INPUTS</span></span>

### <span data-ttu-id="7e6e1-139">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="7e6e1-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7e6e1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e6e1-140">OUTPUTS</span></span>

### <span data-ttu-id="7e6e1-141">Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="7e6e1-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="7e6e1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e6e1-142">NOTES</span></span>

## <span data-ttu-id="7e6e1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e6e1-143">RELATED LINKS</span></span>
