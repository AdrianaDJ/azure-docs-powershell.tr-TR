---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2e50135762826661e82f499f2aec48c67d00c648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572814"
---
# <span data-ttu-id="ce454-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ce454-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="ce454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce454-102">SYNOPSIS</span></span>
<span data-ttu-id="ce454-103">Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ce454-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce454-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce454-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce454-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce454-105">DESCRIPTION</span></span>
<span data-ttu-id="ce454-106">**New-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da yeni bir dosya veya klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ce454-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ce454-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce454-107">EXAMPLES</span></span>

### <span data-ttu-id="ce454-108">Örnek 1: yeni bir dosya ve yeni bir klasör oluşturma</span><span class="sxs-lookup"><span data-stu-id="ce454-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="ce454-109">İlk komut, belirtilen hesap için dosya NewFile.txt oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ce454-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="ce454-110">İkinci komut kök klasörde NewFolder klasörünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ce454-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="ce454-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce454-111">PARAMETERS</span></span>

### <span data-ttu-id="ce454-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="ce454-112">-Account</span></span>
<span data-ttu-id="ce454-113">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce454-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ce454-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce454-114">-DefaultProfile</span></span>
<span data-ttu-id="ce454-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce454-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce454-116">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="ce454-116">-Encoding</span></span>
<span data-ttu-id="ce454-117">Oluşturulacak öğenin kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce454-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="ce454-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ce454-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce454-119">Bilinmediği</span><span class="sxs-lookup"><span data-stu-id="ce454-119">Unknown</span></span>
- <span data-ttu-id="ce454-120">Dizisi</span><span class="sxs-lookup"><span data-stu-id="ce454-120">String</span></span>
- <span data-ttu-id="ce454-121">'Dur</span><span class="sxs-lookup"><span data-stu-id="ce454-121">Unicode</span></span>
- <span data-ttu-id="ce454-122">Inda</span><span class="sxs-lookup"><span data-stu-id="ce454-122">Byte</span></span>
- <span data-ttu-id="ce454-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="ce454-123">BigEndianUnicode</span></span>
- <span data-ttu-id="ce454-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="ce454-124">UTF8</span></span>
- <span data-ttu-id="ce454-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="ce454-125">UTF7</span></span>
- <span data-ttu-id="ce454-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="ce454-126">Ascii</span></span>
- <span data-ttu-id="ce454-127">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="ce454-127">Default</span></span>
- <span data-ttu-id="ce454-128">Doldur</span><span class="sxs-lookup"><span data-stu-id="ce454-128">Oem</span></span>
- <span data-ttu-id="ce454-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="ce454-129">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce454-130">-Klasör</span><span class="sxs-lookup"><span data-stu-id="ce454-130">-Folder</span></span>
<span data-ttu-id="ce454-131">Bu işlemin bir klasör oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce454-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="ce454-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ce454-132">-Force</span></span>
<span data-ttu-id="ce454-133">Zaten varsa, bu işlemin hedef öğenin üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ce454-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="ce454-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="ce454-134">-Path</span></span>
<span data-ttu-id="ce454-135">Kök dizinle (/) başlayarak oluşturulacak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce454-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ce454-136">-Değer</span><span class="sxs-lookup"><span data-stu-id="ce454-136">-Value</span></span>
<span data-ttu-id="ce454-137">Oluşturduğunuz öğeye eklenecek içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce454-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="ce454-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce454-138">-Confirm</span></span>
<span data-ttu-id="ce454-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce454-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce454-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce454-140">-WhatIf</span></span>
<span data-ttu-id="ce454-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce454-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce454-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce454-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce454-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce454-143">CommonParameters</span></span>
<span data-ttu-id="ce454-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce454-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce454-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce454-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce454-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce454-146">INPUTS</span></span>

### <span data-ttu-id="ce454-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ce454-147">System.String</span></span>

### <span data-ttu-id="ce454-148">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ce454-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ce454-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce454-149">System.Object</span></span>

### <span data-ttu-id="ce454-150">Microsoft. Azure. Commands. DataLakeStore. modeller. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="ce454-150">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="ce454-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce454-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ce454-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce454-152">OUTPUTS</span></span>

### <span data-ttu-id="ce454-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ce454-153">System.String</span></span>
<span data-ttu-id="ce454-154">Oluşturulan dosyanın veya klasörün tam yolu.</span><span class="sxs-lookup"><span data-stu-id="ce454-154">The full path to the created file or folder.</span></span>

## <span data-ttu-id="ce454-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce454-155">NOTES</span></span>

## <span data-ttu-id="ce454-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce454-156">RELATED LINKS</span></span>

[<span data-ttu-id="ce454-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ce454-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ce454-158">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ce454-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ce454-159">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ce454-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ce454-160">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ce454-160">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ce454-161">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ce454-161">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ce454-162">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ce454-162">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


