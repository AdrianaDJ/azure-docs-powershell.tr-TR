---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/join-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: c321c605977e09f119d19e5c4ced44261c3de0cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588931"
---
# <span data-ttu-id="6ce0f-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6ce0f-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6ce0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ce0f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce0f-103">Veri Lake Store 'da bir dosya oluşturmak için bir veya birden çok dosyaya katılır.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ce0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ce0f-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ce0f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce0f-106">**Join-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosya oluşturmak için bir veya birden çok dosyaya katılır.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="6ce0f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ce0f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ce0f-108">Örnek 1: iki öğeye katılma</span><span class="sxs-lookup"><span data-stu-id="6ce0f-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="6ce0f-109">Bu komut File01.txt ve File02.txt CombinedFile.txt dosyayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="6ce0f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ce0f-110">PARAMETERS</span></span>

### <span data-ttu-id="6ce0f-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="6ce0f-111">-Account</span></span>
<span data-ttu-id="6ce0f-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6ce0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce0f-113">-DefaultProfile</span></span>
<span data-ttu-id="6ce0f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ce0f-115">-Hedef</span><span class="sxs-lookup"><span data-stu-id="6ce0f-115">-Destination</span></span>
<span data-ttu-id="6ce0f-116">Kök dizinden (/) başlayarak, birleştirilmiş öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce0f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6ce0f-117">-Force</span></span>
<span data-ttu-id="6ce0f-118">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="6ce0f-119">-Yollar</span><span class="sxs-lookup"><span data-stu-id="6ce0f-119">-Paths</span></span>
<span data-ttu-id="6ce0f-120">Kök dizinden (/) başlayarak birleştirilecek olan dosyaların veri Lake Store yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce0f-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ce0f-121">-Confirm</span></span>
<span data-ttu-id="6ce0f-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce0f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce0f-123">-WhatIf</span></span>
<span data-ttu-id="6ce0f-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce0f-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce0f-126">CommonParameters</span></span>
<span data-ttu-id="6ce0f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce0f-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce0f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce0f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ce0f-129">INPUTS</span></span>

### <span data-ttu-id="6ce0f-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ce0f-130">None</span></span>
<span data-ttu-id="6ce0f-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ce0f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ce0f-132">OUTPUTS</span></span>

### <span data-ttu-id="6ce0f-133">dizisi</span><span class="sxs-lookup"><span data-stu-id="6ce0f-133">string</span></span>
<span data-ttu-id="6ce0f-134">Birleştirilen dosyalardaki sonuç dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="6ce0f-134">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="6ce0f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ce0f-135">NOTES</span></span>

## <span data-ttu-id="6ce0f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ce0f-136">RELATED LINKS</span></span>

[<span data-ttu-id="6ce0f-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6ce0f-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6ce0f-138">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6ce0f-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6ce0f-139">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6ce0f-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6ce0f-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6ce0f-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6ce0f-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6ce0f-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6ce0f-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6ce0f-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


