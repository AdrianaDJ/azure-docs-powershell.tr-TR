---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935163"
---
# <span data-ttu-id="334ee-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="334ee-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="334ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="334ee-102">SYNOPSIS</span></span>
<span data-ttu-id="334ee-103">Sağlayıcıya sağlayıcı Galerisi öğesi yükler.</span><span class="sxs-lookup"><span data-stu-id="334ee-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="334ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="334ee-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="334ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="334ee-105">DESCRIPTION</span></span>
<span data-ttu-id="334ee-106">Sağlayıcıya sağlayıcı Galerisi öğesi yükler.</span><span class="sxs-lookup"><span data-stu-id="334ee-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="334ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="334ee-107">EXAMPLES</span></span>

### <span data-ttu-id="334ee-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="334ee-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="334ee-109">Yeni galeri öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="334ee-109">Create a new gallery item.</span></span>

## <span data-ttu-id="334ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="334ee-110">PARAMETERS</span></span>

### <span data-ttu-id="334ee-111">-Gallergıuri</span><span class="sxs-lookup"><span data-stu-id="334ee-111">-GalleryItemUri</span></span>
<span data-ttu-id="334ee-112">Galeri öğesi JSON dosyasının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="334ee-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="334ee-113">-Force</span><span class="sxs-lookup"><span data-stu-id="334ee-113">-Force</span></span>
<span data-ttu-id="334ee-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="334ee-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334ee-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="334ee-115">-WhatIf</span></span>
<span data-ttu-id="334ee-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="334ee-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="334ee-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="334ee-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334ee-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="334ee-118">-Confirm</span></span>
<span data-ttu-id="334ee-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="334ee-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334ee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334ee-120">CommonParameters</span></span>
<span data-ttu-id="334ee-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="334ee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334ee-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334ee-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334ee-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="334ee-123">INPUTS</span></span>

## <span data-ttu-id="334ee-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="334ee-124">OUTPUTS</span></span>

### <span data-ttu-id="334ee-125">Microsoft. AzureStack. Management. Gallery. admin. modeller. GALLERYITEM</span><span class="sxs-lookup"><span data-stu-id="334ee-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="334ee-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="334ee-126">NOTES</span></span>

## <span data-ttu-id="334ee-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="334ee-127">RELATED LINKS</span></span>
