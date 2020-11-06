---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588560"
---
# <span data-ttu-id="373c6-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="373c6-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="373c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="373c6-102">SYNOPSIS</span></span>
<span data-ttu-id="373c6-103">Get veya LIST Galerisi görüntü sürümleri.</span><span class="sxs-lookup"><span data-stu-id="373c6-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="373c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="373c6-104">SYNTAX</span></span>

### <span data-ttu-id="373c6-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="373c6-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="373c6-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="373c6-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="373c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="373c6-107">DESCRIPTION</span></span>
<span data-ttu-id="373c6-108">Get veya LIST Galerisi görüntü sürümleri.</span><span class="sxs-lookup"><span data-stu-id="373c6-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="373c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="373c6-109">EXAMPLES</span></span>

### <span data-ttu-id="373c6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="373c6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="373c6-111">Galeri görüntüsü sürümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="373c6-111">Get the gallery image version.</span></span>

## <span data-ttu-id="373c6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="373c6-112">PARAMETERS</span></span>

### <span data-ttu-id="373c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373c6-113">-DefaultProfile</span></span>
<span data-ttu-id="373c6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="373c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="373c6-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="373c6-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="373c6-116">Çoğaltma durumunu göster.</span><span class="sxs-lookup"><span data-stu-id="373c6-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373c6-117">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="373c6-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="373c6-118">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="373c6-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373c6-119">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="373c6-119">-GalleryName</span></span>
<span data-ttu-id="373c6-120">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="373c6-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373c6-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="373c6-121">-Name</span></span>
<span data-ttu-id="373c6-122">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="373c6-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373c6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373c6-123">-ResourceGroupName</span></span>
<span data-ttu-id="373c6-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="373c6-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="373c6-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="373c6-125">-ResourceId</span></span>
<span data-ttu-id="373c6-126">Galeri görüntüsü sürümü için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="373c6-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="373c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373c6-127">CommonParameters</span></span>
<span data-ttu-id="373c6-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="373c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373c6-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="373c6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373c6-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="373c6-130">INPUTS</span></span>

### <span data-ttu-id="373c6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="373c6-131">System.String</span></span>

### <span data-ttu-id="373c6-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="373c6-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="373c6-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="373c6-133">OUTPUTS</span></span>

### <span data-ttu-id="373c6-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="373c6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="373c6-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="373c6-135">NOTES</span></span>

## <span data-ttu-id="373c6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="373c6-136">RELATED LINKS</span></span>
