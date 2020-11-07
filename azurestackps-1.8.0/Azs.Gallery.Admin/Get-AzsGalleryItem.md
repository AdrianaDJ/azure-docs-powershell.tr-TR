---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934712"
---
# <span data-ttu-id="0ea69-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="0ea69-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="0ea69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea69-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea69-103">Galeri öğelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="0ea69-103">Lists gallery items.</span></span>

## <span data-ttu-id="0ea69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ea69-104">SYNTAX</span></span>

### <span data-ttu-id="0ea69-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ea69-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="0ea69-106">Al</span><span class="sxs-lookup"><span data-stu-id="0ea69-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="0ea69-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ea69-107">DESCRIPTION</span></span>
<span data-ttu-id="0ea69-108">Azure yığını marketi 'nde kullanılabilen Galeri öğelerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="0ea69-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="0ea69-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ea69-109">EXAMPLES</span></span>

### <span data-ttu-id="0ea69-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="0ea69-110">EXAMPLE 1</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="0ea69-111">Liste Galerisi öğeleri.</span><span class="sxs-lookup"><span data-stu-id="0ea69-111">List gallery items.</span></span>

### <span data-ttu-id="0ea69-112">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="0ea69-112">EXAMPLE 2</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="0ea69-113">Bir galeri öğesini ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="0ea69-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="0ea69-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ea69-114">PARAMETERS</span></span>

### <span data-ttu-id="0ea69-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ea69-115">-Name</span></span>
<span data-ttu-id="0ea69-116">Galeri öğesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="0ea69-116">Identity of the gallery item.</span></span>
<span data-ttu-id="0ea69-117">Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0ea69-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="0ea69-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea69-118">CommonParameters</span></span>
<span data-ttu-id="0ea69-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ea69-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea69-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea69-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea69-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ea69-121">INPUTS</span></span>

## <span data-ttu-id="0ea69-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ea69-122">OUTPUTS</span></span>

### <span data-ttu-id="0ea69-123">Microsoft. AzureStack. Management. Gallery. admin. modeller. GALLERYITEM</span><span class="sxs-lookup"><span data-stu-id="0ea69-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="0ea69-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ea69-124">NOTES</span></span>

## <span data-ttu-id="0ea69-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ea69-125">RELATED LINKS</span></span>
