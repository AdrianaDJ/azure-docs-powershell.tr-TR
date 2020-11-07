---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 750203e954ef96619e32b63ffd6eae333bb852f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916895"
---
# <span data-ttu-id="1495a-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="1495a-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="1495a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1495a-102">SYNOPSIS</span></span>
<span data-ttu-id="1495a-103">Çöp kutusunda filtreyle eşleşen silinmiş girdileri arar.</span><span class="sxs-lookup"><span data-stu-id="1495a-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="1495a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1495a-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1495a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1495a-105">DESCRIPTION</span></span>
<span data-ttu-id="1495a-106">**Get-AzDataLakeStoreDeletedItem** cmdlet 'ı, veri Lake Store 'da verilen filtreyle eşleşen silinmiş dosyaları veya klasörleri arar.</span><span class="sxs-lookup"><span data-stu-id="1495a-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="1495a-107">Silinmiş öğeler-OriginalPath, TrashDirPath, tür, CreationTime öğelerinin aşağıdaki özniteliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="1495a-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="1495a-108">Çöp kutusundaki milyonlarca dosyayı aramak ve bir iş olarak çalıştırmak zorunda kalabiliyor, bu da uzun süren bir işlem olabilir.</span><span class="sxs-lookup"><span data-stu-id="1495a-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>

## <span data-ttu-id="1495a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1495a-109">EXAMPLES</span></span>

### <span data-ttu-id="1495a-110">Örnek: Data Lake Store 'dan bir dosyanın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="1495a-110">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="1495a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1495a-111">PARAMETERS</span></span>

### <span data-ttu-id="1495a-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="1495a-112">-Account</span></span>
<span data-ttu-id="1495a-113">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1495a-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1495a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="1495a-114">-AsJob</span></span>
<span data-ttu-id="1495a-115">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1495a-115">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1495a-116">-Sayı</span><span class="sxs-lookup"><span data-stu-id="1495a-116">-Count</span></span>
<span data-ttu-id="1495a-117">Kullanıcının bulmak istediği sonuç sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1495a-117">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="1495a-118">Sorgu, sayım sonuçlarını bulana kadar çalışır veya tüm çöp aracılığıyla arar; hangisi önce olur.</span><span class="sxs-lookup"><span data-stu-id="1495a-118">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1495a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1495a-119">-DefaultProfile</span></span>
<span data-ttu-id="1495a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1495a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1495a-121">-Filtre</span><span class="sxs-lookup"><span data-stu-id="1495a-121">-Filter</span></span>
<span data-ttu-id="1495a-122">Arama sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1495a-122">Specifies the search query.</span></span> <span data-ttu-id="1495a-123">Daha belirgin bir değer daha ilgili sonuçlara olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1495a-123">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1495a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1495a-124">CommonParameters</span></span>
<span data-ttu-id="1495a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1495a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1495a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1495a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1495a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1495a-127">INPUTS</span></span>

### <span data-ttu-id="1495a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1495a-128">System.String</span></span>

## <span data-ttu-id="1495a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1495a-129">OUTPUTS</span></span>

### <span data-ttu-id="1495a-130">System. topluluklar. Generic. LIST<Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="1495a-130">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="1495a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1495a-131">NOTES</span></span>

## <span data-ttu-id="1495a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1495a-132">RELATED LINKS</span></span>

[<span data-ttu-id="1495a-133">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="1495a-133">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)