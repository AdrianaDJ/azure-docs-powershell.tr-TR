---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934454"
---
# <span data-ttu-id="ec41f-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="ec41f-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="ec41f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec41f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec41f-103">Sağlayıcıya sağlayıcı Galerisi öğesi yükler.</span><span class="sxs-lookup"><span data-stu-id="ec41f-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="ec41f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec41f-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec41f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec41f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec41f-106">Sağlayıcıya sağlayıcı Galerisi öğesi yükler.</span><span class="sxs-lookup"><span data-stu-id="ec41f-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="ec41f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec41f-107">EXAMPLES</span></span>

### <span data-ttu-id="ec41f-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ec41f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="ec41f-109">Yeni galeri öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec41f-109">Create a new gallery item.</span></span>

## <span data-ttu-id="ec41f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec41f-110">PARAMETERS</span></span>

### <span data-ttu-id="ec41f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ec41f-111">-Force</span></span>
<span data-ttu-id="ec41f-112">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="ec41f-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ec41f-113">-Gallergıuri</span><span class="sxs-lookup"><span data-stu-id="ec41f-113">-GalleryItemUri</span></span>
<span data-ttu-id="ec41f-114">Galeri öğesi JSON dosyasının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="ec41f-114">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="ec41f-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec41f-115">-Confirm</span></span>
<span data-ttu-id="ec41f-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec41f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec41f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec41f-117">-WhatIf</span></span>
<span data-ttu-id="ec41f-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec41f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec41f-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec41f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec41f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec41f-120">CommonParameters</span></span>
<span data-ttu-id="ec41f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec41f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec41f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec41f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec41f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec41f-123">INPUTS</span></span>

## <span data-ttu-id="ec41f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec41f-124">OUTPUTS</span></span>

### <span data-ttu-id="ec41f-125">Microsoft. AzureStack. Management. Gallery. admin. modeller. GALLERYITEM</span><span class="sxs-lookup"><span data-stu-id="ec41f-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="ec41f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec41f-126">NOTES</span></span>

## <span data-ttu-id="ec41f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec41f-127">RELATED LINKS</span></span>
