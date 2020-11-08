---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934417"
---
# <span data-ttu-id="68242-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="68242-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="68242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68242-102">SYNOPSIS</span></span>
<span data-ttu-id="68242-103">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="68242-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="68242-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68242-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="68242-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68242-105">DESCRIPTION</span></span>
<span data-ttu-id="68242-106">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="68242-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="68242-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68242-107">EXAMPLES</span></span>

### <span data-ttu-id="68242-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="68242-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="68242-109">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="68242-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="68242-110">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="68242-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="68242-111">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="68242-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="68242-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68242-112">PARAMETERS</span></span>

### <span data-ttu-id="68242-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="68242-113">-FarmName</span></span>
<span data-ttu-id="68242-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="68242-114">Farm Id.</span></span>

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

### <span data-ttu-id="68242-115">-Filtre</span><span class="sxs-lookup"><span data-stu-id="68242-115">-Filter</span></span>
<span data-ttu-id="68242-116">Filtre dizesi</span><span class="sxs-lookup"><span data-stu-id="68242-116">Filter string</span></span>

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

### <span data-ttu-id="68242-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68242-117">-ResourceGroupName</span></span>
<span data-ttu-id="68242-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="68242-118">Resource group name.</span></span>

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

### <span data-ttu-id="68242-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68242-119">CommonParameters</span></span>
<span data-ttu-id="68242-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68242-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68242-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68242-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68242-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68242-122">INPUTS</span></span>

## <span data-ttu-id="68242-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68242-123">OUTPUTS</span></span>

## <span data-ttu-id="68242-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68242-124">NOTES</span></span>

## <span data-ttu-id="68242-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68242-125">RELATED LINKS</span></span>
