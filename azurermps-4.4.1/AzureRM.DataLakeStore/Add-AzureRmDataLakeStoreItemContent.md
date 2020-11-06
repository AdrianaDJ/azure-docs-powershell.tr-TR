---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 4ce79044793bbecc76d72fab015166ccc3d8fba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587949"
---
# <span data-ttu-id="6a9d1-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6a9d1-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="6a9d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9d1-103">Veri Lake Store 'daki bir öğeye içerik ekler.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a9d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a9d1-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a9d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a9d1-105">DESCRIPTION</span></span>
<span data-ttu-id="6a9d1-106">**Add-AzureRmDataLakeStoreItemContent** cmdlet 'ı bir Azure Data Lake Store 'daki bir öğeye içerik ekler.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="6a9d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a9d1-107">EXAMPLES</span></span>

### <span data-ttu-id="6a9d1-108">Örnek 1: dosyaya içerik ekleme</span><span class="sxs-lookup"><span data-stu-id="6a9d1-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="6a9d1-109">Bu komut myFile.txt dosyaya içerik ekler.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="6a9d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a9d1-110">PARAMETERS</span></span>

### <span data-ttu-id="6a9d1-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="6a9d1-111">-Account</span></span>
<span data-ttu-id="6a9d1-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6a9d1-113">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="6a9d1-113">-Encoding</span></span>
<span data-ttu-id="6a9d1-114">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-114">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="6a9d1-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6a9d1-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a9d1-116">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="6a9d1-116">Unknown</span></span>
- <span data-ttu-id="6a9d1-117">Dizisi</span><span class="sxs-lookup"><span data-stu-id="6a9d1-117">String</span></span>
- <span data-ttu-id="6a9d1-118">'Dur</span><span class="sxs-lookup"><span data-stu-id="6a9d1-118">Unicode</span></span>
- <span data-ttu-id="6a9d1-119">Inda</span><span class="sxs-lookup"><span data-stu-id="6a9d1-119">Byte</span></span>
- <span data-ttu-id="6a9d1-120">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="6a9d1-120">BigEndianUnicode</span></span>
- <span data-ttu-id="6a9d1-121">UTF8</span><span class="sxs-lookup"><span data-stu-id="6a9d1-121">UTF8</span></span>
- <span data-ttu-id="6a9d1-122">UTF7</span><span class="sxs-lookup"><span data-stu-id="6a9d1-122">UTF7</span></span>
- <span data-ttu-id="6a9d1-123">ASCII</span><span class="sxs-lookup"><span data-stu-id="6a9d1-123">Ascii</span></span>
- <span data-ttu-id="6a9d1-124">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="6a9d1-124">Default</span></span>
- <span data-ttu-id="6a9d1-125">Doldur</span><span class="sxs-lookup"><span data-stu-id="6a9d1-125">Oem</span></span>
- <span data-ttu-id="6a9d1-126">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="6a9d1-126">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d1-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="6a9d1-127">-Path</span></span>
<span data-ttu-id="6a9d1-128">Kök dizinle (/) başlayarak değiştirilecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-128">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6a9d1-129">-Değer</span><span class="sxs-lookup"><span data-stu-id="6a9d1-129">-Value</span></span>
<span data-ttu-id="6a9d1-130">Öğeye eklenecek içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-130">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9d1-131">-DefaultProfile</span></span>
<span data-ttu-id="6a9d1-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a9d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9d1-133">CommonParameters</span></span>
<span data-ttu-id="6a9d1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9d1-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9d1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9d1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a9d1-136">INPUTS</span></span>

### <span data-ttu-id="6a9d1-137">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="6a9d1-137">Object</span></span>
<span data-ttu-id="6a9d1-138">' Value ' parametresi ardışık düzenin ' Object ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6a9d1-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="6a9d1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a9d1-139">OUTPUTS</span></span>

### <span data-ttu-id="6a9d1-140">bool</span><span class="sxs-lookup"><span data-stu-id="6a9d1-140">bool</span></span>
<span data-ttu-id="6a9d1-141">Başarı durumunda doğru sonucunu verir.</span><span class="sxs-lookup"><span data-stu-id="6a9d1-141">Returns true on success.</span></span>

## <span data-ttu-id="6a9d1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a9d1-142">NOTES</span></span>

## <span data-ttu-id="6a9d1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a9d1-143">RELATED LINKS</span></span>

[<span data-ttu-id="6a9d1-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6a9d1-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


