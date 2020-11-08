---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935056"
---
# <span data-ttu-id="70ffe-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="70ffe-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="70ffe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="70ffe-103">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="70ffe-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="70ffe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70ffe-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="70ffe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="70ffe-106">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="70ffe-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="70ffe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="70ffe-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="70ffe-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="70ffe-109">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="70ffe-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="70ffe-110">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="70ffe-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="70ffe-111">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="70ffe-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="70ffe-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70ffe-112">PARAMETERS</span></span>

### <span data-ttu-id="70ffe-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="70ffe-113">-FarmName</span></span>
<span data-ttu-id="70ffe-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="70ffe-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ffe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ffe-115">-ResourceGroupName</span></span>
<span data-ttu-id="70ffe-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="70ffe-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ffe-117">-Filtre</span><span class="sxs-lookup"><span data-stu-id="70ffe-117">-Filter</span></span>
<span data-ttu-id="70ffe-118">Filtre dizesi</span><span class="sxs-lookup"><span data-stu-id="70ffe-118">Filter string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ffe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ffe-119">CommonParameters</span></span>
<span data-ttu-id="70ffe-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70ffe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ffe-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ffe-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ffe-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70ffe-122">INPUTS</span></span>

## <span data-ttu-id="70ffe-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70ffe-123">OUTPUTS</span></span>

## <span data-ttu-id="70ffe-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70ffe-124">NOTES</span></span>

## <span data-ttu-id="70ffe-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70ffe-125">RELATED LINKS</span></span>