---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 828418095c7e77a7ee484d00e9d4d3f6f4a9927b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752338"
---
# <span data-ttu-id="4837d-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="4837d-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="4837d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4837d-102">SYNOPSIS</span></span>
<span data-ttu-id="4837d-103">Data Lake Store 'daki bir klasördeki öğelerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4837d-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="4837d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4837d-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4837d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4837d-105">DESCRIPTION</span></span>
<span data-ttu-id="4837d-106">**Get-AzDataLakeStoreChildItem** cmdlet 'ı, Data Lake Store 'daki bir klasördeki öğelerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4837d-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="4837d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4837d-107">EXAMPLES</span></span>

### <span data-ttu-id="4837d-108">Örnek 1: bir klasörün alt öğelerini alma</span><span class="sxs-lookup"><span data-stu-id="4837d-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="4837d-109">Bu komut MyFiles klasörünün alt öğelerini alır.</span><span class="sxs-lookup"><span data-stu-id="4837d-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="4837d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4837d-110">PARAMETERS</span></span>

### <span data-ttu-id="4837d-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4837d-111">-Account</span></span>
<span data-ttu-id="4837d-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4837d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4837d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4837d-113">-DefaultProfile</span></span>
<span data-ttu-id="4837d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4837d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4837d-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="4837d-115">-Path</span></span>
<span data-ttu-id="4837d-116">Kök dizinle (/) başlayarak klasörün Data Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4837d-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4837d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4837d-117">CommonParameters</span></span>
<span data-ttu-id="4837d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4837d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4837d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4837d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4837d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4837d-120">INPUTS</span></span>

### <span data-ttu-id="4837d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4837d-121">System.String</span></span>

### <span data-ttu-id="4837d-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4837d-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="4837d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4837d-123">OUTPUTS</span></span>

### <span data-ttu-id="4837d-124">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4837d-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="4837d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4837d-125">NOTES</span></span>

## <span data-ttu-id="4837d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4837d-126">RELATED LINKS</span></span>
