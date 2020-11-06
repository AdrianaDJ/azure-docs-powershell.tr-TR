---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572170"
---
# <span data-ttu-id="25901-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="25901-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="25901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25901-102">SYNOPSIS</span></span>
<span data-ttu-id="25901-103">Bir konumdaki tüm yazılım yük dengeleyici örneklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="25901-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="25901-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25901-104">SYNTAX</span></span>

### <span data-ttu-id="25901-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25901-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="25901-106">Al</span><span class="sxs-lookup"><span data-stu-id="25901-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="25901-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="25901-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="25901-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="25901-108">DESCRIPTION</span></span>
<span data-ttu-id="25901-109">Bir konumdaki tüm yazılım yük dengeleyici örneklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="25901-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="25901-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25901-110">EXAMPLES</span></span>

### <span data-ttu-id="25901-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="25901-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="25901-112">Bir konuma tüm yazılım yük dengeleyici Çoğullayıcı örneklerini alın.</span><span class="sxs-lookup"><span data-stu-id="25901-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="25901-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="25901-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="25901-114">Ad verilen bir konumda belirli bir yazılım yük dengeleyici Çoğullayıcı örneği edinin.</span><span class="sxs-lookup"><span data-stu-id="25901-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="25901-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25901-115">PARAMETERS</span></span>

### <span data-ttu-id="25901-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="25901-116">-Filter</span></span>
<span data-ttu-id="25901-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="25901-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="25901-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="25901-118">-Location</span></span>
<span data-ttu-id="25901-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="25901-119">Location of the resource.</span></span>

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

### <span data-ttu-id="25901-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="25901-120">-Name</span></span>
<span data-ttu-id="25901-121">SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="25901-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="25901-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25901-122">-ResourceGroupName</span></span>
<span data-ttu-id="25901-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="25901-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="25901-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="25901-124">-ResourceId</span></span>
<span data-ttu-id="25901-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="25901-125">The resource id.</span></span>

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

### <span data-ttu-id="25901-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="25901-126">-Skip</span></span>
<span data-ttu-id="25901-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="25901-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="25901-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="25901-128">-Top</span></span>
<span data-ttu-id="25901-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="25901-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="25901-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="25901-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="25901-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25901-131">CommonParameters</span></span>
<span data-ttu-id="25901-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25901-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25901-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25901-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25901-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25901-134">INPUTS</span></span>

## <span data-ttu-id="25901-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25901-135">OUTPUTS</span></span>

### <span data-ttu-id="25901-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="25901-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="25901-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25901-137">NOTES</span></span>

## <span data-ttu-id="25901-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25901-138">RELATED LINKS</span></span>

