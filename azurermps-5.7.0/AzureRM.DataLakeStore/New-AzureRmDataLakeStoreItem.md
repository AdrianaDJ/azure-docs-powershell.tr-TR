---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587564"
---
# <span data-ttu-id="1c3fc-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1c3fc-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="1c3fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3fc-103">Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c3fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c3fc-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c3fc-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3fc-106">**New-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1c3fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c3fc-107">EXAMPLES</span></span>

### <span data-ttu-id="1c3fc-108">Örnek 1: yeni bir dosya ve yeni bir klasör oluşturma</span><span class="sxs-lookup"><span data-stu-id="1c3fc-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="1c3fc-109">İlk komut, belirtilen hesap için dosya NewFile.txt oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="1c3fc-110">İkinci komut kök klasörde NewFolder klasörünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="1c3fc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c3fc-111">PARAMETERS</span></span>

### <span data-ttu-id="1c3fc-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="1c3fc-112">-Account</span></span>
<span data-ttu-id="1c3fc-113">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1c3fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3fc-114">-DefaultProfile</span></span>
<span data-ttu-id="1c3fc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c3fc-116">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="1c3fc-116">-Encoding</span></span>
<span data-ttu-id="1c3fc-117">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="1c3fc-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1c3fc-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c3fc-119">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="1c3fc-119">Unknown</span></span>
- <span data-ttu-id="1c3fc-120">Dizisi</span><span class="sxs-lookup"><span data-stu-id="1c3fc-120">String</span></span>
- <span data-ttu-id="1c3fc-121">'Dur</span><span class="sxs-lookup"><span data-stu-id="1c3fc-121">Unicode</span></span>
- <span data-ttu-id="1c3fc-122">Inda</span><span class="sxs-lookup"><span data-stu-id="1c3fc-122">Byte</span></span>
- <span data-ttu-id="1c3fc-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="1c3fc-123">BigEndianUnicode</span></span>
- <span data-ttu-id="1c3fc-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="1c3fc-124">UTF8</span></span>
- <span data-ttu-id="1c3fc-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="1c3fc-125">UTF7</span></span>
- <span data-ttu-id="1c3fc-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="1c3fc-126">Ascii</span></span>
- <span data-ttu-id="1c3fc-127">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="1c3fc-127">Default</span></span>
- <span data-ttu-id="1c3fc-128">Doldur</span><span class="sxs-lookup"><span data-stu-id="1c3fc-128">Oem</span></span>
- <span data-ttu-id="1c3fc-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="1c3fc-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3fc-130">-Klasör</span><span class="sxs-lookup"><span data-stu-id="1c3fc-130">-Folder</span></span>
<span data-ttu-id="1c3fc-131">Bu işlemin bir klasör oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="1c3fc-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1c3fc-132">-Force</span></span>
<span data-ttu-id="1c3fc-133">Zaten varsa, bu işlemin hedef öğenin üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="1c3fc-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="1c3fc-134">-Path</span></span>
<span data-ttu-id="1c3fc-135">Kök dizinle (/) başlayarak oluşturulacak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1c3fc-136">-Değer</span><span class="sxs-lookup"><span data-stu-id="1c3fc-136">-Value</span></span>
<span data-ttu-id="1c3fc-137">Oluşturduğunuz öğeye eklenecek içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3fc-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c3fc-138">-Confirm</span></span>
<span data-ttu-id="1c3fc-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3fc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3fc-140">-WhatIf</span></span>
<span data-ttu-id="1c3fc-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3fc-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3fc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3fc-143">CommonParameters</span></span>
<span data-ttu-id="1c3fc-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3fc-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3fc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3fc-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c3fc-146">INPUTS</span></span>

### <span data-ttu-id="1c3fc-147">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="1c3fc-147">Object</span></span>
<span data-ttu-id="1c3fc-148">' Value ' parametresi ardışık düzenin ' Object ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1c3fc-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="1c3fc-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c3fc-149">OUTPUTS</span></span>

### <span data-ttu-id="1c3fc-150">dizisi</span><span class="sxs-lookup"><span data-stu-id="1c3fc-150">string</span></span>
<span data-ttu-id="1c3fc-151">Oluşturulan dosyanın veya klasörün tam yolu.</span><span class="sxs-lookup"><span data-stu-id="1c3fc-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="1c3fc-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c3fc-152">NOTES</span></span>

## <span data-ttu-id="1c3fc-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c3fc-153">RELATED LINKS</span></span>

[<span data-ttu-id="1c3fc-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1c3fc-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1c3fc-155">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1c3fc-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1c3fc-156">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1c3fc-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1c3fc-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1c3fc-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1c3fc-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1c3fc-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1c3fc-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1c3fc-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


