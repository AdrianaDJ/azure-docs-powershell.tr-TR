---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 43ff179aa11c3cf9bf4b22f8b5c938a473a9d8c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761318"
---
# <span data-ttu-id="0a758-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="0a758-101">New-AzGallery</span></span>

## <span data-ttu-id="0a758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a758-102">SYNOPSIS</span></span>
<span data-ttu-id="0a758-103">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="0a758-103">Create a gallery.</span></span>

## <span data-ttu-id="0a758-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a758-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a758-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a758-105">DESCRIPTION</span></span>
<span data-ttu-id="0a758-106">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="0a758-106">Create a gallery.</span></span>

## <span data-ttu-id="0a758-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a758-107">EXAMPLES</span></span>

### <span data-ttu-id="0a758-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0a758-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="0a758-109">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="0a758-109">Create a gallery.</span></span>

## <span data-ttu-id="0a758-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a758-110">PARAMETERS</span></span>

### <span data-ttu-id="0a758-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="0a758-111">-AsJob</span></span>
<span data-ttu-id="0a758-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0a758-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a758-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a758-113">-DefaultProfile</span></span>
<span data-ttu-id="0a758-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a758-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a758-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="0a758-115">-Description</span></span>
<span data-ttu-id="0a758-116">Galeri kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="0a758-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="0a758-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="0a758-117">-Location</span></span>
<span data-ttu-id="0a758-118">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="0a758-118">Resource location</span></span>

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

### <span data-ttu-id="0a758-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a758-119">-Name</span></span>
<span data-ttu-id="0a758-120">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="0a758-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="0a758-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a758-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a758-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0a758-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a758-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0a758-123">-Tag</span></span>
<span data-ttu-id="0a758-124">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="0a758-124">Resource tags</span></span>

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

### <span data-ttu-id="0a758-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a758-125">-Confirm</span></span>
<span data-ttu-id="0a758-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a758-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a758-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a758-127">-WhatIf</span></span>
<span data-ttu-id="0a758-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a758-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a758-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a758-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a758-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a758-130">CommonParameters</span></span>
<span data-ttu-id="0a758-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a758-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a758-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a758-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a758-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a758-133">INPUTS</span></span>

### <span data-ttu-id="0a758-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0a758-134">System.String</span></span>

### <span data-ttu-id="0a758-135">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a758-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a758-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a758-136">OUTPUTS</span></span>

### <span data-ttu-id="0a758-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="0a758-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="0a758-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a758-138">NOTES</span></span>

## <span data-ttu-id="0a758-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a758-139">RELATED LINKS</span></span>
