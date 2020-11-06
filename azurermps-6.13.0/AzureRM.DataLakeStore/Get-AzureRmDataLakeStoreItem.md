---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a1e70286364fea53062a75b7ac886834803c3674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593681"
---
# <span data-ttu-id="4cc5d-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="4cc5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc5d-103">Data Lake Store 'da bir dosya veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4cc5d-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cc5d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cc5d-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc5d-106">**Get-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4cc5d-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4cc5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cc5d-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc5d-108">Örnek 1: veri Lake Store 'dan bir dosyanın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="4cc5d-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="4cc5d-109">Bu komut, Data Lake Store 'dan dosya Test.csv ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4cc5d-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="4cc5d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cc5d-110">PARAMETERS</span></span>

### <span data-ttu-id="4cc5d-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4cc5d-111">-Account</span></span>
<span data-ttu-id="4cc5d-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cc5d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4cc5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc5d-113">-DefaultProfile</span></span>
<span data-ttu-id="4cc5d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cc5d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cc5d-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="4cc5d-115">-Path</span></span>
<span data-ttu-id="4cc5d-116">Kök dizinden (/) başlayarak öğenin ayrıntılarının alınacağı veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cc5d-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4cc5d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc5d-117">CommonParameters</span></span>
<span data-ttu-id="4cc5d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cc5d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc5d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc5d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc5d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cc5d-120">INPUTS</span></span>

### <span data-ttu-id="4cc5d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc5d-121">System.String</span></span>

### <span data-ttu-id="4cc5d-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4cc5d-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="4cc5d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cc5d-123">OUTPUTS</span></span>

### <span data-ttu-id="4cc5d-124">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="4cc5d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cc5d-125">NOTES</span></span>

## <span data-ttu-id="4cc5d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cc5d-126">RELATED LINKS</span></span>

[<span data-ttu-id="4cc5d-127">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-127">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4cc5d-128">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-128">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="4cc5d-129">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-129">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4cc5d-130">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-130">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4cc5d-131">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-131">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4cc5d-132">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-132">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4cc5d-133">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-133">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4cc5d-134">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cc5d-134">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


