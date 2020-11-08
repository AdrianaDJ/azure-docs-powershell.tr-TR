---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd62756b3a41af82a245a39d4f80478d47d90e1c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935065"
---
# <span data-ttu-id="72f61-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="72f61-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="72f61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f61-102">SYNOPSIS</span></span>
<span data-ttu-id="72f61-103">Çöp toplama işinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="72f61-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="72f61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72f61-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="72f61-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72f61-105">DESCRIPTION</span></span>
<span data-ttu-id="72f61-106">Çöp toplama işinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="72f61-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="72f61-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72f61-107">EXAMPLES</span></span>

### <span data-ttu-id="72f61-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="72f61-108">EXAMPLE 1</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="72f61-109">Çöp koleksiyonunun durumu hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="72f61-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="72f61-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72f61-110">PARAMETERS</span></span>

### <span data-ttu-id="72f61-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="72f61-111">-FarmName</span></span>
<span data-ttu-id="72f61-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="72f61-112">Farm Id.</span></span>

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

### <span data-ttu-id="72f61-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="72f61-113">-JobId</span></span>
<span data-ttu-id="72f61-114">İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="72f61-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f61-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f61-115">-ResourceGroupName</span></span>
<span data-ttu-id="72f61-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="72f61-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f61-117">CommonParameters</span></span>
<span data-ttu-id="72f61-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72f61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f61-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f61-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f61-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72f61-120">INPUTS</span></span>

## <span data-ttu-id="72f61-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72f61-121">OUTPUTS</span></span>

## <span data-ttu-id="72f61-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72f61-122">NOTES</span></span>

## <span data-ttu-id="72f61-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72f61-123">RELATED LINKS</span></span>