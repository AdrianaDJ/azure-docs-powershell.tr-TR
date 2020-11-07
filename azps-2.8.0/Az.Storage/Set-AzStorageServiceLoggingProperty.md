---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 43b8c6426fe2d4eceab65fc1b103e62cdb1eb346
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751316"
---
# <span data-ttu-id="c25ce-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c25ce-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="c25ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c25ce-103">Azure Depolama hizmetlerinin günlüğe kaydedilmesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="c25ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c25ce-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c25ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c25ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c25ce-106">**Set-AzStorageServiceLoggingProperty** cmdlet 'ı Azure Storage Services için günlüğe kaydetmeyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="c25ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c25ce-107">EXAMPLES</span></span>

### <span data-ttu-id="c25ce-108">Örnek 1: blob hizmeti için günlük özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c25ce-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="c25ce-109">Bu komut, BLOB depolama için sürüm 1,0 günlüğünü okuma ve yazma işlemlerini içerecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="c25ce-110">Azure depolama hizmeti günlüğü 10 günlük girişleri korur.</span><span class="sxs-lookup"><span data-stu-id="c25ce-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="c25ce-111">Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş günlük özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c25ce-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="c25ce-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c25ce-112">PARAMETERS</span></span>

### <span data-ttu-id="c25ce-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c25ce-113">-Context</span></span>
<span data-ttu-id="c25ce-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c25ce-115">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c25ce-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c25ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25ce-116">-DefaultProfile</span></span>
<span data-ttu-id="c25ce-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c25ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25ce-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="c25ce-118">-LoggingOperations</span></span>
<span data-ttu-id="c25ce-119">Azure depolama hizmeti işlemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="c25ce-120">Azure depolama hizmetleri, bu parametrenin belirttiği işlemleri günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c25ce-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="c25ce-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c25ce-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c25ce-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c25ce-122">None</span></span>
- <span data-ttu-id="c25ce-123">Okuması</span><span class="sxs-lookup"><span data-stu-id="c25ce-123">Read</span></span>
- <span data-ttu-id="c25ce-124">Yazmaktır</span><span class="sxs-lookup"><span data-stu-id="c25ce-124">Write</span></span>
- <span data-ttu-id="c25ce-125">Silme</span><span class="sxs-lookup"><span data-stu-id="c25ce-125">Delete</span></span>
- <span data-ttu-id="c25ce-126">Tüm</span><span class="sxs-lookup"><span data-stu-id="c25ce-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25ce-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c25ce-127">-PassThru</span></span>
<span data-ttu-id="c25ce-128">Bu cmdlet 'in güncelleştirilmiş günlüğe kaydetme özelliklerini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="c25ce-129">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c25ce-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c25ce-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c25ce-130">-RetentionDays</span></span>
<span data-ttu-id="c25ce-131">Azure depolama hizmeti 'nin günlüğe kaydedilen bilgileri koruduğu gün sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25ce-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c25ce-132">-ServiceType</span></span>
<span data-ttu-id="c25ce-133">Depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-133">Specifies the storage service type.</span></span>
<span data-ttu-id="c25ce-134">Bu cmdlet, bu parametrenin belirttiği hizmet türünün günlük özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c25ce-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c25ce-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c25ce-136">'Unu</span><span class="sxs-lookup"><span data-stu-id="c25ce-136">Blob</span></span> 
- <span data-ttu-id="c25ce-137">Tablo</span><span class="sxs-lookup"><span data-stu-id="c25ce-137">Table</span></span>
- <span data-ttu-id="c25ce-138">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="c25ce-138">Queue</span></span>
- <span data-ttu-id="c25ce-139">Dosya dosyanın değeri şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c25ce-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c25ce-140">-Version</span><span class="sxs-lookup"><span data-stu-id="c25ce-140">-Version</span></span>
<span data-ttu-id="c25ce-141">Azure depolama hizmeti günlüğünün sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c25ce-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="c25ce-142">Varsayılan değer 1,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="c25ce-142">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25ce-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25ce-143">CommonParameters</span></span>
<span data-ttu-id="c25ce-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c25ce-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25ce-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25ce-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25ce-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c25ce-146">INPUTS</span></span>

### <span data-ttu-id="c25ce-147">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="c25ce-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c25ce-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c25ce-148">OUTPUTS</span></span>

### <span data-ttu-id="c25ce-149">Microsoft. Azure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="c25ce-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="c25ce-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c25ce-150">NOTES</span></span>

## <span data-ttu-id="c25ce-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c25ce-151">RELATED LINKS</span></span>

[<span data-ttu-id="c25ce-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c25ce-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="c25ce-153">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c25ce-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

