---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934839"
---
# <span data-ttu-id="797da-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="797da-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="797da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="797da-102">SYNOPSIS</span></span>
<span data-ttu-id="797da-103">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="797da-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="797da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="797da-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="797da-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="797da-105">DESCRIPTION</span></span>
<span data-ttu-id="797da-106">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="797da-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="797da-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="797da-107">EXAMPLES</span></span>

### <span data-ttu-id="797da-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="797da-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="797da-109">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="797da-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="797da-110">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="797da-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="797da-111">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="797da-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="797da-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="797da-112">PARAMETERS</span></span>

### <span data-ttu-id="797da-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="797da-113">-FarmName</span></span>
<span data-ttu-id="797da-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="797da-114">Farm Id.</span></span>

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

### <span data-ttu-id="797da-115">-Filtre</span><span class="sxs-lookup"><span data-stu-id="797da-115">-Filter</span></span>
<span data-ttu-id="797da-116">Filtre dizesi</span><span class="sxs-lookup"><span data-stu-id="797da-116">Filter string</span></span>

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

### <span data-ttu-id="797da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="797da-117">-ResourceGroupName</span></span>
<span data-ttu-id="797da-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="797da-118">Resource group name.</span></span>

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

### <span data-ttu-id="797da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797da-119">CommonParameters</span></span>
<span data-ttu-id="797da-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="797da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797da-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="797da-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797da-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="797da-122">INPUTS</span></span>

## <span data-ttu-id="797da-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="797da-123">OUTPUTS</span></span>

## <span data-ttu-id="797da-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="797da-124">NOTES</span></span>

## <span data-ttu-id="797da-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="797da-125">RELATED LINKS</span></span>

