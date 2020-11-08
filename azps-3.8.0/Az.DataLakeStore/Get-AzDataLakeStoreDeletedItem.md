---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095981"
---
# <span data-ttu-id="72af3-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="72af3-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="72af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72af3-102">SYNOPSIS</span></span>
<span data-ttu-id="72af3-103">Çöp kutusunda filtreyle eşleşen silinmiş girdileri arar.</span><span class="sxs-lookup"><span data-stu-id="72af3-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="72af3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72af3-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72af3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72af3-105">DESCRIPTION</span></span>
<span data-ttu-id="72af3-106">**Get-AzDataLakeStoreDeletedItem** cmdlet 'ı, veri Lake Store 'da verilen filtreyle eşleşen silinmiş dosyaları veya klasörleri arar.</span><span class="sxs-lookup"><span data-stu-id="72af3-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="72af3-107">Silinmiş öğeler-OriginalPath, TrashDirPath, tür, CreationTime öğelerinin aşağıdaki özniteliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="72af3-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="72af3-108">Çöp kutusundaki milyonlarca dosyayı aramak ve bir iş olarak çalıştırmak zorunda kalabiliyor, bu da uzun süren bir işlem olabilir.</span><span class="sxs-lookup"><span data-stu-id="72af3-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="72af3-109">Dikkat: dosyaların silinmesini kaldırma işlemi en iyi çaba işlemidir.</span><span class="sxs-lookup"><span data-stu-id="72af3-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="72af3-110">Bir dosyanın silindikten sonra geri yüklenebileceğini garanti etmez.</span><span class="sxs-lookup"><span data-stu-id="72af3-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="72af3-111">Bu API kullanımı, Whitelist ile etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="72af3-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="72af3-112">ADL hesabınız beyaz listelenmezse, bu API 'yi kullanmak throw özel durumuna uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="72af3-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="72af3-113">Daha fazla bilgi ve yardım için lütfen Microsoft desteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="72af3-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="72af3-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72af3-114">EXAMPLES</span></span>

### <span data-ttu-id="72af3-115">Örnek: Data Lake Store 'dan bir dosyanın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="72af3-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="72af3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72af3-116">PARAMETERS</span></span>

### <span data-ttu-id="72af3-117">-Hesap</span><span class="sxs-lookup"><span data-stu-id="72af3-117">-Account</span></span>
<span data-ttu-id="72af3-118">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72af3-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="72af3-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="72af3-119">-AsJob</span></span>
<span data-ttu-id="72af3-120">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="72af3-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="72af3-121">-Sayı</span><span class="sxs-lookup"><span data-stu-id="72af3-121">-Count</span></span>
<span data-ttu-id="72af3-122">Kullanıcının bulmak istediği sonuç sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72af3-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="72af3-123">Sorgu, sayım sonuçlarını bulana kadar çalışır veya tüm çöp aracılığıyla arar; hangisi önce olur.</span><span class="sxs-lookup"><span data-stu-id="72af3-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="72af3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72af3-124">-DefaultProfile</span></span>
<span data-ttu-id="72af3-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72af3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72af3-126">-Filtre</span><span class="sxs-lookup"><span data-stu-id="72af3-126">-Filter</span></span>
<span data-ttu-id="72af3-127">Arama sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72af3-127">Specifies the search query.</span></span> <span data-ttu-id="72af3-128">Daha belirgin bir değer daha ilgili sonuçlara olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="72af3-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="72af3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72af3-129">CommonParameters</span></span>
<span data-ttu-id="72af3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72af3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72af3-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72af3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72af3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72af3-132">INPUTS</span></span>

### <span data-ttu-id="72af3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="72af3-133">System.String</span></span>

## <span data-ttu-id="72af3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72af3-134">OUTPUTS</span></span>

### <span data-ttu-id="72af3-135">System. topluluklar. Generic. LIST<Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="72af3-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="72af3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72af3-136">NOTES</span></span>

## <span data-ttu-id="72af3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72af3-137">RELATED LINKS</span></span>

[<span data-ttu-id="72af3-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="72af3-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)