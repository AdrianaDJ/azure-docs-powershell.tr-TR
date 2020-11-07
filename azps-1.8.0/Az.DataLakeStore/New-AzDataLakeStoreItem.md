---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 222df24f2d3db296ce116e49da8baeb3e22ec699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916864"
---
# <span data-ttu-id="ad932-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ad932-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="ad932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad932-102">SYNOPSIS</span></span>
<span data-ttu-id="ad932-103">Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad932-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ad932-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad932-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad932-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad932-105">DESCRIPTION</span></span>
<span data-ttu-id="ad932-106">**New-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad932-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ad932-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad932-107">EXAMPLES</span></span>

### <span data-ttu-id="ad932-108">Örnek 1: yeni bir dosya ve yeni bir klasör oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad932-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="ad932-109">İlk komut, belirtilen hesap için dosya NewFile.txt oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad932-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="ad932-110">İkinci komut kök klasörde NewFolder klasörünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad932-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="ad932-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad932-111">PARAMETERS</span></span>

### <span data-ttu-id="ad932-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="ad932-112">-Account</span></span>
<span data-ttu-id="ad932-113">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad932-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ad932-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad932-114">-DefaultProfile</span></span>
<span data-ttu-id="ad932-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad932-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad932-116">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="ad932-116">-Encoding</span></span>
<span data-ttu-id="ad932-117">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad932-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="ad932-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ad932-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad932-119">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="ad932-119">Unknown</span></span>
- <span data-ttu-id="ad932-120">Dizisi</span><span class="sxs-lookup"><span data-stu-id="ad932-120">String</span></span>
- <span data-ttu-id="ad932-121">'Dur</span><span class="sxs-lookup"><span data-stu-id="ad932-121">Unicode</span></span>
- <span data-ttu-id="ad932-122">Inda</span><span class="sxs-lookup"><span data-stu-id="ad932-122">Byte</span></span>
- <span data-ttu-id="ad932-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="ad932-123">BigEndianUnicode</span></span>
- <span data-ttu-id="ad932-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="ad932-124">UTF8</span></span>
- <span data-ttu-id="ad932-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="ad932-125">UTF7</span></span>
- <span data-ttu-id="ad932-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="ad932-126">Ascii</span></span>
- <span data-ttu-id="ad932-127">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="ad932-127">Default</span></span>
- <span data-ttu-id="ad932-128">Doldur</span><span class="sxs-lookup"><span data-stu-id="ad932-128">Oem</span></span>
- <span data-ttu-id="ad932-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="ad932-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="ad932-130">-Klasör</span><span class="sxs-lookup"><span data-stu-id="ad932-130">-Folder</span></span>
<span data-ttu-id="ad932-131">Bu işlemin bir klasör oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad932-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="ad932-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ad932-132">-Force</span></span>
<span data-ttu-id="ad932-133">Zaten varsa, bu işlemin hedef öğenin üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ad932-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="ad932-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="ad932-134">-Path</span></span>
<span data-ttu-id="ad932-135">Kök dizinle (/) başlayarak oluşturulacak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad932-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ad932-136">-Değer</span><span class="sxs-lookup"><span data-stu-id="ad932-136">-Value</span></span>
<span data-ttu-id="ad932-137">Oluşturduğunuz öğeye eklenecek içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad932-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad932-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad932-138">-Confirm</span></span>
<span data-ttu-id="ad932-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad932-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad932-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad932-140">-WhatIf</span></span>
<span data-ttu-id="ad932-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad932-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad932-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad932-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad932-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad932-143">CommonParameters</span></span>
<span data-ttu-id="ad932-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad932-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad932-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad932-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad932-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad932-146">INPUTS</span></span>

### <span data-ttu-id="ad932-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ad932-147">System.String</span></span>

### <span data-ttu-id="ad932-148">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ad932-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ad932-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="ad932-149">System.Object</span></span>

### <span data-ttu-id="ad932-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="ad932-150">System.Text.Encoding</span></span>

### <span data-ttu-id="ad932-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ad932-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ad932-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad932-152">OUTPUTS</span></span>

### <span data-ttu-id="ad932-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ad932-153">System.String</span></span>

## <span data-ttu-id="ad932-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad932-154">NOTES</span></span>

## <span data-ttu-id="ad932-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad932-155">RELATED LINKS</span></span>

[<span data-ttu-id="ad932-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ad932-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="ad932-157">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ad932-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="ad932-158">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ad932-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="ad932-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ad932-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="ad932-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ad932-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="ad932-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ad932-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


