---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763754"
---
# <span data-ttu-id="bd4a3-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="bd4a3-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="bd4a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4a3-103">Data Lake Store 'daki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd4a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd4a3-104">SYNTAX</span></span>

### <span data-ttu-id="bd4a3-105">Dosya içeriğini önizleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd4a3-105">Preview file content (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd4a3-106">Dosya satırlarını dosyanın noktasından Önizleme</span><span class="sxs-lookup"><span data-stu-id="bd4a3-106">Preview file rows from the head of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd4a3-107">Dosya satırlarından dosya kuyruğunu Önizleme</span><span class="sxs-lookup"><span data-stu-id="bd4a3-107">Preview file rows from the tail of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd4a3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd4a3-108">DESCRIPTION</span></span>
<span data-ttu-id="bd4a3-109">**Get-AzureRmDataLakeStoreItemContent** cmdlet 'ı Data Lake Store 'daki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="bd4a3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd4a3-110">EXAMPLES</span></span>

### <span data-ttu-id="bd4a3-111">Örnek 1: dosyanın içeriğini alma</span><span class="sxs-lookup"><span data-stu-id="bd4a3-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="bd4a3-112">Bu komut, ContosoADL hesabındaki MyFile.txt dosyasının içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="bd4a3-113">Örnek 2: dosyanın ilk iki satırını alma</span><span class="sxs-lookup"><span data-stu-id="bd4a3-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="bd4a3-114">Bu komut, ContosoADL hesabındaki dosya MyFile.txt ilk iki yeni satır ayrılmış satırı alır.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="bd4a3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd4a3-115">PARAMETERS</span></span>

### <span data-ttu-id="bd4a3-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="bd4a3-116">-Account</span></span>
<span data-ttu-id="bd4a3-117">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="bd4a3-118">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="bd4a3-118">-Encoding</span></span>
<span data-ttu-id="bd4a3-119">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-119">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="bd4a3-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bd4a3-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bd4a3-121">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="bd4a3-121">Unknown</span></span>
- <span data-ttu-id="bd4a3-122">Dizisi</span><span class="sxs-lookup"><span data-stu-id="bd4a3-122">String</span></span>
- <span data-ttu-id="bd4a3-123">'Dur</span><span class="sxs-lookup"><span data-stu-id="bd4a3-123">Unicode</span></span>
- <span data-ttu-id="bd4a3-124">Inda</span><span class="sxs-lookup"><span data-stu-id="bd4a3-124">Byte</span></span>
- <span data-ttu-id="bd4a3-125">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="bd4a3-125">BigEndianUnicode</span></span>
- <span data-ttu-id="bd4a3-126">UTF8</span><span class="sxs-lookup"><span data-stu-id="bd4a3-126">UTF8</span></span>
- <span data-ttu-id="bd4a3-127">UTF7</span><span class="sxs-lookup"><span data-stu-id="bd4a3-127">UTF7</span></span>
- <span data-ttu-id="bd4a3-128">ASCII</span><span class="sxs-lookup"><span data-stu-id="bd4a3-128">Ascii</span></span>
- <span data-ttu-id="bd4a3-129">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="bd4a3-129">Default</span></span>
- <span data-ttu-id="bd4a3-130">Doldur</span><span class="sxs-lookup"><span data-stu-id="bd4a3-130">Oem</span></span>
- <span data-ttu-id="bd4a3-131">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="bd4a3-131">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd4a3-132">-Force</span><span class="sxs-lookup"><span data-stu-id="bd4a3-132">-Force</span></span>
<span data-ttu-id="bd4a3-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd4a3-134">Başlı</span><span class="sxs-lookup"><span data-stu-id="bd4a3-134">-Head</span></span>
<span data-ttu-id="bd4a3-135">Dosyanın başlangıcından Önizlenecek satır (yeni satır sınırlı) sayısı.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-135">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="bd4a3-136">Verilerin ilk 4mb bir yeni satır ile karşılaşmıyorsanız, yalnızca bu veriler döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-136">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd4a3-137">Uzunluklu</span><span class="sxs-lookup"><span data-stu-id="bd4a3-137">-Length</span></span>
<span data-ttu-id="bd4a3-138">Alınacak içeriğin bayt cinsinden uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-138">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd4a3-139">-Offset</span><span class="sxs-lookup"><span data-stu-id="bd4a3-139">-Offset</span></span>
<span data-ttu-id="bd4a3-140">İçerik almadan önce dosyada atlanacak bayt sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-140">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd4a3-141">-Yol</span><span class="sxs-lookup"><span data-stu-id="bd4a3-141">-Path</span></span>
<span data-ttu-id="bd4a3-142">Kök dizinden (/) başlayarak bir dosyanın veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-142">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="bd4a3-143">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="bd4a3-143">-Tail</span></span>
<span data-ttu-id="bd4a3-144">Dosyanın sonundan Önizlenecek satır (yeni hat sınırlı) sayısı.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-144">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="bd4a3-145">Verilerin ilk 4mb bir yeni satır ile karşılaşmıyorsanız, yalnızca bu veriler döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-145">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd4a3-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd4a3-146">-Confirm</span></span>
<span data-ttu-id="bd4a3-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd4a3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd4a3-148">-WhatIf</span></span>
<span data-ttu-id="bd4a3-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd4a3-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd4a3-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4a3-151">-DefaultProfile</span></span>
<span data-ttu-id="bd4a3-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd4a3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4a3-153">CommonParameters</span></span>
<span data-ttu-id="bd4a3-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4a3-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd4a3-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4a3-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd4a3-156">INPUTS</span></span>

## <span data-ttu-id="bd4a3-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd4a3-157">OUTPUTS</span></span>

### <span data-ttu-id="bd4a3-158">Byte []</span><span class="sxs-lookup"><span data-stu-id="bd4a3-158">byte[]</span></span>
<span data-ttu-id="bd4a3-159">Alınan dosya içeriğinin bayt akışı temsili.</span><span class="sxs-lookup"><span data-stu-id="bd4a3-159">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="bd4a3-160">dizisi</span><span class="sxs-lookup"><span data-stu-id="bd4a3-160">string</span></span>
<span data-ttu-id="bd4a3-161">Alınan dosya içeriğinin dize temsili (belirtilen kodlamada).</span><span class="sxs-lookup"><span data-stu-id="bd4a3-161">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="bd4a3-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd4a3-162">NOTES</span></span>

## <span data-ttu-id="bd4a3-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd4a3-163">RELATED LINKS</span></span>

