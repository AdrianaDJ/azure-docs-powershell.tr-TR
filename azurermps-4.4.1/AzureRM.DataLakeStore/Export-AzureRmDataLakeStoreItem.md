---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593153"
---
# <span data-ttu-id="4bd32-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="4bd32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bd32-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd32-103">Data Lake Store 'dan bir dosya indirir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bd32-104">SYNTAX</span></span>

### <span data-ttu-id="4bd32-105">Tanılama günlüğü yok (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bd32-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bd32-106">Tanılama günlüğünü içer</span><span class="sxs-lookup"><span data-stu-id="4bd32-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bd32-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd32-108">**Export-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'dan bir dosyayı indirir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="4bd32-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bd32-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd32-110">Örnek 1: Data Lake Store 'dan bir öğe Indirin</span><span class="sxs-lookup"><span data-stu-id="4bd32-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="4bd32-111">Bu komut, TestSource.csv C:\Test.csv veri</span><span class="sxs-lookup"><span data-stu-id="4bd32-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="4bd32-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bd32-112">PARAMETERS</span></span>

### <span data-ttu-id="4bd32-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4bd32-113">-Account</span></span>
<span data-ttu-id="4bd32-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4bd32-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="4bd32-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="4bd32-116">Bir klasör indirmesi için paralel olarak indirilecek en fazla dosya sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="4bd32-117">Varsayılan değer 5 ' tir (5).</span><span class="sxs-lookup"><span data-stu-id="4bd32-117">The default value is five (5).</span></span>

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

### <span data-ttu-id="4bd32-118">-Hedef</span><span class="sxs-lookup"><span data-stu-id="4bd32-118">-Destination</span></span>
<span data-ttu-id="4bd32-119">Dosyanın indirileceği yerel dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="4bd32-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="4bd32-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="4bd32-121">İsteğe bağlı olarak, dosya veya klasör içeri aktarma sırasında olayları kaydetmek için kullanılacak tanı günlüğü düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="4bd32-122">Varsayılan hata.</span><span class="sxs-lookup"><span data-stu-id="4bd32-122">Default is Error.</span></span>

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

### <span data-ttu-id="4bd32-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="4bd32-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="4bd32-124">Dosya veya klasör içeri aktarma işlemi sırasında olayları kaydetmek için tanı günlüğü yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="4bd32-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4bd32-125">-Force</span></span>
<span data-ttu-id="4bd32-126">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="4bd32-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="4bd32-127">-Path</span></span>
<span data-ttu-id="4bd32-128">Kök dizinden (/) başlayarak Data Lake Store 'dan indirilecek öğenin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="4bd32-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="4bd32-129">-PerFileThreadCount</span></span>
<span data-ttu-id="4bd32-130">Dosya başına kullanılacak en yüksek iş parçacığı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="4bd32-131">Varsayılan değer on (10) değeridir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd32-132">-Recurse</span><span class="sxs-lookup"><span data-stu-id="4bd32-132">-Recurse</span></span>
<span data-ttu-id="4bd32-133">Bir klasör indirmesinin özyinelemeli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="4bd32-134">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="4bd32-134">-Resume</span></span>
<span data-ttu-id="4bd32-135">Kopyalanan dosya veya dosyaların önceki indirmede bir devam olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="4bd32-136">İndirme, tam olarak indirilmemiş olan son dosyadan devam etmeyi dener.</span><span class="sxs-lookup"><span data-stu-id="4bd32-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="4bd32-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bd32-137">-Confirm</span></span>
<span data-ttu-id="4bd32-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bd32-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bd32-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd32-139">-WhatIf</span></span>
<span data-ttu-id="4bd32-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bd32-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bd32-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bd32-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bd32-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd32-142">-DefaultProfile</span></span>
<span data-ttu-id="4bd32-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bd32-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd32-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd32-144">CommonParameters</span></span>
<span data-ttu-id="4bd32-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bd32-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd32-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd32-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd32-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bd32-147">INPUTS</span></span>

## <span data-ttu-id="4bd32-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bd32-148">OUTPUTS</span></span>

### <span data-ttu-id="4bd32-149">dizisi</span><span class="sxs-lookup"><span data-stu-id="4bd32-149">string</span></span>
<span data-ttu-id="4bd32-150">Dosya veya klasörün indirildiği yol.</span><span class="sxs-lookup"><span data-stu-id="4bd32-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="4bd32-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bd32-151">NOTES</span></span>

## <span data-ttu-id="4bd32-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bd32-152">RELATED LINKS</span></span>

[<span data-ttu-id="4bd32-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4bd32-154">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4bd32-155">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4bd32-156">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4bd32-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4bd32-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4bd32-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bd32-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


