---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 76490987a6a4d016a1d07b29cd69484305ddf849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916899"
---
# <span data-ttu-id="a011a-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="a011a-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="a011a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a011a-102">SYNOPSIS</span></span>
<span data-ttu-id="a011a-103">Belirtilen yoldaki toplam boyut, dosya ve dizinlerin özetini alır</span><span class="sxs-lookup"><span data-stu-id="a011a-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="a011a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a011a-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a011a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a011a-105">DESCRIPTION</span></span>
<span data-ttu-id="a011a-106">**Get-AzDataLakeStoreChildItemSummary** , belirli bir yol için içerik özetini getirir.</span><span class="sxs-lookup"><span data-stu-id="a011a-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="a011a-107">Bu, verilen yoldaki tüm dosyaların, dizinlerin ve toplam dosyalarının toplam sayısını yinelemeli olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="a011a-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="a011a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a011a-108">EXAMPLES</span></span>

### <span data-ttu-id="a011a-109">Örnek 1: klasörün içerik özetini alma</span><span class="sxs-lookup"><span data-stu-id="a011a-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="a011a-110">Toplam dizinlerin, dosyaların ve bu sayının,/A'in altında yer alan sayısını listeler.</span><span class="sxs-lookup"><span data-stu-id="a011a-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="a011a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a011a-111">PARAMETERS</span></span>

### <span data-ttu-id="a011a-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="a011a-112">-Account</span></span>
<span data-ttu-id="a011a-113">Dosya sistemi işlemini yürütme</span><span class="sxs-lookup"><span data-stu-id="a011a-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="a011a-114">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="a011a-114">-Concurrency</span></span>
<span data-ttu-id="a011a-115">Paralel olarak işlenen dosya/dizinlerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a011a-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="a011a-116">Varsayılan, sistem belirtimine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a011a-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a011a-117">-DefaultProfile</span></span>
<span data-ttu-id="a011a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a011a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a011a-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="a011a-119">-Path</span></span>
<span data-ttu-id="a011a-120">Belirtilen Data Lake hesabındaki yol.</span><span class="sxs-lookup"><span data-stu-id="a011a-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="a011a-121">'/Folder/file.txt ' biçiminde bir dosya veya klasör olabilir; burada DNS, ilk '/', dosya sisteminin kökünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="a011a-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a011a-122">-Confirm</span></span>
<span data-ttu-id="a011a-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a011a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a011a-124">-WhatIf</span></span>
<span data-ttu-id="a011a-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a011a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a011a-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a011a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a011a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a011a-127">CommonParameters</span></span>
<span data-ttu-id="a011a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a011a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a011a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a011a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a011a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a011a-130">INPUTS</span></span>

### <span data-ttu-id="a011a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a011a-131">System.String</span></span>

### <span data-ttu-id="a011a-132">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a011a-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a011a-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a011a-133">System.Int32</span></span>

## <span data-ttu-id="a011a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a011a-134">OUTPUTS</span></span>

### <span data-ttu-id="a011a-135">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="a011a-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="a011a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a011a-136">NOTES</span></span>

## <span data-ttu-id="a011a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a011a-137">RELATED LINKS</span></span>
