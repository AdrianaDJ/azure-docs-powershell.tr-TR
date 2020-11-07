---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f7b23188f0ba56a62f2442626f406b134ccd48e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761076"
---
# <span data-ttu-id="87415-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="87415-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87415-102">SYNOPSIS</span></span>
<span data-ttu-id="87415-103">Data Lake Store 'dan bir dosya indirir.</span><span class="sxs-lookup"><span data-stu-id="87415-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="87415-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87415-104">SYNTAX</span></span>

### <span data-ttu-id="87415-105">NoDiagnosticLogging (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87415-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87415-106">Includediagnosticlogging</span><span class="sxs-lookup"><span data-stu-id="87415-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87415-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="87415-107">DESCRIPTION</span></span>
<span data-ttu-id="87415-108">**Export-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'dan bir dosyayı indirir.</span><span class="sxs-lookup"><span data-stu-id="87415-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="87415-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87415-109">EXAMPLES</span></span>

### <span data-ttu-id="87415-110">Örnek 1: Data Lake Store 'dan bir öğe Indirin</span><span class="sxs-lookup"><span data-stu-id="87415-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="87415-111">Bu komut, Data Lake Store 'dan TestSource.csv dosya C:\Test.csv</span><span class="sxs-lookup"><span data-stu-id="87415-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="87415-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87415-112">PARAMETERS</span></span>

### <span data-ttu-id="87415-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="87415-113">-Account</span></span>
<span data-ttu-id="87415-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87415-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="87415-115">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="87415-115">-Concurrency</span></span>
<span data-ttu-id="87415-116">Paralel olarak indirilecek dosya veya öbeklerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87415-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="87415-117">Varsayılan, sistem belirtimlerine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="87415-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="87415-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87415-118">-DefaultProfile</span></span>
<span data-ttu-id="87415-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87415-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87415-120">-Hedef</span><span class="sxs-lookup"><span data-stu-id="87415-120">-Destination</span></span>
<span data-ttu-id="87415-121">Dosyanın indirileceği yerel dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87415-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87415-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="87415-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="87415-123">İsteğe bağlı olarak, dosya veya klasör içeri aktarma sırasında olayları kaydetmek için kullanılacak tanı günlüğü düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87415-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="87415-124">Varsayılan hata.</span><span class="sxs-lookup"><span data-stu-id="87415-124">Default is Error.</span></span>

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

### <span data-ttu-id="87415-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="87415-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="87415-126">Dosya veya klasör içeri aktarma işlemi sırasında olayları kaydetmek için tanı günlüğü yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87415-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="87415-127">-Force</span><span class="sxs-lookup"><span data-stu-id="87415-127">-Force</span></span>
<span data-ttu-id="87415-128">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="87415-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87415-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="87415-129">-Path</span></span>
<span data-ttu-id="87415-130">Kök dizinden (/) başlayarak Data Lake Store 'dan indirilecek öğenin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87415-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87415-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="87415-131">-Recurse</span></span>
<span data-ttu-id="87415-132">Bir klasör indirmesinin özyinelemeli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="87415-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="87415-133">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="87415-133">-Resume</span></span>
<span data-ttu-id="87415-134">Kopyalanan dosyaların, önceki indirmede devam ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87415-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="87415-135">Bu, sistemin tam olarak indirilmemiş olan son dosyadan devam ettirmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="87415-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="87415-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="87415-136">-Confirm</span></span>
<span data-ttu-id="87415-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87415-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87415-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87415-138">-WhatIf</span></span>
<span data-ttu-id="87415-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87415-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87415-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87415-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87415-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87415-141">CommonParameters</span></span>
<span data-ttu-id="87415-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87415-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87415-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87415-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87415-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87415-144">INPUTS</span></span>

### <span data-ttu-id="87415-145">System. String</span><span class="sxs-lookup"><span data-stu-id="87415-145">System.String</span></span>

### <span data-ttu-id="87415-146">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="87415-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="87415-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87415-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="87415-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="87415-148">System.Int32</span></span>

### <span data-ttu-id="87415-149">Microsoft. Azure. Commands. DataLakeStore. modeller. LogLevel</span><span class="sxs-lookup"><span data-stu-id="87415-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="87415-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87415-150">OUTPUTS</span></span>

### <span data-ttu-id="87415-151">System. String</span><span class="sxs-lookup"><span data-stu-id="87415-151">System.String</span></span>

## <span data-ttu-id="87415-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87415-152">NOTES</span></span>

## <span data-ttu-id="87415-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87415-153">RELATED LINKS</span></span>

[<span data-ttu-id="87415-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="87415-155">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="87415-156">Katıl-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="87415-157">Taşı-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="87415-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="87415-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="87415-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87415-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


