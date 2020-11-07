---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a7b47425aad152d8851ff90717698b4c25ef026d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763755"
---
# <span data-ttu-id="737ca-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="737ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737ca-102">SYNOPSIS</span></span>
<span data-ttu-id="737ca-103">Data Lake Store 'da bir dosya veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="737ca-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="737ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="737ca-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="737ca-105">DESCRIPTION</span></span>
<span data-ttu-id="737ca-106">**Get-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="737ca-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="737ca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="737ca-107">EXAMPLES</span></span>

### <span data-ttu-id="737ca-108">Örnek 1: veri Lake Store 'dan bir dosyanın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="737ca-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="737ca-109">Bu komut, Data Lake Store 'dan dosya Test.csv ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="737ca-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="737ca-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="737ca-110">PARAMETERS</span></span>

### <span data-ttu-id="737ca-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="737ca-111">-Account</span></span>
<span data-ttu-id="737ca-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="737ca-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="737ca-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="737ca-113">-Path</span></span>
<span data-ttu-id="737ca-114">Kök dizinden (/) başlayarak öğenin ayrıntılarının alınacağı veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="737ca-114">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="737ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737ca-115">-DefaultProfile</span></span>
<span data-ttu-id="737ca-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="737ca-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="737ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737ca-117">CommonParameters</span></span>
<span data-ttu-id="737ca-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="737ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737ca-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737ca-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737ca-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="737ca-120">INPUTS</span></span>

## <span data-ttu-id="737ca-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="737ca-121">OUTPUTS</span></span>

### <span data-ttu-id="737ca-122">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-122">DataLakeStoreItem</span></span>
<span data-ttu-id="737ca-123">Belirtilen yoldaki dosya veya klasör.</span><span class="sxs-lookup"><span data-stu-id="737ca-123">The file or folder at the path specified.</span></span>

## <span data-ttu-id="737ca-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="737ca-124">NOTES</span></span>

## <span data-ttu-id="737ca-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="737ca-125">RELATED LINKS</span></span>

[<span data-ttu-id="737ca-126">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-126">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="737ca-127">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="737ca-127">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="737ca-128">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-128">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="737ca-129">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-129">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="737ca-130">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-130">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="737ca-131">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-131">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="737ca-132">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-132">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="737ca-133">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="737ca-133">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


