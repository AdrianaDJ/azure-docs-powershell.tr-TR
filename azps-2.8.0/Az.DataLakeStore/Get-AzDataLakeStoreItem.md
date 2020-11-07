---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: b3118c11fa794fef71836a580e272ec481c72147
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752325"
---
# <span data-ttu-id="b851e-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="b851e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b851e-102">SYNOPSIS</span></span>
<span data-ttu-id="b851e-103">Data Lake Store 'da bir dosya veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b851e-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b851e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b851e-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b851e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b851e-105">DESCRIPTION</span></span>
<span data-ttu-id="b851e-106">**Get-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b851e-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b851e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b851e-107">EXAMPLES</span></span>

### <span data-ttu-id="b851e-108">Örnek 1: veri Lake Store 'dan bir dosyanın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="b851e-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="b851e-109">Bu komut, Data Lake Store 'dan dosya Test.csv ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b851e-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="b851e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b851e-110">PARAMETERS</span></span>

### <span data-ttu-id="b851e-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="b851e-111">-Account</span></span>
<span data-ttu-id="b851e-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b851e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b851e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b851e-113">-DefaultProfile</span></span>
<span data-ttu-id="b851e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b851e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b851e-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="b851e-115">-Path</span></span>
<span data-ttu-id="b851e-116">Kök dizinden (/) başlayarak öğenin ayrıntılarının alınacağı veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b851e-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b851e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b851e-117">CommonParameters</span></span>
<span data-ttu-id="b851e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b851e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b851e-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b851e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b851e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b851e-120">INPUTS</span></span>

### <span data-ttu-id="b851e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b851e-121">System.String</span></span>

### <span data-ttu-id="b851e-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b851e-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="b851e-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b851e-123">OUTPUTS</span></span>

### <span data-ttu-id="b851e-124">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="b851e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b851e-125">NOTES</span></span>

## <span data-ttu-id="b851e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b851e-126">RELATED LINKS</span></span>

[<span data-ttu-id="b851e-127">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="b851e-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="b851e-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="b851e-129">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="b851e-130">Katıl-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="b851e-131">Taşı-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="b851e-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="b851e-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="b851e-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b851e-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


