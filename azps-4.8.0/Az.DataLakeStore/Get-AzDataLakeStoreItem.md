---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107852"
---
# <span data-ttu-id="f513c-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f513c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f513c-102">SYNOPSIS</span></span>
<span data-ttu-id="f513c-103">Data Lake Store 'da bir dosya veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f513c-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f513c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f513c-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f513c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f513c-105">DESCRIPTION</span></span>
<span data-ttu-id="f513c-106">**Get-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f513c-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f513c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f513c-107">EXAMPLES</span></span>

### <span data-ttu-id="f513c-108">Örnek 1: veri Lake Store 'dan bir dosyanın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="f513c-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="f513c-109">Bu komut, Data Lake Store 'dan dosya Test.csv ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f513c-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="f513c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f513c-110">PARAMETERS</span></span>

### <span data-ttu-id="f513c-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f513c-111">-Account</span></span>
<span data-ttu-id="f513c-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f513c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f513c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f513c-113">-DefaultProfile</span></span>
<span data-ttu-id="f513c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f513c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f513c-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="f513c-115">-Path</span></span>
<span data-ttu-id="f513c-116">Kök dizinden (/) başlayarak öğenin ayrıntılarının alınacağı veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f513c-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f513c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f513c-117">CommonParameters</span></span>
<span data-ttu-id="f513c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f513c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f513c-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f513c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f513c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f513c-120">INPUTS</span></span>

### <span data-ttu-id="f513c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f513c-121">System.String</span></span>

### <span data-ttu-id="f513c-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f513c-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="f513c-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f513c-123">OUTPUTS</span></span>

### <span data-ttu-id="f513c-124">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="f513c-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f513c-125">NOTES</span></span>

## <span data-ttu-id="f513c-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f513c-126">RELATED LINKS</span></span>

[<span data-ttu-id="f513c-127">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f513c-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="f513c-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="f513c-129">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f513c-130">Katıl-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="f513c-131">Taşı-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="f513c-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f513c-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f513c-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f513c-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


