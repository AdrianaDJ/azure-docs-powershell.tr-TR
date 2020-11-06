---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592136"
---
# <span data-ttu-id="f7d71-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="f7d71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d71-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d71-103">Bir yerel dosyayı veya dizini veri Lake Store 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="f7d71-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7d71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7d71-104">SYNTAX</span></span>

### <span data-ttu-id="f7d71-105">NoDiagnosticLogging (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7d71-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d71-106">Includediagnosticlogging</span><span class="sxs-lookup"><span data-stu-id="f7d71-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d71-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7d71-107">DESCRIPTION</span></span>
<span data-ttu-id="f7d71-108">**Import-AzureRmDataLakeStoreItem** cmdlet 'i, bir veri</span><span class="sxs-lookup"><span data-stu-id="f7d71-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="f7d71-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7d71-109">EXAMPLES</span></span>

### <span data-ttu-id="f7d71-110">Örnek 1: dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="f7d71-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="f7d71-111">Bu komut SrcFile.csv dosyayı karşıya yükler ve bunu Data Lake Store 'daki MyFiles klasörüne File.csv</span><span class="sxs-lookup"><span data-stu-id="f7d71-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="f7d71-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7d71-112">PARAMETERS</span></span>

### <span data-ttu-id="f7d71-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f7d71-113">-Account</span></span>
<span data-ttu-id="f7d71-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-115">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="f7d71-115">-Concurrency</span></span>
<span data-ttu-id="f7d71-116">Paralel yüklenecek dosya veya öbeklerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="f7d71-117">Varsayılan, sistem belirtimlerine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="f7d71-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="f7d71-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="f7d71-119">Bir klasörün karşıya yüklenmesi için paralel yüklenecek dosya sayısı üst sınırını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="f7d71-120">Varsayılan olarak, klasör ve dosya boyutu</span><span class="sxs-lookup"><span data-stu-id="f7d71-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d71-121">-DefaultProfile</span></span>
<span data-ttu-id="f7d71-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7d71-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-123">-Hedef</span><span class="sxs-lookup"><span data-stu-id="f7d71-123">-Destination</span></span>
<span data-ttu-id="f7d71-124">Kök dizinden (/) başlayarak dosyanın veya klasörün karşıya yükleneceği Data Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="f7d71-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="f7d71-126">İsteğe bağlı olarak, dosya veya klasör içeri aktarma sırasında olayları kaydetmek için kullanılacak tanı günlüğü düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="f7d71-127">Varsayılan hata.</span><span class="sxs-lookup"><span data-stu-id="f7d71-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="f7d71-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="f7d71-129">Dosya veya klasör içeri aktarma işlemi sırasında olayları kaydetmek için tanı günlüğü yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f7d71-130">-Force</span></span>
<span data-ttu-id="f7d71-131">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="f7d71-132">-ForceBinary</span></span>
<span data-ttu-id="f7d71-133">Kopyalanan dosyaların, ekler arasında yeni satır koruma konusu olmadan kopyalanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="f7d71-134">-Path</span></span>
<span data-ttu-id="f7d71-135">Karşıya yüklenecek dosyanın veya klasörün yerel yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="f7d71-136">-PerFileThreadCount</span></span>
<span data-ttu-id="f7d71-137">Dosya başına kullanılacak en yüksek iş parçacığı sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="f7d71-138">Varsayılan olarak, klasör ve dosya boyutu</span><span class="sxs-lookup"><span data-stu-id="f7d71-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-139">-Recurse</span><span class="sxs-lookup"><span data-stu-id="f7d71-139">-Recurse</span></span>
<span data-ttu-id="f7d71-140">Bu işlemin tüm alt klasörlerdeki tüm öğeleri karşıya yüklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-141">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="f7d71-141">-Resume</span></span>
<span data-ttu-id="f7d71-142">Kopyalanan dosyaların önceki karşıya yükleme işleminin devam ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="f7d71-143">Bu, sistemin tamamen yüklenmemiş son dosyadan devam ettirmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="f7d71-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7d71-144">-Confirm</span></span>
<span data-ttu-id="f7d71-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7d71-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d71-146">-WhatIf</span></span>
<span data-ttu-id="f7d71-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7d71-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d71-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7d71-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d71-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d71-149">CommonParameters</span></span>
<span data-ttu-id="f7d71-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7d71-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d71-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7d71-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d71-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7d71-152">INPUTS</span></span>

### <span data-ttu-id="f7d71-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f7d71-153">None</span></span>
<span data-ttu-id="f7d71-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f7d71-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7d71-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7d71-155">OUTPUTS</span></span>

### <span data-ttu-id="f7d71-156">dizisi</span><span class="sxs-lookup"><span data-stu-id="f7d71-156">string</span></span>
<span data-ttu-id="f7d71-157">Data Lake Store hesabındaki tam yol, karşıya yüklenen dosya veya klasörün tam yoludur.</span><span class="sxs-lookup"><span data-stu-id="f7d71-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="f7d71-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7d71-158">NOTES</span></span>

## <span data-ttu-id="f7d71-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7d71-159">RELATED LINKS</span></span>

[<span data-ttu-id="f7d71-160">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f7d71-161">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f7d71-162">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f7d71-163">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f7d71-164">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f7d71-165">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f7d71-166">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7d71-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


