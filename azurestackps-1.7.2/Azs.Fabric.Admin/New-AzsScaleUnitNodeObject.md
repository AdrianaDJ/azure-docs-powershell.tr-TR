---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934109"
---
# <span data-ttu-id="c969b-101">New-AzsScaleUnitNodeObject</span><span class="sxs-lookup"><span data-stu-id="c969b-101">New-AzsScaleUnitNodeObject</span></span>

## <span data-ttu-id="c969b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c969b-102">SYNOPSIS</span></span>
<span data-ttu-id="c969b-103">Ölçek birimi düğümü eklemeye olanak sağlayan giriş verileri.</span><span class="sxs-lookup"><span data-stu-id="c969b-103">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="c969b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c969b-104">SYNTAX</span></span>

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c969b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c969b-105">DESCRIPTION</span></span>
<span data-ttu-id="c969b-106">Ölçek birimi düğümü eklemeye olanak sağlayan giriş verileri.</span><span class="sxs-lookup"><span data-stu-id="c969b-106">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="c969b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c969b-107">EXAMPLES</span></span>

### <span data-ttu-id="c969b-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c969b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

<span data-ttu-id="c969b-109">Yeni bir düğüm nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c969b-109">Create a new node object.</span></span>

## <span data-ttu-id="c969b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c969b-110">PARAMETERS</span></span>

### <span data-ttu-id="c969b-111">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="c969b-111">-BMCIPv4Address</span></span>
<span data-ttu-id="c969b-112">Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="c969b-112">Bmc address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c969b-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="c969b-113">-ComputerName</span></span>
<span data-ttu-id="c969b-114">Fiziksel makinenin bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="c969b-114">Computer name of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c969b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c969b-115">CommonParameters</span></span>
<span data-ttu-id="c969b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c969b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c969b-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c969b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c969b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c969b-118">INPUTS</span></span>

## <span data-ttu-id="c969b-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c969b-119">OUTPUTS</span></span>

## <span data-ttu-id="c969b-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c969b-120">NOTES</span></span>

## <span data-ttu-id="c969b-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c969b-121">RELATED LINKS</span></span>
