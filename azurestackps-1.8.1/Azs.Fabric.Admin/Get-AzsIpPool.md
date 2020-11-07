---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934970"
---
# <span data-ttu-id="f3320-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="f3320-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="f3320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3320-102">SYNOPSIS</span></span>
<span data-ttu-id="f3320-103">Belirli bir konumdaki tüm IP havuzlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f3320-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="f3320-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3320-104">SYNTAX</span></span>

### <span data-ttu-id="f3320-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f3320-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f3320-106">Al</span><span class="sxs-lookup"><span data-stu-id="f3320-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3320-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f3320-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f3320-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3320-108">DESCRIPTION</span></span>
<span data-ttu-id="f3320-109">Belirli bir konumdaki tüm IP havuzlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f3320-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="f3320-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3320-110">EXAMPLES</span></span>

### <span data-ttu-id="f3320-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="f3320-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="f3320-112">Tüm altyapı IP havuzlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="f3320-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="f3320-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="f3320-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="f3320-114">Ada dayalı bir altyapı IP havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="f3320-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="f3320-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3320-115">PARAMETERS</span></span>

### <span data-ttu-id="f3320-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3320-116">-Name</span></span>
<span data-ttu-id="f3320-117">IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="f3320-117">IP pool name.</span></span>

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

### <span data-ttu-id="f3320-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="f3320-118">-Location</span></span>
<span data-ttu-id="f3320-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f3320-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f3320-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3320-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3320-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f3320-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f3320-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f3320-122">-ResourceId</span></span>
<span data-ttu-id="f3320-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f3320-123">The resource id.</span></span>

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

### <span data-ttu-id="f3320-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="f3320-124">-Filter</span></span>
<span data-ttu-id="f3320-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="f3320-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="f3320-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="f3320-126">-Skip</span></span>
<span data-ttu-id="f3320-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="f3320-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f3320-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="f3320-128">-Top</span></span>
<span data-ttu-id="f3320-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="f3320-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f3320-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f3320-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f3320-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3320-131">CommonParameters</span></span>
<span data-ttu-id="f3320-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3320-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3320-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3320-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3320-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3320-134">INPUTS</span></span>

## <span data-ttu-id="f3320-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3320-135">OUTPUTS</span></span>

### <span data-ttu-id="f3320-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. IpPool</span><span class="sxs-lookup"><span data-stu-id="f3320-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="f3320-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3320-137">NOTES</span></span>

## <span data-ttu-id="f3320-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3320-138">RELATED LINKS</span></span>
