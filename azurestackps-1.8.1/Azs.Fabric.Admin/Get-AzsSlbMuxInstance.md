---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821495581589eff356cd0d88fc98311b5f566d61
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934886"
---
# <span data-ttu-id="1c64e-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="1c64e-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="1c64e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c64e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c64e-103">Bir konumdaki tüm yazılım yük dengeleyici örneklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c64e-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="1c64e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c64e-104">SYNTAX</span></span>

### <span data-ttu-id="1c64e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c64e-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1c64e-106">Al</span><span class="sxs-lookup"><span data-stu-id="1c64e-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c64e-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1c64e-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1c64e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c64e-108">DESCRIPTION</span></span>
<span data-ttu-id="1c64e-109">Bir konumdaki tüm yazılım yük dengeleyici örneklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c64e-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="1c64e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c64e-110">EXAMPLES</span></span>

### <span data-ttu-id="1c64e-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="1c64e-111">EXAMPLE 1</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="1c64e-112">Bir konuma tüm yazılım yük dengeleyici Çoğullayıcı örneklerini alın.</span><span class="sxs-lookup"><span data-stu-id="1c64e-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="1c64e-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="1c64e-113">EXAMPLE 2</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="1c64e-114">Ad verilen bir konumda belirli bir yazılım yük dengeleyici Çoğullayıcı örneği edinin.</span><span class="sxs-lookup"><span data-stu-id="1c64e-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="1c64e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c64e-115">PARAMETERS</span></span>

### <span data-ttu-id="1c64e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c64e-116">-Name</span></span>
<span data-ttu-id="1c64e-117">SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="1c64e-117">Name of a SLB MUX instance.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c64e-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="1c64e-118">-Location</span></span>
<span data-ttu-id="1c64e-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1c64e-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1c64e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c64e-120">-ResourceGroupName</span></span>
<span data-ttu-id="1c64e-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1c64e-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1c64e-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1c64e-122">-ResourceId</span></span>
<span data-ttu-id="1c64e-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1c64e-123">The resource id.</span></span>

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

### <span data-ttu-id="1c64e-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="1c64e-124">-Filter</span></span>
<span data-ttu-id="1c64e-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="1c64e-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1c64e-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="1c64e-126">-Skip</span></span>
<span data-ttu-id="1c64e-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="1c64e-127">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c64e-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="1c64e-128">-Top</span></span>
<span data-ttu-id="1c64e-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="1c64e-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1c64e-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1c64e-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c64e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c64e-131">CommonParameters</span></span>
<span data-ttu-id="1c64e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c64e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c64e-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c64e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c64e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c64e-134">INPUTS</span></span>

## <span data-ttu-id="1c64e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c64e-135">OUTPUTS</span></span>

### <span data-ttu-id="1c64e-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="1c64e-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="1c64e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c64e-137">NOTES</span></span>

## <span data-ttu-id="1c64e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c64e-138">RELATED LINKS</span></span>