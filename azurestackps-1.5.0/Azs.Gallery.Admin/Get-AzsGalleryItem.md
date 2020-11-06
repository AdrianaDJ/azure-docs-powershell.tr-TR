---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571721"
---
# <span data-ttu-id="4d794-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="4d794-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="4d794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d794-102">SYNOPSIS</span></span>
<span data-ttu-id="4d794-103">Galeri öğelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="4d794-103">Lists gallery items.</span></span>

## <span data-ttu-id="4d794-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d794-104">SYNTAX</span></span>

### <span data-ttu-id="4d794-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d794-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="4d794-106">Al</span><span class="sxs-lookup"><span data-stu-id="4d794-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="4d794-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d794-107">DESCRIPTION</span></span>
<span data-ttu-id="4d794-108">Azure yığını marketi 'nde kullanılabilen Galeri öğelerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="4d794-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="4d794-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d794-109">EXAMPLES</span></span>

### <span data-ttu-id="4d794-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4d794-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="4d794-111">Liste Galerisi öğeleri.</span><span class="sxs-lookup"><span data-stu-id="4d794-111">List gallery items.</span></span>

### <span data-ttu-id="4d794-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4d794-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="4d794-113">Bir galeri öğesini ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="4d794-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="4d794-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d794-114">PARAMETERS</span></span>

### <span data-ttu-id="4d794-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d794-115">-Name</span></span>
<span data-ttu-id="4d794-116">Galeri öğesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="4d794-116">Identity of the gallery item.</span></span>
<span data-ttu-id="4d794-117">Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.</span><span class="sxs-lookup"><span data-stu-id="4d794-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d794-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d794-118">CommonParameters</span></span>
<span data-ttu-id="4d794-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d794-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d794-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d794-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d794-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d794-121">INPUTS</span></span>

## <span data-ttu-id="4d794-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d794-122">OUTPUTS</span></span>

### <span data-ttu-id="4d794-123">Microsoft. AzureStack. Management. Gallery. admin. modeller. GALLERYITEM</span><span class="sxs-lookup"><span data-stu-id="4d794-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="4d794-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d794-124">NOTES</span></span>

## <span data-ttu-id="4d794-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d794-125">RELATED LINKS</span></span>

