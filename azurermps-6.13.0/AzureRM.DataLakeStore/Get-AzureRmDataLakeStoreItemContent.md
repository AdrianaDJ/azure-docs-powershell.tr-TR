---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 7a757ca4b310176a71a7b2fe7e5c301137998ff9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593678"
---
# <span data-ttu-id="c7dee-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="c7dee-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="c7dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7dee-102">SYNOPSIS</span></span>
<span data-ttu-id="c7dee-103">Data Lake Store 'daki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="c7dee-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7dee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7dee-104">SYNTAX</span></span>

### <span data-ttu-id="c7dee-105">Dosya Içeriğini Önizleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7dee-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7dee-106">, Filerowsfromhead</span><span class="sxs-lookup"><span data-stu-id="c7dee-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7dee-107">Office.</span><span class="sxs-lookup"><span data-stu-id="c7dee-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7dee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7dee-108">DESCRIPTION</span></span>
<span data-ttu-id="c7dee-109">**Get-AzureRmDataLakeStoreItemContent** cmdlet 'ı Data Lake Store 'daki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="c7dee-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="c7dee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7dee-110">EXAMPLES</span></span>

### <span data-ttu-id="c7dee-111">Örnek 1: dosyanın içeriğini alma</span><span class="sxs-lookup"><span data-stu-id="c7dee-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="c7dee-112">Bu komut, ContosoADL hesabındaki MyFile.txt dosyasının içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="c7dee-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="c7dee-113">Örnek 2: dosyanın ilk iki satırını alma</span><span class="sxs-lookup"><span data-stu-id="c7dee-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="c7dee-114">Bu komut, ContosoADL hesabındaki dosya MyFile.txt ilk iki yeni satır ayrılmış satırı alır.</span><span class="sxs-lookup"><span data-stu-id="c7dee-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="c7dee-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7dee-115">PARAMETERS</span></span>

### <span data-ttu-id="c7dee-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="c7dee-116">-Account</span></span>
<span data-ttu-id="c7dee-117">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7dee-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c7dee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7dee-118">-DefaultProfile</span></span>
<span data-ttu-id="c7dee-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7dee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7dee-120">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="c7dee-120">-Encoding</span></span>
<span data-ttu-id="c7dee-121">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7dee-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="c7dee-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c7dee-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c7dee-123">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="c7dee-123">Unknown</span></span>
- <span data-ttu-id="c7dee-124">Dizisi</span><span class="sxs-lookup"><span data-stu-id="c7dee-124">String</span></span>
- <span data-ttu-id="c7dee-125">'Dur</span><span class="sxs-lookup"><span data-stu-id="c7dee-125">Unicode</span></span>
- <span data-ttu-id="c7dee-126">Inda</span><span class="sxs-lookup"><span data-stu-id="c7dee-126">Byte</span></span>
- <span data-ttu-id="c7dee-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="c7dee-127">BigEndianUnicode</span></span>
- <span data-ttu-id="c7dee-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="c7dee-128">UTF8</span></span>
- <span data-ttu-id="c7dee-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="c7dee-129">UTF7</span></span>
- <span data-ttu-id="c7dee-130">ASCII</span><span class="sxs-lookup"><span data-stu-id="c7dee-130">Ascii</span></span>
- <span data-ttu-id="c7dee-131">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="c7dee-131">Default</span></span>
- <span data-ttu-id="c7dee-132">Doldur</span><span class="sxs-lookup"><span data-stu-id="c7dee-132">Oem</span></span>
- <span data-ttu-id="c7dee-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="c7dee-133">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dee-134">-Force</span><span class="sxs-lookup"><span data-stu-id="c7dee-134">-Force</span></span>
<span data-ttu-id="c7dee-135">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c7dee-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dee-136">Başlı</span><span class="sxs-lookup"><span data-stu-id="c7dee-136">-Head</span></span>
<span data-ttu-id="c7dee-137">Dosyanın başlangıcından Önizlenecek satır (yeni satır sınırlı) sayısı.</span><span class="sxs-lookup"><span data-stu-id="c7dee-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="c7dee-138">Verilerin ilk 4mb bir yeni satır ile karşılaşmıyorsanız, yalnızca bu veriler döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="c7dee-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dee-139">Uzunluklu</span><span class="sxs-lookup"><span data-stu-id="c7dee-139">-Length</span></span>
<span data-ttu-id="c7dee-140">Alınacak içeriğin bayt cinsinden uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7dee-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dee-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="c7dee-141">-Offset</span></span>
<span data-ttu-id="c7dee-142">İçerik almadan önce dosyada atlanacak bayt sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7dee-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dee-143">-Yol</span><span class="sxs-lookup"><span data-stu-id="c7dee-143">-Path</span></span>
<span data-ttu-id="c7dee-144">Kök dizinden (/) başlayarak bir dosyanın veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7dee-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c7dee-145">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="c7dee-145">-Tail</span></span>
<span data-ttu-id="c7dee-146">Dosyanın sonundan Önizlenecek satır (yeni hat sınırlı) sayısı.</span><span class="sxs-lookup"><span data-stu-id="c7dee-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="c7dee-147">Verilerin ilk 4mb bir yeni satır ile karşılaşmıyorsanız, yalnızca bu veriler döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="c7dee-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7dee-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7dee-148">-Confirm</span></span>
<span data-ttu-id="c7dee-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7dee-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7dee-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7dee-150">-WhatIf</span></span>
<span data-ttu-id="c7dee-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7dee-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7dee-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7dee-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7dee-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7dee-153">CommonParameters</span></span>
<span data-ttu-id="c7dee-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7dee-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7dee-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7dee-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7dee-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7dee-156">INPUTS</span></span>

### <span data-ttu-id="c7dee-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c7dee-157">System.String</span></span>

### <span data-ttu-id="c7dee-158">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c7dee-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c7dee-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c7dee-159">System.Int32</span></span>

### <span data-ttu-id="c7dee-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="c7dee-160">System.Int64</span></span>

### <span data-ttu-id="c7dee-161">Microsoft. Azure. Commands. DataLakeStore. modeller. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="c7dee-161">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="c7dee-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7dee-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7dee-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7dee-163">OUTPUTS</span></span>

### <span data-ttu-id="c7dee-164">System. Byte</span><span class="sxs-lookup"><span data-stu-id="c7dee-164">System.Byte</span></span>
<span data-ttu-id="c7dee-165">Alınan dosya içeriğinin bayt akışı temsili.</span><span class="sxs-lookup"><span data-stu-id="c7dee-165">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="c7dee-166">System. String</span><span class="sxs-lookup"><span data-stu-id="c7dee-166">System.String</span></span>
<span data-ttu-id="c7dee-167">Alınan dosya içeriğinin dize temsili (belirtilen kodlamada).</span><span class="sxs-lookup"><span data-stu-id="c7dee-167">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="c7dee-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7dee-168">NOTES</span></span>

## <span data-ttu-id="c7dee-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7dee-169">RELATED LINKS</span></span>
