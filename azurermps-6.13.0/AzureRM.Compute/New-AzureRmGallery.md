---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
ms.openlocfilehash: bb743768654dcaeec9a39e7b590abe71b155cc17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764688"
---
# <span data-ttu-id="9dde9-101">New-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="9dde9-101">New-AzureRmGallery</span></span>

## <span data-ttu-id="9dde9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dde9-102">SYNOPSIS</span></span>
<span data-ttu-id="9dde9-103">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="9dde9-103">Create a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dde9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9dde9-104">SYNTAX</span></span>

```
New-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dde9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9dde9-105">DESCRIPTION</span></span>
<span data-ttu-id="9dde9-106">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="9dde9-106">Create a gallery.</span></span>

## <span data-ttu-id="9dde9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9dde9-107">EXAMPLES</span></span>

### <span data-ttu-id="9dde9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9dde9-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="9dde9-109">Galeri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="9dde9-109">Create a gallery.</span></span>

## <span data-ttu-id="9dde9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9dde9-110">PARAMETERS</span></span>

### <span data-ttu-id="9dde9-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="9dde9-111">-AsJob</span></span>
<span data-ttu-id="9dde9-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9dde9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dde9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dde9-113">-DefaultProfile</span></span>
<span data-ttu-id="9dde9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9dde9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dde9-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9dde9-115">-Description</span></span>
<span data-ttu-id="9dde9-116">Galeri kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9dde9-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="9dde9-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="9dde9-117">-Location</span></span>
<span data-ttu-id="9dde9-118">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="9dde9-118">Resource location</span></span>

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

### <span data-ttu-id="9dde9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9dde9-119">-Name</span></span>
<span data-ttu-id="9dde9-120">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="9dde9-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="9dde9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dde9-121">-ResourceGroupName</span></span>
<span data-ttu-id="9dde9-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9dde9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="9dde9-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9dde9-123">-Tag</span></span>
<span data-ttu-id="9dde9-124">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="9dde9-124">Resource tags</span></span>

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

### <span data-ttu-id="9dde9-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="9dde9-125">-Confirm</span></span>
<span data-ttu-id="9dde9-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9dde9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dde9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dde9-127">-WhatIf</span></span>
<span data-ttu-id="9dde9-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9dde9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dde9-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9dde9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dde9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dde9-130">CommonParameters</span></span>
<span data-ttu-id="9dde9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9dde9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dde9-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dde9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dde9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9dde9-133">INPUTS</span></span>

### <span data-ttu-id="9dde9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9dde9-134">System.String</span></span>

### <span data-ttu-id="9dde9-135">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9dde9-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9dde9-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9dde9-136">OUTPUTS</span></span>

### <span data-ttu-id="9dde9-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="9dde9-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="9dde9-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9dde9-138">NOTES</span></span>

## <span data-ttu-id="9dde9-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9dde9-139">RELATED LINKS</span></span>
