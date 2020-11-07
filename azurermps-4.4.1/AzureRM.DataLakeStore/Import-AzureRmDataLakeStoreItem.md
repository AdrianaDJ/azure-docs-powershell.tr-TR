---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763745"
---
# <span data-ttu-id="4943e-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="4943e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4943e-102">SYNOPSIS</span></span>
<span data-ttu-id="4943e-103">Bir yerel dosyayı veya dizini veri Lake Store 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="4943e-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4943e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4943e-104">SYNTAX</span></span>

### <span data-ttu-id="4943e-105">Tanılama günlüğü yok (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4943e-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4943e-106">Tanılama günlüğünü içer</span><span class="sxs-lookup"><span data-stu-id="4943e-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4943e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4943e-107">DESCRIPTION</span></span>
<span data-ttu-id="4943e-108">**Import-AzureRmDataLakeStoreItem** cmdlet 'i, bir veri</span><span class="sxs-lookup"><span data-stu-id="4943e-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="4943e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4943e-109">EXAMPLES</span></span>

### <span data-ttu-id="4943e-110">Örnek 1: dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="4943e-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="4943e-111">Bu komut SrcFile.csv dosyayı karşıya yükler ve File.csv olarak Data Lake Store 'daki MyFiles klasörüne ekler.</span><span class="sxs-lookup"><span data-stu-id="4943e-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="4943e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4943e-112">PARAMETERS</span></span>

### <span data-ttu-id="4943e-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4943e-113">-Account</span></span>
<span data-ttu-id="4943e-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="4943e-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="4943e-116">Bir klasörün karşıya yüklenmesi için paralel yüklenecek dosya sayısı üst sınırını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4943e-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="4943e-117">Varsayılan değer 5 ' tir (5).</span><span class="sxs-lookup"><span data-stu-id="4943e-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-118">-Hedef</span><span class="sxs-lookup"><span data-stu-id="4943e-118">-Destination</span></span>
<span data-ttu-id="4943e-119">Kök dizinden (/) başlayarak dosyanın veya klasörün karşıya yükleneceği Data Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="4943e-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="4943e-121">İsteğe bağlı olarak, dosya veya klasör içeri aktarma sırasında olayları kaydetmek için kullanılacak tanı günlüğü düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4943e-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="4943e-122">Varsayılan hata.</span><span class="sxs-lookup"><span data-stu-id="4943e-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="4943e-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="4943e-124">Dosya veya klasör içeri aktarma işlemi sırasında olayları kaydetmek için tanı günlüğü yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4943e-125">-Force</span></span>
<span data-ttu-id="4943e-126">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4943e-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="4943e-127">-ForceBinary</span></span>
<span data-ttu-id="4943e-128">Bu işlemin dosyayı ikili dosya olarak yüklediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-128">Indicates that this operation uploads the file as a binary file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="4943e-129">-Path</span></span>
<span data-ttu-id="4943e-130">Karşıya yüklenecek dosyanın veya klasörün yerel yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-130">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="4943e-131">-PerFileThreadCount</span></span>
<span data-ttu-id="4943e-132">Dosya başına kullanılacak en yüksek iş parçacığı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="4943e-133">Varsayılan değer on (10) değeridir.</span><span class="sxs-lookup"><span data-stu-id="4943e-133">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-134">-Recurse</span><span class="sxs-lookup"><span data-stu-id="4943e-134">-Recurse</span></span>
<span data-ttu-id="4943e-135">Bu işlemin tüm alt klasörlerdeki tüm öğeleri karşıya yüklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-135">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-136">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="4943e-136">-Resume</span></span>
<span data-ttu-id="4943e-137">Bu işlemin önceden iptal edilmiş veya başarısız karşıya yüklemeyi sürdürmek gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4943e-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="4943e-138">-Confirm</span></span>
<span data-ttu-id="4943e-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4943e-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4943e-140">-WhatIf</span></span>
<span data-ttu-id="4943e-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4943e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4943e-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4943e-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4943e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4943e-143">-DefaultProfile</span></span>
<span data-ttu-id="4943e-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4943e-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4943e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4943e-145">CommonParameters</span></span>
<span data-ttu-id="4943e-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4943e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4943e-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4943e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4943e-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4943e-148">INPUTS</span></span>

## <span data-ttu-id="4943e-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4943e-149">OUTPUTS</span></span>

### <span data-ttu-id="4943e-150">dizisi</span><span class="sxs-lookup"><span data-stu-id="4943e-150">string</span></span>
<span data-ttu-id="4943e-151">Data Lake Store hesabındaki tam yol, karşıya yüklenen dosya veya klasörün tam yoludur.</span><span class="sxs-lookup"><span data-stu-id="4943e-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="4943e-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4943e-152">NOTES</span></span>

## <span data-ttu-id="4943e-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4943e-153">RELATED LINKS</span></span>

[<span data-ttu-id="4943e-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4943e-155">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4943e-156">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4943e-157">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4943e-158">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4943e-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4943e-160">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4943e-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


