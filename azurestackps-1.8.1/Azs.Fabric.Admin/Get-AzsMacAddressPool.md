---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934966"
---
# <span data-ttu-id="74f52-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="74f52-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="74f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f52-102">SYNOPSIS</span></span>
<span data-ttu-id="74f52-103">Bir konumdaki tüm MAC adresi havuzlarının bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="74f52-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="74f52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74f52-104">SYNTAX</span></span>

### <span data-ttu-id="74f52-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74f52-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="74f52-106">Al</span><span class="sxs-lookup"><span data-stu-id="74f52-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="74f52-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="74f52-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="74f52-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="74f52-108">DESCRIPTION</span></span>
<span data-ttu-id="74f52-109">Bir konumdaki tüm MAC adresi havuzlarının bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="74f52-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="74f52-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74f52-110">EXAMPLES</span></span>

### <span data-ttu-id="74f52-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="74f52-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="74f52-112">Tüm MAC adresi havuzlarını bir konumda edinin.</span><span class="sxs-lookup"><span data-stu-id="74f52-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="74f52-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="74f52-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="74f52-114">Ad tabanlı bir konumda belirli bir MAC adresi havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="74f52-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="74f52-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74f52-115">PARAMETERS</span></span>

### <span data-ttu-id="74f52-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="74f52-116">-Name</span></span>
<span data-ttu-id="74f52-117">MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="74f52-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="74f52-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="74f52-118">-Location</span></span>
<span data-ttu-id="74f52-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="74f52-119">Location of the resource.</span></span>

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

### <span data-ttu-id="74f52-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f52-120">-ResourceGroupName</span></span>
<span data-ttu-id="74f52-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="74f52-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="74f52-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="74f52-122">-ResourceId</span></span>
<span data-ttu-id="74f52-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="74f52-123">The resource id.</span></span>

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

### <span data-ttu-id="74f52-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="74f52-124">-Filter</span></span>
<span data-ttu-id="74f52-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="74f52-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="74f52-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="74f52-126">-Skip</span></span>
<span data-ttu-id="74f52-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="74f52-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="74f52-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="74f52-128">-Top</span></span>
<span data-ttu-id="74f52-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="74f52-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="74f52-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="74f52-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="74f52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f52-131">CommonParameters</span></span>
<span data-ttu-id="74f52-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74f52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f52-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f52-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f52-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74f52-134">INPUTS</span></span>

## <span data-ttu-id="74f52-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74f52-135">OUTPUTS</span></span>

### <span data-ttu-id="74f52-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="74f52-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="74f52-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74f52-137">NOTES</span></span>

## <span data-ttu-id="74f52-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74f52-138">RELATED LINKS</span></span>
