---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a087c2f7cfd4358e137550aa2e916fa2200d2a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593146"
---
# <span data-ttu-id="abd57-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abd57-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="abd57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abd57-102">SYNOPSIS</span></span>
<span data-ttu-id="abd57-103">Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="abd57-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abd57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abd57-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abd57-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="abd57-105">DESCRIPTION</span></span>
<span data-ttu-id="abd57-106">**New-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="abd57-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="abd57-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abd57-107">EXAMPLES</span></span>

### <span data-ttu-id="abd57-108">Örnek 1: yeni bir dosya ve yeni bir klasör oluşturma</span><span class="sxs-lookup"><span data-stu-id="abd57-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="abd57-109">İlk komut, belirtilen hesap için dosya NewFile.txt oluşturur.</span><span class="sxs-lookup"><span data-stu-id="abd57-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="abd57-110">İkinci komut kök klasörde NewFolder klasörünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="abd57-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="abd57-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abd57-111">PARAMETERS</span></span>

### <span data-ttu-id="abd57-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="abd57-112">-Account</span></span>
<span data-ttu-id="abd57-113">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abd57-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="abd57-114">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="abd57-114">-Encoding</span></span>
<span data-ttu-id="abd57-115">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abd57-115">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="abd57-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="abd57-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="abd57-117">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="abd57-117">Unknown</span></span>
- <span data-ttu-id="abd57-118">Dizisi</span><span class="sxs-lookup"><span data-stu-id="abd57-118">String</span></span>
- <span data-ttu-id="abd57-119">'Dur</span><span class="sxs-lookup"><span data-stu-id="abd57-119">Unicode</span></span>
- <span data-ttu-id="abd57-120">Inda</span><span class="sxs-lookup"><span data-stu-id="abd57-120">Byte</span></span>
- <span data-ttu-id="abd57-121">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="abd57-121">BigEndianUnicode</span></span>
- <span data-ttu-id="abd57-122">UTF8</span><span class="sxs-lookup"><span data-stu-id="abd57-122">UTF8</span></span>
- <span data-ttu-id="abd57-123">UTF7</span><span class="sxs-lookup"><span data-stu-id="abd57-123">UTF7</span></span>
- <span data-ttu-id="abd57-124">ASCII</span><span class="sxs-lookup"><span data-stu-id="abd57-124">Ascii</span></span>
- <span data-ttu-id="abd57-125">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="abd57-125">Default</span></span>
- <span data-ttu-id="abd57-126">Doldur</span><span class="sxs-lookup"><span data-stu-id="abd57-126">Oem</span></span>
- <span data-ttu-id="abd57-127">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="abd57-127">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abd57-128">-Klasör</span><span class="sxs-lookup"><span data-stu-id="abd57-128">-Folder</span></span>
<span data-ttu-id="abd57-129">Bu işlemin bir klasör oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="abd57-129">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="abd57-130">-Force</span><span class="sxs-lookup"><span data-stu-id="abd57-130">-Force</span></span>
<span data-ttu-id="abd57-131">Zaten varsa, bu işlemin hedef öğenin üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="abd57-131">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="abd57-132">-Yol</span><span class="sxs-lookup"><span data-stu-id="abd57-132">-Path</span></span>
<span data-ttu-id="abd57-133">Kök dizinle (/) başlayarak oluşturulacak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="abd57-133">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="abd57-134">-Değer</span><span class="sxs-lookup"><span data-stu-id="abd57-134">-Value</span></span>
<span data-ttu-id="abd57-135">Oluşturduğunuz öğeye eklenecek içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="abd57-135">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="abd57-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="abd57-136">-Confirm</span></span>
<span data-ttu-id="abd57-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abd57-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd57-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abd57-138">-WhatIf</span></span>
<span data-ttu-id="abd57-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="abd57-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abd57-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="abd57-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd57-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd57-141">-DefaultProfile</span></span>
<span data-ttu-id="abd57-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abd57-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abd57-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd57-143">CommonParameters</span></span>
<span data-ttu-id="abd57-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abd57-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd57-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd57-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd57-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abd57-146">INPUTS</span></span>

### <span data-ttu-id="abd57-147">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="abd57-147">Object</span></span>
<span data-ttu-id="abd57-148">' Value ' parametresi ardışık düzenin ' Object ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="abd57-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="abd57-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abd57-149">OUTPUTS</span></span>

### <span data-ttu-id="abd57-150">dizisi</span><span class="sxs-lookup"><span data-stu-id="abd57-150">string</span></span>
<span data-ttu-id="abd57-151">Oluşturulan dosyanın veya klasörün tam yolu.</span><span class="sxs-lookup"><span data-stu-id="abd57-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="abd57-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abd57-152">NOTES</span></span>

## <span data-ttu-id="abd57-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abd57-153">RELATED LINKS</span></span>

[<span data-ttu-id="abd57-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abd57-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="abd57-155">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abd57-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="abd57-156">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abd57-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="abd57-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abd57-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="abd57-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abd57-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="abd57-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abd57-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


