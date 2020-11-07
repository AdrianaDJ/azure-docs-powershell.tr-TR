---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937783"
---
# <span data-ttu-id="d37b8-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d37b8-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="d37b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d37b8-103">Veri Lake Store 'da bir dosya oluşturmak için bir veya birden çok dosyaya katılır.</span><span class="sxs-lookup"><span data-stu-id="d37b8-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="d37b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d37b8-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d37b8-105">DESCRIPTION</span></span>
<span data-ttu-id="d37b8-106">**Join-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosya oluşturmak için bir veya birden çok dosyaya katılır.</span><span class="sxs-lookup"><span data-stu-id="d37b8-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="d37b8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d37b8-107">EXAMPLES</span></span>

### <span data-ttu-id="d37b8-108">Örnek 1: iki öğeye katılma</span><span class="sxs-lookup"><span data-stu-id="d37b8-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="d37b8-109">Bu komut File01.txt ve File02.txt CombinedFile.txt dosyayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d37b8-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="d37b8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d37b8-110">PARAMETERS</span></span>

### <span data-ttu-id="d37b8-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="d37b8-111">-Account</span></span>
<span data-ttu-id="d37b8-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d37b8-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d37b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37b8-113">-DefaultProfile</span></span>
<span data-ttu-id="d37b8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d37b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d37b8-115">-Hedef</span><span class="sxs-lookup"><span data-stu-id="d37b8-115">-Destination</span></span>
<span data-ttu-id="d37b8-116">Kök dizinden (/) başlayarak, birleştirilmiş öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d37b8-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d37b8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d37b8-117">-Force</span></span>
<span data-ttu-id="d37b8-118">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d37b8-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="d37b8-119">-Yollar</span><span class="sxs-lookup"><span data-stu-id="d37b8-119">-Paths</span></span>
<span data-ttu-id="d37b8-120">Kök dizinden (/) başlayarak birleştirilecek olan dosyaların veri Lake Store yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d37b8-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d37b8-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d37b8-121">-Confirm</span></span>
<span data-ttu-id="d37b8-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d37b8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37b8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37b8-123">-WhatIf</span></span>
<span data-ttu-id="d37b8-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d37b8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37b8-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d37b8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37b8-126">CommonParameters</span></span>
<span data-ttu-id="d37b8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d37b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37b8-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37b8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37b8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d37b8-129">INPUTS</span></span>

### <span data-ttu-id="d37b8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d37b8-130">System.String</span></span>

### <span data-ttu-id="d37b8-131">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="d37b8-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="d37b8-132">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d37b8-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d37b8-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d37b8-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d37b8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d37b8-134">OUTPUTS</span></span>

### <span data-ttu-id="d37b8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d37b8-135">System.String</span></span>

## <span data-ttu-id="d37b8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d37b8-136">NOTES</span></span>

## <span data-ttu-id="d37b8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d37b8-137">RELATED LINKS</span></span>

[<span data-ttu-id="d37b8-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d37b8-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="d37b8-139">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d37b8-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="d37b8-140">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d37b8-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="d37b8-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d37b8-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="d37b8-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d37b8-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="d37b8-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d37b8-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


