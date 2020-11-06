---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 91e7969600f387a95f46cad02f87cf6466f2c642
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588483"
---
# <span data-ttu-id="2dc1c-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="2dc1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc1c-103">Bir yerel dosyayı veya dizini veri Lake Store 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dc1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2dc1c-104">SYNTAX</span></span>

### <span data-ttu-id="2dc1c-105">NoDiagnosticLogging (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2dc1c-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dc1c-106">Includediagnosticlogging</span><span class="sxs-lookup"><span data-stu-id="2dc1c-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dc1c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2dc1c-107">DESCRIPTION</span></span>
<span data-ttu-id="2dc1c-108">**Import-AzureRmDataLakeStoreItem** cmdlet 'i, bir veri</span><span class="sxs-lookup"><span data-stu-id="2dc1c-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="2dc1c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2dc1c-109">EXAMPLES</span></span>

### <span data-ttu-id="2dc1c-110">Örnek 1: dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="2dc1c-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="2dc1c-111">Bu komut SrcFile.csv dosyayı karşıya yükler ve bunu Data Lake Store 'daki MyFiles klasörüne File.csv</span><span class="sxs-lookup"><span data-stu-id="2dc1c-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="2dc1c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2dc1c-112">PARAMETERS</span></span>

### <span data-ttu-id="2dc1c-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2dc1c-113">-Account</span></span>
<span data-ttu-id="2dc1c-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2dc1c-115">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="2dc1c-115">-Concurrency</span></span>
<span data-ttu-id="2dc1c-116">Paralel yüklenecek dosya veya öbeklerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="2dc1c-117">Varsayılan, sistem belirtimlerine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="2dc1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc1c-118">-DefaultProfile</span></span>
<span data-ttu-id="2dc1c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dc1c-120">-Hedef</span><span class="sxs-lookup"><span data-stu-id="2dc1c-120">-Destination</span></span>
<span data-ttu-id="2dc1c-121">Kök dizinden (/) başlayarak dosyanın veya klasörün karşıya yükleneceği Data Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2dc1c-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="2dc1c-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="2dc1c-123">İsteğe bağlı olarak, dosya veya klasör içeri aktarma sırasında olayları kaydetmek için kullanılacak tanı günlüğü düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="2dc1c-124">Varsayılan hata.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-124">Default is Error.</span></span>

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

### <span data-ttu-id="2dc1c-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="2dc1c-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="2dc1c-126">Dosya veya klasör içeri aktarma işlemi sırasında olayları kaydetmek için tanı günlüğü yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="2dc1c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2dc1c-127">-Force</span></span>
<span data-ttu-id="2dc1c-128">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="2dc1c-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="2dc1c-129">-ForceBinary</span></span>
<span data-ttu-id="2dc1c-130">Kopyalanan dosyaların, ekler arasında yeni satır koruma konusu olmadan kopyalanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="2dc1c-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="2dc1c-131">-Path</span></span>
<span data-ttu-id="2dc1c-132">Karşıya yüklenecek dosyanın veya klasörün yerel yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="2dc1c-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="2dc1c-133">-Recurse</span></span>
<span data-ttu-id="2dc1c-134">Bu işlemin tüm alt klasörlerdeki tüm öğeleri karşıya yüklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="2dc1c-135">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="2dc1c-135">-Resume</span></span>
<span data-ttu-id="2dc1c-136">Kopyalanan dosyaların önceki karşıya yükleme işleminin devam ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="2dc1c-137">Bu, sistemin tamamen yüklenmemiş son dosyadan devam ettirmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="2dc1c-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="2dc1c-138">-Confirm</span></span>
<span data-ttu-id="2dc1c-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc1c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc1c-140">-WhatIf</span></span>
<span data-ttu-id="2dc1c-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dc1c-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc1c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc1c-143">CommonParameters</span></span>
<span data-ttu-id="2dc1c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc1c-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc1c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc1c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2dc1c-146">INPUTS</span></span>

### <span data-ttu-id="2dc1c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc1c-147">System.String</span></span>

### <span data-ttu-id="2dc1c-148">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2dc1c-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2dc1c-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2dc1c-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2dc1c-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2dc1c-150">System.Int32</span></span>

### <span data-ttu-id="2dc1c-151">Microsoft. Azure. Commands. DataLakeStore. modeller. LogLevel</span><span class="sxs-lookup"><span data-stu-id="2dc1c-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="2dc1c-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2dc1c-152">OUTPUTS</span></span>

### <span data-ttu-id="2dc1c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc1c-153">System.String</span></span>
<span data-ttu-id="2dc1c-154">Data Lake Store hesabındaki tam yol, karşıya yüklenen dosya veya klasörün tam yoludur.</span><span class="sxs-lookup"><span data-stu-id="2dc1c-154">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="2dc1c-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2dc1c-155">NOTES</span></span>

## <span data-ttu-id="2dc1c-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2dc1c-156">RELATED LINKS</span></span>

[<span data-ttu-id="2dc1c-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2dc1c-158">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2dc1c-159">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-159">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2dc1c-160">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-160">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2dc1c-161">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-161">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2dc1c-162">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-162">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2dc1c-163">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2dc1c-163">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


