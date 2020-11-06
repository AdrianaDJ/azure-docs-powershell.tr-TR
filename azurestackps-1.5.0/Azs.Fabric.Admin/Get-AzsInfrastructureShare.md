---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571462"
---
# <span data-ttu-id="97295-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="97295-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="97295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97295-102">SYNOPSIS</span></span>
<span data-ttu-id="97295-103">Belirli bir konumdaki tüm doku dosyası paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97295-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="97295-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97295-104">SYNTAX</span></span>

### <span data-ttu-id="97295-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97295-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="97295-106">Al</span><span class="sxs-lookup"><span data-stu-id="97295-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="97295-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="97295-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="97295-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97295-108">DESCRIPTION</span></span>
<span data-ttu-id="97295-109">Belirli bir konumdaki tüm doku dosyası paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97295-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="97295-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97295-110">EXAMPLES</span></span>

### <span data-ttu-id="97295-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="97295-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="97295-112">Tüm dosya paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97295-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="97295-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="97295-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="97295-114">Ada dayalı bir dosya paylaşımı döndürür.</span><span class="sxs-lookup"><span data-stu-id="97295-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="97295-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97295-115">PARAMETERS</span></span>

### <span data-ttu-id="97295-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="97295-116">-Filter</span></span>
<span data-ttu-id="97295-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="97295-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="97295-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="97295-118">-Location</span></span>
<span data-ttu-id="97295-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="97295-119">Location of the resource.</span></span>

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

### <span data-ttu-id="97295-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="97295-120">-Name</span></span>
<span data-ttu-id="97295-121">Doku dosyası paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="97295-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="97295-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97295-122">-ResourceGroupName</span></span>
<span data-ttu-id="97295-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="97295-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="97295-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97295-124">-ResourceId</span></span>
<span data-ttu-id="97295-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="97295-125">The resource id.</span></span>

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

### <span data-ttu-id="97295-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97295-126">CommonParameters</span></span>
<span data-ttu-id="97295-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97295-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97295-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97295-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97295-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97295-129">INPUTS</span></span>

## <span data-ttu-id="97295-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97295-130">OUTPUTS</span></span>

### <span data-ttu-id="97295-131">Microsoft. AzureStack. Management. Fabric. admin. modeller. FileShare</span><span class="sxs-lookup"><span data-stu-id="97295-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="97295-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97295-132">NOTES</span></span>

## <span data-ttu-id="97295-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97295-133">RELATED LINKS</span></span>

