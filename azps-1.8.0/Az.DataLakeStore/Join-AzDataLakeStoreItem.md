---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 7ff40890783edbfaf610434f0b25ad04b4b3be21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761066"
---
# <span data-ttu-id="120e4-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="120e4-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="120e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120e4-102">SYNOPSIS</span></span>
<span data-ttu-id="120e4-103">Veri Lake Store 'da bir dosya oluşturmak için bir veya birden çok dosyaya katılır.</span><span class="sxs-lookup"><span data-stu-id="120e4-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="120e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="120e4-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="120e4-105">DESCRIPTION</span></span>
<span data-ttu-id="120e4-106">**Join-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosya oluşturmak için bir veya birden çok dosyaya katılır.</span><span class="sxs-lookup"><span data-stu-id="120e4-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="120e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="120e4-107">EXAMPLES</span></span>

### <span data-ttu-id="120e4-108">Örnek 1: iki öğeye katılma</span><span class="sxs-lookup"><span data-stu-id="120e4-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="120e4-109">Bu komut File01.txt ve File02.txt CombinedFile.txt dosyayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="120e4-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="120e4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="120e4-110">PARAMETERS</span></span>

### <span data-ttu-id="120e4-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="120e4-111">-Account</span></span>
<span data-ttu-id="120e4-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="120e4-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="120e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120e4-113">-DefaultProfile</span></span>
<span data-ttu-id="120e4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="120e4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="120e4-115">-Hedef</span><span class="sxs-lookup"><span data-stu-id="120e4-115">-Destination</span></span>
<span data-ttu-id="120e4-116">Kök dizinden (/) başlayarak, birleştirilmiş öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="120e4-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="120e4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="120e4-117">-Force</span></span>
<span data-ttu-id="120e4-118">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="120e4-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="120e4-119">-Yollar</span><span class="sxs-lookup"><span data-stu-id="120e4-119">-Paths</span></span>
<span data-ttu-id="120e4-120">Kök dizinden (/) başlayarak birleştirilecek olan dosyaların veri Lake Store yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="120e4-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="120e4-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="120e4-121">-Confirm</span></span>
<span data-ttu-id="120e4-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="120e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120e4-123">-WhatIf</span></span>
<span data-ttu-id="120e4-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="120e4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120e4-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="120e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120e4-126">CommonParameters</span></span>
<span data-ttu-id="120e4-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="120e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120e4-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="120e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120e4-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="120e4-129">INPUTS</span></span>

### <span data-ttu-id="120e4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="120e4-130">System.String</span></span>

### <span data-ttu-id="120e4-131">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="120e4-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="120e4-132">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="120e4-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="120e4-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="120e4-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="120e4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="120e4-134">OUTPUTS</span></span>

### <span data-ttu-id="120e4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="120e4-135">System.String</span></span>

## <span data-ttu-id="120e4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="120e4-136">NOTES</span></span>

## <span data-ttu-id="120e4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="120e4-137">RELATED LINKS</span></span>

[<span data-ttu-id="120e4-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="120e4-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="120e4-139">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="120e4-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="120e4-140">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="120e4-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="120e4-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="120e4-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="120e4-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="120e4-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="120e4-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="120e4-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


