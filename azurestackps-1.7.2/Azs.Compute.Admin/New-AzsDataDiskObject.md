---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933916"
---
# <span data-ttu-id="7954e-101">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="7954e-101">New-AzsDataDiskObject</span></span>

## <span data-ttu-id="7954e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7954e-102">SYNOPSIS</span></span>
<span data-ttu-id="7954e-103">Yeni bir sanal makine platformu görüntüsü oluşturmak için kullanılan bir veri diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7954e-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="7954e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7954e-104">SYNTAX</span></span>

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7954e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7954e-105">DESCRIPTION</span></span>
<span data-ttu-id="7954e-106">Veri diski hakkında nesne içeren bir bilgi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7954e-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="7954e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7954e-107">EXAMPLES</span></span>

### <span data-ttu-id="7954e-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7954e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="7954e-109">Yeni bir veri disketi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7954e-109">Create a new data disk object.</span></span>

## <span data-ttu-id="7954e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7954e-110">PARAMETERS</span></span>

### <span data-ttu-id="7954e-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="7954e-111">-Lun</span></span>
<span data-ttu-id="7954e-112">Mantıksal birim numarası.</span><span class="sxs-lookup"><span data-stu-id="7954e-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7954e-113">-URI</span><span class="sxs-lookup"><span data-stu-id="7954e-113">-Uri</span></span>
<span data-ttu-id="7954e-114">Disk şablonunun konumu.</span><span class="sxs-lookup"><span data-stu-id="7954e-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="7954e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7954e-115">CommonParameters</span></span>
<span data-ttu-id="7954e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7954e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7954e-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7954e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7954e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7954e-118">INPUTS</span></span>

## <span data-ttu-id="7954e-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7954e-119">OUTPUTS</span></span>

## <span data-ttu-id="7954e-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7954e-120">NOTES</span></span>

## <span data-ttu-id="7954e-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7954e-121">RELATED LINKS</span></span>

