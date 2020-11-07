---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: 33c833004269e26204d97b9993db93aac7389642
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917468"
---
# <span data-ttu-id="71e88-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="71e88-101">Get-AzGallery</span></span>

## <span data-ttu-id="71e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e88-102">SYNOPSIS</span></span>
<span data-ttu-id="71e88-103">Galeri alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="71e88-103">Get or list galleries.</span></span>

## <span data-ttu-id="71e88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71e88-104">SYNTAX</span></span>

### <span data-ttu-id="71e88-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="71e88-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71e88-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="71e88-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e88-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="71e88-107">DESCRIPTION</span></span>
<span data-ttu-id="71e88-108">Galeri alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="71e88-108">Get or list galleries.</span></span>

## <span data-ttu-id="71e88-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71e88-109">EXAMPLES</span></span>

### <span data-ttu-id="71e88-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="71e88-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="71e88-111">"Gallery1" galerisini edinin</span><span class="sxs-lookup"><span data-stu-id="71e88-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="71e88-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="71e88-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="71e88-113">Tüm galerileri RG1.</span><span class="sxs-lookup"><span data-stu-id="71e88-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="71e88-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="71e88-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="71e88-115">Tüm galerileri aboneliğe alın.</span><span class="sxs-lookup"><span data-stu-id="71e88-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="71e88-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="71e88-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="71e88-117">"Galeri" ile başlayan tüm galerileri tüm galerileri edinin.</span><span class="sxs-lookup"><span data-stu-id="71e88-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="71e88-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71e88-118">PARAMETERS</span></span>

### <span data-ttu-id="71e88-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e88-119">-DefaultProfile</span></span>
<span data-ttu-id="71e88-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71e88-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e88-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="71e88-121">-Name</span></span>
<span data-ttu-id="71e88-122">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="71e88-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="71e88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e88-123">-ResourceGroupName</span></span>
<span data-ttu-id="71e88-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="71e88-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="71e88-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="71e88-125">-ResourceId</span></span>
<span data-ttu-id="71e88-126">Galeri için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="71e88-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="71e88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e88-127">CommonParameters</span></span>
<span data-ttu-id="71e88-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71e88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e88-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="71e88-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e88-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71e88-130">INPUTS</span></span>

### <span data-ttu-id="71e88-131">System. String</span><span class="sxs-lookup"><span data-stu-id="71e88-131">System.String</span></span>

## <span data-ttu-id="71e88-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71e88-132">OUTPUTS</span></span>

### <span data-ttu-id="71e88-133">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="71e88-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="71e88-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71e88-134">NOTES</span></span>

## <span data-ttu-id="71e88-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71e88-135">RELATED LINKS</span></span>
