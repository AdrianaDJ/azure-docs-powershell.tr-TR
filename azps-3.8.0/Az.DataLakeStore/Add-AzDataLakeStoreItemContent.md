---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095999"
---
# <span data-ttu-id="85b27-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="85b27-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="85b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85b27-102">SYNOPSIS</span></span>
<span data-ttu-id="85b27-103">Veri Lake Store 'daki bir öğeye içerik ekler.</span><span class="sxs-lookup"><span data-stu-id="85b27-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="85b27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85b27-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85b27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85b27-105">DESCRIPTION</span></span>
<span data-ttu-id="85b27-106">**Add-AzDataLakeStoreItemContent** cmdlet 'ı bir Azure Data Lake Store 'daki bir öğeye içerik ekler.</span><span class="sxs-lookup"><span data-stu-id="85b27-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="85b27-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85b27-107">EXAMPLES</span></span>

### <span data-ttu-id="85b27-108">Örnek 1: dosyaya içerik ekleme</span><span class="sxs-lookup"><span data-stu-id="85b27-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="85b27-109">Bu komut myFile.txt dosyaya içerik ekler.</span><span class="sxs-lookup"><span data-stu-id="85b27-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="85b27-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85b27-110">PARAMETERS</span></span>

### <span data-ttu-id="85b27-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="85b27-111">-Account</span></span>
<span data-ttu-id="85b27-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b27-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="85b27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b27-113">-DefaultProfile</span></span>
<span data-ttu-id="85b27-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="85b27-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85b27-115">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="85b27-115">-Encoding</span></span>
<span data-ttu-id="85b27-116">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b27-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="85b27-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="85b27-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85b27-118">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="85b27-118">Unknown</span></span>
- <span data-ttu-id="85b27-119">Dizisi</span><span class="sxs-lookup"><span data-stu-id="85b27-119">String</span></span>
- <span data-ttu-id="85b27-120">'Dur</span><span class="sxs-lookup"><span data-stu-id="85b27-120">Unicode</span></span>
- <span data-ttu-id="85b27-121">Inda</span><span class="sxs-lookup"><span data-stu-id="85b27-121">Byte</span></span>
- <span data-ttu-id="85b27-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="85b27-122">BigEndianUnicode</span></span>
- <span data-ttu-id="85b27-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="85b27-123">UTF8</span></span>
- <span data-ttu-id="85b27-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="85b27-124">UTF7</span></span>
- <span data-ttu-id="85b27-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="85b27-125">Ascii</span></span>
- <span data-ttu-id="85b27-126">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="85b27-126">Default</span></span>
- <span data-ttu-id="85b27-127">Doldur</span><span class="sxs-lookup"><span data-stu-id="85b27-127">Oem</span></span>
- <span data-ttu-id="85b27-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="85b27-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b27-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="85b27-129">-Path</span></span>
<span data-ttu-id="85b27-130">Kök dizinle (/) başlayarak değiştirilecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b27-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="85b27-131">-Değer</span><span class="sxs-lookup"><span data-stu-id="85b27-131">-Value</span></span>
<span data-ttu-id="85b27-132">Öğeye eklenecek içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b27-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="85b27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b27-133">CommonParameters</span></span>
<span data-ttu-id="85b27-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85b27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b27-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b27-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b27-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85b27-136">INPUTS</span></span>

### <span data-ttu-id="85b27-137">System. String</span><span class="sxs-lookup"><span data-stu-id="85b27-137">System.String</span></span>

### <span data-ttu-id="85b27-138">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="85b27-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="85b27-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="85b27-139">System.Object</span></span>

### <span data-ttu-id="85b27-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="85b27-140">System.Text.Encoding</span></span>

## <span data-ttu-id="85b27-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85b27-141">OUTPUTS</span></span>

### <span data-ttu-id="85b27-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85b27-142">System.Boolean</span></span>

## <span data-ttu-id="85b27-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85b27-143">NOTES</span></span>

## <span data-ttu-id="85b27-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85b27-144">RELATED LINKS</span></span>

[<span data-ttu-id="85b27-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="85b27-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


