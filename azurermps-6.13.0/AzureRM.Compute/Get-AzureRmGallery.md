---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588568"
---
# <span data-ttu-id="d8231-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="d8231-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="d8231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8231-102">SYNOPSIS</span></span>
<span data-ttu-id="d8231-103">Galeri alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="d8231-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8231-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8231-104">SYNTAX</span></span>

### <span data-ttu-id="d8231-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8231-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8231-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="d8231-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8231-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8231-107">DESCRIPTION</span></span>
<span data-ttu-id="d8231-108">Galeri alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="d8231-108">Get or list galleries.</span></span>

## <span data-ttu-id="d8231-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8231-109">EXAMPLES</span></span>

### <span data-ttu-id="d8231-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8231-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

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

<span data-ttu-id="d8231-111">Galeriyi edinin.</span><span class="sxs-lookup"><span data-stu-id="d8231-111">Get the gallery.</span></span>

## <span data-ttu-id="d8231-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8231-112">PARAMETERS</span></span>

### <span data-ttu-id="d8231-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8231-113">-DefaultProfile</span></span>
<span data-ttu-id="d8231-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8231-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8231-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8231-115">-Name</span></span>
<span data-ttu-id="d8231-116">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="d8231-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8231-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8231-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8231-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d8231-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8231-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d8231-119">-ResourceId</span></span>
<span data-ttu-id="d8231-120">Galeri için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d8231-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="d8231-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8231-121">CommonParameters</span></span>
<span data-ttu-id="d8231-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8231-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8231-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8231-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8231-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8231-124">INPUTS</span></span>

### <span data-ttu-id="d8231-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d8231-125">System.String</span></span>

### <span data-ttu-id="d8231-126">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="d8231-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="d8231-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8231-127">OUTPUTS</span></span>

### <span data-ttu-id="d8231-128">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="d8231-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="d8231-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8231-129">NOTES</span></span>

## <span data-ttu-id="d8231-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8231-130">RELATED LINKS</span></span>
