---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762374"
---
# <span data-ttu-id="08306-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="08306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08306-102">SYNOPSIS</span></span>
<span data-ttu-id="08306-103">Data Lake Store 'dan bir dosya indirir.</span><span class="sxs-lookup"><span data-stu-id="08306-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08306-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08306-104">SYNTAX</span></span>

### <span data-ttu-id="08306-105">NoDiagnosticLogging (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="08306-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08306-106">Includediagnosticlogging</span><span class="sxs-lookup"><span data-stu-id="08306-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08306-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="08306-107">DESCRIPTION</span></span>
<span data-ttu-id="08306-108">**Export-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'dan bir dosyayı indirir.</span><span class="sxs-lookup"><span data-stu-id="08306-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="08306-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08306-109">EXAMPLES</span></span>

### <span data-ttu-id="08306-110">Örnek 1: Data Lake Store 'dan bir öğe Indirin</span><span class="sxs-lookup"><span data-stu-id="08306-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="08306-111">Bu komut, Data Lake Store 'dan TestSource.csv dosya C:\Test.csv</span><span class="sxs-lookup"><span data-stu-id="08306-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="08306-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08306-112">PARAMETERS</span></span>

### <span data-ttu-id="08306-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="08306-113">-Account</span></span>
<span data-ttu-id="08306-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08306-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="08306-115">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="08306-115">-Concurrency</span></span>
<span data-ttu-id="08306-116">Paralel olarak indirilecek dosya veya öbeklerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08306-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="08306-117">Varsayılan, sistem belirtimlerine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="08306-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08306-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="08306-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="08306-119">Bir klasör indirmesi için paralel olarak indirilecek en fazla dosya sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08306-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="08306-120">Varsayılan olarak, klasör ve dosya boyutu</span><span class="sxs-lookup"><span data-stu-id="08306-120">Default will be computed as a best effort based on folder and file size</span></span>

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

### <span data-ttu-id="08306-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08306-121">-DefaultProfile</span></span>
<span data-ttu-id="08306-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08306-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08306-123">-Hedef</span><span class="sxs-lookup"><span data-stu-id="08306-123">-Destination</span></span>
<span data-ttu-id="08306-124">Dosyanın indirileceği yerel dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="08306-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08306-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="08306-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="08306-126">İsteğe bağlı olarak, dosya veya klasör içeri aktarma sırasında olayları kaydetmek için kullanılacak tanı günlüğü düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="08306-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="08306-127">Varsayılan hata.</span><span class="sxs-lookup"><span data-stu-id="08306-127">Default is Error.</span></span>

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

### <span data-ttu-id="08306-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="08306-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="08306-129">Dosya veya klasör içeri aktarma işlemi sırasında olayları kaydetmek için tanı günlüğü yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="08306-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="08306-130">-Force</span><span class="sxs-lookup"><span data-stu-id="08306-130">-Force</span></span>
<span data-ttu-id="08306-131">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="08306-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08306-132">-Yol</span><span class="sxs-lookup"><span data-stu-id="08306-132">-Path</span></span>
<span data-ttu-id="08306-133">Kök dizinden (/) başlayarak Data Lake Store 'dan indirilecek öğenin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="08306-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08306-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="08306-134">-PerFileThreadCount</span></span>
<span data-ttu-id="08306-135">Dosya başına kullanılacak en yüksek iş parçacığı sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08306-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="08306-136">Varsayılan olarak, klasör ve dosya boyutu</span><span class="sxs-lookup"><span data-stu-id="08306-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08306-137">-Recurse</span><span class="sxs-lookup"><span data-stu-id="08306-137">-Recurse</span></span>
<span data-ttu-id="08306-138">Bir klasör indirmesinin özyinelemeli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="08306-138">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="08306-139">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="08306-139">-Resume</span></span>
<span data-ttu-id="08306-140">Kopyalanan dosyaların, önceki indirmede devam ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="08306-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="08306-141">Bu, sistemin tam olarak indirilmemiş olan son dosyadan devam ettirmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="08306-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="08306-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="08306-142">-Confirm</span></span>
<span data-ttu-id="08306-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08306-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08306-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08306-144">-WhatIf</span></span>
<span data-ttu-id="08306-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08306-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08306-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08306-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08306-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08306-147">CommonParameters</span></span>
<span data-ttu-id="08306-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08306-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08306-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08306-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08306-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08306-150">INPUTS</span></span>

### <span data-ttu-id="08306-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="08306-151">None</span></span>
<span data-ttu-id="08306-152">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="08306-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08306-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08306-153">OUTPUTS</span></span>

### <span data-ttu-id="08306-154">dizisi</span><span class="sxs-lookup"><span data-stu-id="08306-154">string</span></span>
<span data-ttu-id="08306-155">Dosya veya klasörün indirildiği yol.</span><span class="sxs-lookup"><span data-stu-id="08306-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="08306-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08306-156">NOTES</span></span>

## <span data-ttu-id="08306-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08306-157">RELATED LINKS</span></span>

[<span data-ttu-id="08306-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="08306-159">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="08306-160">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="08306-161">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="08306-162">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="08306-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="08306-164">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="08306-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


