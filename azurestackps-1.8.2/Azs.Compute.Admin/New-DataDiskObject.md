---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106787"
---
# <span data-ttu-id="5d0b6-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="5d0b6-101">New-DataDiskObject</span></span>

## <span data-ttu-id="5d0b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0b6-103">Yeni bir sanal makine platformu görüntüsü oluşturmak için kullanılan bir veri diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d0b6-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="5d0b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d0b6-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="5d0b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d0b6-105">DESCRIPTION</span></span>
<span data-ttu-id="5d0b6-106">Veri diski hakkında nesne içeren bir bilgi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d0b6-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="5d0b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d0b6-107">EXAMPLES</span></span>

### <span data-ttu-id="5d0b6-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5d0b6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="5d0b6-109">Yeni bir veri disketi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d0b6-109">Create a new data disk object.</span></span>

## <span data-ttu-id="5d0b6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d0b6-110">PARAMETERS</span></span>

### <span data-ttu-id="5d0b6-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="5d0b6-111">-Lun</span></span>
<span data-ttu-id="5d0b6-112">Mantıksal birim numarası.</span><span class="sxs-lookup"><span data-stu-id="5d0b6-112">Logical unit number.</span></span>

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

### <span data-ttu-id="5d0b6-113">-URI</span><span class="sxs-lookup"><span data-stu-id="5d0b6-113">-Uri</span></span>
<span data-ttu-id="5d0b6-114">Disk şablonunun konumu.</span><span class="sxs-lookup"><span data-stu-id="5d0b6-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="5d0b6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0b6-115">CommonParameters</span></span>
<span data-ttu-id="5d0b6-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d0b6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0b6-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d0b6-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0b6-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d0b6-118">INPUTS</span></span>

## <span data-ttu-id="5d0b6-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d0b6-119">OUTPUTS</span></span>

## <span data-ttu-id="5d0b6-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d0b6-120">NOTES</span></span>

## <span data-ttu-id="5d0b6-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d0b6-121">RELATED LINKS</span></span>

