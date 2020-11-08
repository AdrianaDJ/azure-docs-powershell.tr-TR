---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276243"
---
# <span data-ttu-id="c2406-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="c2406-101">New-AzGallery</span></span>

## <span data-ttu-id="c2406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2406-102">SYNOPSIS</span></span>
<span data-ttu-id="c2406-103">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c2406-103">Create a gallery.</span></span>

## <span data-ttu-id="c2406-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2406-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2406-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2406-105">DESCRIPTION</span></span>
<span data-ttu-id="c2406-106">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c2406-106">Create a gallery.</span></span>

## <span data-ttu-id="c2406-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2406-107">EXAMPLES</span></span>

### <span data-ttu-id="c2406-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c2406-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="c2406-109">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c2406-109">Create a gallery.</span></span>

## <span data-ttu-id="c2406-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2406-110">PARAMETERS</span></span>

### <span data-ttu-id="c2406-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="c2406-111">-AsJob</span></span>
<span data-ttu-id="c2406-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c2406-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2406-113">-DefaultProfile</span></span>
<span data-ttu-id="c2406-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2406-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c2406-115">-Description</span></span>
<span data-ttu-id="c2406-116">Galeri kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="c2406-116">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="c2406-117">-Location</span></span>
<span data-ttu-id="c2406-118">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="c2406-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2406-119">-Name</span></span>
<span data-ttu-id="c2406-120">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="c2406-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2406-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2406-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c2406-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c2406-123">-Tag</span></span>
<span data-ttu-id="c2406-124">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="c2406-124">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2406-125">-Confirm</span></span>
<span data-ttu-id="c2406-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2406-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2406-127">-WhatIf</span></span>
<span data-ttu-id="c2406-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2406-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2406-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2406-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2406-130">CommonParameters</span></span>
<span data-ttu-id="c2406-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2406-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2406-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c2406-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2406-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2406-133">INPUTS</span></span>

### <span data-ttu-id="c2406-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c2406-134">System.String</span></span>

### <span data-ttu-id="c2406-135">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2406-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c2406-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2406-136">OUTPUTS</span></span>

### <span data-ttu-id="c2406-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="c2406-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c2406-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2406-138">NOTES</span></span>

## <span data-ttu-id="c2406-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2406-139">RELATED LINKS</span></span>
