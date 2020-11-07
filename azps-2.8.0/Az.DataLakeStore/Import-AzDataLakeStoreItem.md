---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ccb538446e7cb179e15f3af17d0cde03c4ab44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752317"
---
# <span data-ttu-id="87a0f-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="87a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="87a0f-103">Bir yerel dosyayı veya dizini veri Lake Store 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="87a0f-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="87a0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87a0f-104">SYNTAX</span></span>

### <span data-ttu-id="87a0f-105">NoDiagnosticLogging (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87a0f-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87a0f-106">Includediagnosticlogging</span><span class="sxs-lookup"><span data-stu-id="87a0f-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87a0f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="87a0f-107">DESCRIPTION</span></span>
<span data-ttu-id="87a0f-108">**Import-AzDataLakeStoreItem** cmdlet 'i, bir veri</span><span class="sxs-lookup"><span data-stu-id="87a0f-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="87a0f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87a0f-109">EXAMPLES</span></span>

### <span data-ttu-id="87a0f-110">Örnek 1: dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="87a0f-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="87a0f-111">Bu komut SrcFile.csv dosyayı karşıya yükler ve bunu Data Lake Store 'daki MyFiles klasörüne File.csv</span><span class="sxs-lookup"><span data-stu-id="87a0f-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="87a0f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87a0f-112">PARAMETERS</span></span>

### <span data-ttu-id="87a0f-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="87a0f-113">-Account</span></span>
<span data-ttu-id="87a0f-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="87a0f-115">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="87a0f-115">-Concurrency</span></span>
<span data-ttu-id="87a0f-116">Paralel yüklenecek dosya veya öbeklerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="87a0f-117">Varsayılan, sistem belirtimlerine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="87a0f-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a0f-118">-DefaultProfile</span></span>
<span data-ttu-id="87a0f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87a0f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a0f-120">-Hedef</span><span class="sxs-lookup"><span data-stu-id="87a0f-120">-Destination</span></span>
<span data-ttu-id="87a0f-121">Kök dizinden (/) başlayarak dosyanın veya klasörün karşıya yükleneceği Data Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="87a0f-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="87a0f-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="87a0f-123">İsteğe bağlı olarak, dosya veya klasör içeri aktarma sırasında olayları kaydetmek için kullanılacak tanı günlüğü düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="87a0f-124">Varsayılan hata.</span><span class="sxs-lookup"><span data-stu-id="87a0f-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a0f-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="87a0f-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="87a0f-126">Dosya veya klasör içeri aktarma işlemi sırasında olayları kaydetmek için tanı günlüğü yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a0f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="87a0f-127">-Force</span></span>
<span data-ttu-id="87a0f-128">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="87a0f-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="87a0f-129">-ForceBinary</span></span>
<span data-ttu-id="87a0f-130">Kopyalanan dosyaların, ekler arasında yeni satır koruma konusu olmadan kopyalanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="87a0f-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="87a0f-131">-Path</span></span>
<span data-ttu-id="87a0f-132">Karşıya yüklenecek dosyanın veya klasörün yerel yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="87a0f-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="87a0f-133">-Recurse</span></span>
<span data-ttu-id="87a0f-134">Bu işlemin tüm alt klasörlerdeki tüm öğeleri karşıya yüklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="87a0f-135">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="87a0f-135">-Resume</span></span>
<span data-ttu-id="87a0f-136">Kopyalanan dosyaların önceki karşıya yükleme işleminin devam ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="87a0f-137">Bu, sistemin tamamen yüklenmemiş son dosyadan devam ettirmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="87a0f-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="87a0f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="87a0f-138">-Confirm</span></span>
<span data-ttu-id="87a0f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87a0f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a0f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a0f-140">-WhatIf</span></span>
<span data-ttu-id="87a0f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87a0f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a0f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87a0f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a0f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a0f-143">CommonParameters</span></span>
<span data-ttu-id="87a0f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87a0f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a0f-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a0f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a0f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87a0f-146">INPUTS</span></span>

### <span data-ttu-id="87a0f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="87a0f-147">System.String</span></span>

### <span data-ttu-id="87a0f-148">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="87a0f-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="87a0f-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87a0f-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="87a0f-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="87a0f-150">System.Int32</span></span>

### <span data-ttu-id="87a0f-151">Microsoft. Azure. Commands. DataLakeStore. modeller. LogLevel</span><span class="sxs-lookup"><span data-stu-id="87a0f-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="87a0f-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87a0f-152">OUTPUTS</span></span>

### <span data-ttu-id="87a0f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="87a0f-153">System.String</span></span>

## <span data-ttu-id="87a0f-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87a0f-154">NOTES</span></span>

## <span data-ttu-id="87a0f-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87a0f-155">RELATED LINKS</span></span>

[<span data-ttu-id="87a0f-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="87a0f-157">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="87a0f-158">Katıl-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="87a0f-159">Taşı-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="87a0f-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="87a0f-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="87a0f-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87a0f-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


