---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
ms.openlocfilehash: 5d8ed5a26e141d0ae8d6eb7494a76d8c53590d29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763878"
---
# <span data-ttu-id="d227e-101">Update-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="d227e-101">Update-AzureRmGallery</span></span>

## <span data-ttu-id="d227e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d227e-102">SYNOPSIS</span></span>
<span data-ttu-id="d227e-103">Galeriyi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d227e-103">Update a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d227e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d227e-104">SYNTAX</span></span>

### <span data-ttu-id="d227e-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d227e-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d227e-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="d227e-106">ResourceIdParameter</span></span>
```
Update-AzureRmGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d227e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d227e-107">ObjectParameter</span></span>
```
Update-AzureRmGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d227e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d227e-108">DESCRIPTION</span></span>
<span data-ttu-id="d227e-109">Galeriyi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d227e-109">Update a gallery.</span></span>

## <span data-ttu-id="d227e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d227e-110">EXAMPLES</span></span>

### <span data-ttu-id="d227e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d227e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="d227e-112">Galeriyi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d227e-112">Update a gallery.</span></span>

## <span data-ttu-id="d227e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d227e-113">PARAMETERS</span></span>

### <span data-ttu-id="d227e-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d227e-114">-AsJob</span></span>
<span data-ttu-id="d227e-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d227e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d227e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d227e-116">-DefaultProfile</span></span>
<span data-ttu-id="d227e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d227e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227e-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d227e-118">-Description</span></span>
<span data-ttu-id="d227e-119">Galeri kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="d227e-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="d227e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d227e-120">-InputObject</span></span>
<span data-ttu-id="d227e-121">PS Galerisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d227e-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="d227e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d227e-122">-Name</span></span>
<span data-ttu-id="d227e-123">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="d227e-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="d227e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d227e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d227e-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d227e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d227e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d227e-126">-ResourceId</span></span>
<span data-ttu-id="d227e-127">Galeri için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d227e-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="d227e-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d227e-128">-Tag</span></span>
<span data-ttu-id="d227e-129">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="d227e-129">Resource tags</span></span>

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

### <span data-ttu-id="d227e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d227e-130">-Confirm</span></span>
<span data-ttu-id="d227e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d227e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d227e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d227e-132">-WhatIf</span></span>
<span data-ttu-id="d227e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d227e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d227e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d227e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d227e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d227e-135">CommonParameters</span></span>
<span data-ttu-id="d227e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d227e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d227e-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d227e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d227e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d227e-138">INPUTS</span></span>

### <span data-ttu-id="d227e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d227e-139">System.String</span></span>

### <span data-ttu-id="d227e-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="d227e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="d227e-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d227e-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d227e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d227e-142">OUTPUTS</span></span>

### <span data-ttu-id="d227e-143">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="d227e-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="d227e-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d227e-144">NOTES</span></span>

## <span data-ttu-id="d227e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d227e-145">RELATED LINKS</span></span>
