---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935161"
---
# <span data-ttu-id="dd64f-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="dd64f-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="dd64f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd64f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd64f-103">Galeri öğelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="dd64f-103">Lists gallery items.</span></span>

## <span data-ttu-id="dd64f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd64f-104">SYNTAX</span></span>

### <span data-ttu-id="dd64f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd64f-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="dd64f-106">Al</span><span class="sxs-lookup"><span data-stu-id="dd64f-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="dd64f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd64f-107">DESCRIPTION</span></span>
<span data-ttu-id="dd64f-108">Azure yığını marketi 'nde kullanılabilen Galeri öğelerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="dd64f-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="dd64f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd64f-109">EXAMPLES</span></span>

### <span data-ttu-id="dd64f-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="dd64f-110">EXAMPLE 1</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="dd64f-111">Liste Galerisi öğeleri.</span><span class="sxs-lookup"><span data-stu-id="dd64f-111">List gallery items.</span></span>

### <span data-ttu-id="dd64f-112">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="dd64f-112">EXAMPLE 2</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="dd64f-113">Bir galeri öğesini ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="dd64f-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="dd64f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd64f-114">PARAMETERS</span></span>

### <span data-ttu-id="dd64f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd64f-115">-Name</span></span>
<span data-ttu-id="dd64f-116">Galeri öğesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="dd64f-116">Identity of the gallery item.</span></span>
<span data-ttu-id="dd64f-117">Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.</span><span class="sxs-lookup"><span data-stu-id="dd64f-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="dd64f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd64f-118">CommonParameters</span></span>
<span data-ttu-id="dd64f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd64f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd64f-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd64f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd64f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd64f-121">INPUTS</span></span>

## <span data-ttu-id="dd64f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd64f-122">OUTPUTS</span></span>

### <span data-ttu-id="dd64f-123">Microsoft. AzureStack. Management. Gallery. admin. modeller. GALLERYITEM</span><span class="sxs-lookup"><span data-stu-id="dd64f-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="dd64f-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd64f-124">NOTES</span></span>

## <span data-ttu-id="dd64f-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd64f-125">RELATED LINKS</span></span>
