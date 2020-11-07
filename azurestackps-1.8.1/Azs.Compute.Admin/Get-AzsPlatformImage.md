---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935007"
---
# <span data-ttu-id="26159-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="26159-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="26159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26159-102">SYNOPSIS</span></span>
<span data-ttu-id="26159-103">Platform görüntü deposuna yüklenen sanal makine resimlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="26159-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="26159-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26159-104">SYNTAX</span></span>

### <span data-ttu-id="26159-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26159-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="26159-106">Al</span><span class="sxs-lookup"><span data-stu-id="26159-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="26159-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="26159-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="26159-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="26159-108">DESCRIPTION</span></span>
<span data-ttu-id="26159-109">Platform resimlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="26159-109">Returns platform images.</span></span>

## <span data-ttu-id="26159-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26159-110">EXAMPLES</span></span>

### <span data-ttu-id="26159-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="26159-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="26159-112">Yerel konumdaki platform görüntü deposuna yüklenen sanal makine resimlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="26159-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="26159-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="26159-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="26159-114">Belirli bir platform görüntüsü edinin.</span><span class="sxs-lookup"><span data-stu-id="26159-114">Get a specific platform image.</span></span>

## <span data-ttu-id="26159-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26159-115">PARAMETERS</span></span>

### <span data-ttu-id="26159-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="26159-116">-Location</span></span>
<span data-ttu-id="26159-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="26159-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26159-118">-Teklif</span><span class="sxs-lookup"><span data-stu-id="26159-118">-Offer</span></span>
<span data-ttu-id="26159-119">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="26159-119">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26159-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="26159-120">-Publisher</span></span>
<span data-ttu-id="26159-121">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="26159-121">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26159-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="26159-122">-ResourceId</span></span>
<span data-ttu-id="26159-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="26159-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26159-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="26159-124">-Sku</span></span>
<span data-ttu-id="26159-125">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="26159-125">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26159-126">-Version</span><span class="sxs-lookup"><span data-stu-id="26159-126">-Version</span></span>
<span data-ttu-id="26159-127">Platform görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="26159-127">The version of the platform image.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26159-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26159-128">CommonParameters</span></span>
<span data-ttu-id="26159-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26159-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26159-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26159-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26159-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26159-131">INPUTS</span></span>

## <span data-ttu-id="26159-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26159-132">OUTPUTS</span></span>

### <span data-ttu-id="26159-133">Plaformımageobject</span><span class="sxs-lookup"><span data-stu-id="26159-133">PlatformImageObject</span></span>

## <span data-ttu-id="26159-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26159-134">NOTES</span></span>

## <span data-ttu-id="26159-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26159-135">RELATED LINKS</span></span>

