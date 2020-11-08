---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937793"
---
# <span data-ttu-id="7c33d-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="7c33d-101">Update-AzGallery</span></span>

## <span data-ttu-id="7c33d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c33d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c33d-103">Galeriyi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="7c33d-103">Update a gallery.</span></span>

## <span data-ttu-id="7c33d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c33d-104">SYNTAX</span></span>

### <span data-ttu-id="7c33d-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c33d-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c33d-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="7c33d-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c33d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7c33d-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c33d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c33d-108">DESCRIPTION</span></span>
<span data-ttu-id="7c33d-109">Galeriyi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="7c33d-109">Update a gallery.</span></span>

## <span data-ttu-id="7c33d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c33d-110">EXAMPLES</span></span>

### <span data-ttu-id="7c33d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7c33d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="7c33d-112">Galeriyi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="7c33d-112">Update a gallery.</span></span>

## <span data-ttu-id="7c33d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c33d-113">PARAMETERS</span></span>

### <span data-ttu-id="7c33d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="7c33d-114">-AsJob</span></span>
<span data-ttu-id="7c33d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7c33d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c33d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c33d-116">-DefaultProfile</span></span>
<span data-ttu-id="7c33d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c33d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c33d-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7c33d-118">-Description</span></span>
<span data-ttu-id="7c33d-119">Galeri kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="7c33d-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="7c33d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c33d-120">-InputObject</span></span>
<span data-ttu-id="7c33d-121">PS Galerisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7c33d-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c33d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c33d-122">-Name</span></span>
<span data-ttu-id="7c33d-123">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="7c33d-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c33d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c33d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c33d-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7c33d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c33d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7c33d-126">-ResourceId</span></span>
<span data-ttu-id="7c33d-127">Galeri için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7c33d-127">The resource Id for the gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c33d-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7c33d-128">-Tag</span></span>
<span data-ttu-id="7c33d-129">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="7c33d-129">Resource tags</span></span>

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

### <span data-ttu-id="7c33d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7c33d-130">-Confirm</span></span>
<span data-ttu-id="7c33d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7c33d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c33d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c33d-132">-WhatIf</span></span>
<span data-ttu-id="7c33d-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c33d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c33d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7c33d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c33d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c33d-135">CommonParameters</span></span>
<span data-ttu-id="7c33d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c33d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c33d-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7c33d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c33d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c33d-138">INPUTS</span></span>

### <span data-ttu-id="7c33d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7c33d-139">System.String</span></span>

### <span data-ttu-id="7c33d-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="7c33d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="7c33d-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c33d-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c33d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c33d-142">OUTPUTS</span></span>

### <span data-ttu-id="7c33d-143">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="7c33d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="7c33d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c33d-144">NOTES</span></span>

## <span data-ttu-id="7c33d-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c33d-145">RELATED LINKS</span></span>