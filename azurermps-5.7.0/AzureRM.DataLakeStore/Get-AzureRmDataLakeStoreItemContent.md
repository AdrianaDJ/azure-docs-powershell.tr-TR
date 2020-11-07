---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 28e314f5ac7306233c3e2a3619a1a332dd6f3314
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762537"
---
# <span data-ttu-id="f6f2c-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f6f2c-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="f6f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f2c-103">Data Lake Store 'daki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6f2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6f2c-104">SYNTAX</span></span>

### <span data-ttu-id="f6f2c-105">Dosya Içeriğini Önizleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6f2c-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6f2c-106">, Filerowsfromhead</span><span class="sxs-lookup"><span data-stu-id="f6f2c-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6f2c-107">Office.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6f2c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="f6f2c-109">**Get-AzureRmDataLakeStoreItemContent** cmdlet 'ı Data Lake Store 'daki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="f6f2c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6f2c-110">EXAMPLES</span></span>

### <span data-ttu-id="f6f2c-111">Örnek 1: dosyanın içeriğini alma</span><span class="sxs-lookup"><span data-stu-id="f6f2c-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="f6f2c-112">Bu komut, ContosoADL hesabındaki MyFile.txt dosyasının içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="f6f2c-113">Örnek 2: dosyanın ilk iki satırını alma</span><span class="sxs-lookup"><span data-stu-id="f6f2c-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="f6f2c-114">Bu komut, ContosoADL hesabındaki dosya MyFile.txt ilk iki yeni satır ayrılmış satırı alır.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="f6f2c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6f2c-115">PARAMETERS</span></span>

### <span data-ttu-id="f6f2c-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f6f2c-116">-Account</span></span>
<span data-ttu-id="f6f2c-117">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f6f2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f2c-118">-DefaultProfile</span></span>
<span data-ttu-id="f6f2c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f2c-120">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="f6f2c-120">-Encoding</span></span>
<span data-ttu-id="f6f2c-121">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f6f2c-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f6f2c-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6f2c-123">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="f6f2c-123">Unknown</span></span>
- <span data-ttu-id="f6f2c-124">Dizisi</span><span class="sxs-lookup"><span data-stu-id="f6f2c-124">String</span></span>
- <span data-ttu-id="f6f2c-125">'Dur</span><span class="sxs-lookup"><span data-stu-id="f6f2c-125">Unicode</span></span>
- <span data-ttu-id="f6f2c-126">Inda</span><span class="sxs-lookup"><span data-stu-id="f6f2c-126">Byte</span></span>
- <span data-ttu-id="f6f2c-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f6f2c-127">BigEndianUnicode</span></span>
- <span data-ttu-id="f6f2c-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="f6f2c-128">UTF8</span></span>
- <span data-ttu-id="f6f2c-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="f6f2c-129">UTF7</span></span>
- <span data-ttu-id="f6f2c-130">ASCII</span><span class="sxs-lookup"><span data-stu-id="f6f2c-130">Ascii</span></span>
- <span data-ttu-id="f6f2c-131">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="f6f2c-131">Default</span></span>
- <span data-ttu-id="f6f2c-132">Doldur</span><span class="sxs-lookup"><span data-stu-id="f6f2c-132">Oem</span></span>
- <span data-ttu-id="f6f2c-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f6f2c-133">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f6f2c-134">-Force</span></span>
<span data-ttu-id="f6f2c-135">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2c-136">Başlı</span><span class="sxs-lookup"><span data-stu-id="f6f2c-136">-Head</span></span>
<span data-ttu-id="f6f2c-137">Dosyanın başlangıcından Önizlenecek satır (yeni satır sınırlı) sayısı.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="f6f2c-138">Verilerin ilk 4mb bir yeni satır ile karşılaşmıyorsanız, yalnızca bu veriler döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2c-139">Uzunluklu</span><span class="sxs-lookup"><span data-stu-id="f6f2c-139">-Length</span></span>
<span data-ttu-id="f6f2c-140">Alınacak içeriğin bayt cinsinden uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2c-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="f6f2c-141">-Offset</span></span>
<span data-ttu-id="f6f2c-142">İçerik almadan önce dosyada atlanacak bayt sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2c-143">-Yol</span><span class="sxs-lookup"><span data-stu-id="f6f2c-143">-Path</span></span>
<span data-ttu-id="f6f2c-144">Kök dizinden (/) başlayarak bir dosyanın veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f6f2c-145">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="f6f2c-145">-Tail</span></span>
<span data-ttu-id="f6f2c-146">Dosyanın sonundan Önizlenecek satır (yeni hat sınırlı) sayısı.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="f6f2c-147">Verilerin ilk 4mb bir yeni satır ile karşılaşmıyorsanız, yalnızca bu veriler döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2c-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6f2c-148">-Confirm</span></span>
<span data-ttu-id="f6f2c-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f2c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f2c-150">-WhatIf</span></span>
<span data-ttu-id="f6f2c-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6f2c-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f2c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f2c-153">CommonParameters</span></span>
<span data-ttu-id="f6f2c-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f2c-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f2c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f2c-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6f2c-156">INPUTS</span></span>

### <span data-ttu-id="f6f2c-157">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f6f2c-157">None</span></span>
<span data-ttu-id="f6f2c-158">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6f2c-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6f2c-159">OUTPUTS</span></span>

### <span data-ttu-id="f6f2c-160">Byte []</span><span class="sxs-lookup"><span data-stu-id="f6f2c-160">byte[]</span></span>
<span data-ttu-id="f6f2c-161">Alınan dosya içeriğinin bayt akışı temsili.</span><span class="sxs-lookup"><span data-stu-id="f6f2c-161">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="f6f2c-162">dizisi</span><span class="sxs-lookup"><span data-stu-id="f6f2c-162">string</span></span>
<span data-ttu-id="f6f2c-163">Alınan dosya içeriğinin dize temsili (belirtilen kodlamada).</span><span class="sxs-lookup"><span data-stu-id="f6f2c-163">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="f6f2c-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6f2c-164">NOTES</span></span>

## <span data-ttu-id="f6f2c-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6f2c-165">RELATED LINKS</span></span>

