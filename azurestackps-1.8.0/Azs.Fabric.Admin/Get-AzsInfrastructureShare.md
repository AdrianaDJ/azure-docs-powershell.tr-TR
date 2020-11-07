---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934631"
---
# <span data-ttu-id="1ed27-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="1ed27-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="1ed27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed27-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed27-103">Belirli bir konumdaki tüm doku dosyası paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1ed27-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="1ed27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ed27-104">SYNTAX</span></span>

### <span data-ttu-id="1ed27-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ed27-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ed27-106">Al</span><span class="sxs-lookup"><span data-stu-id="1ed27-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ed27-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1ed27-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1ed27-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ed27-108">DESCRIPTION</span></span>
<span data-ttu-id="1ed27-109">Belirli bir konumdaki tüm doku dosyası paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1ed27-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="1ed27-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ed27-110">EXAMPLES</span></span>

### <span data-ttu-id="1ed27-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="1ed27-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="1ed27-112">Tüm dosya paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1ed27-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="1ed27-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="1ed27-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="1ed27-114">Ada dayalı bir dosya paylaşımı döndürür.</span><span class="sxs-lookup"><span data-stu-id="1ed27-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="1ed27-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ed27-115">PARAMETERS</span></span>

### <span data-ttu-id="1ed27-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ed27-116">-Name</span></span>
<span data-ttu-id="1ed27-117">Doku dosyası paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="1ed27-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="1ed27-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="1ed27-118">-Location</span></span>
<span data-ttu-id="1ed27-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1ed27-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1ed27-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed27-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ed27-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1ed27-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1ed27-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1ed27-122">-ResourceId</span></span>
<span data-ttu-id="1ed27-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1ed27-123">The resource id.</span></span>

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

### <span data-ttu-id="1ed27-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="1ed27-124">-Filter</span></span>
<span data-ttu-id="1ed27-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="1ed27-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1ed27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed27-126">CommonParameters</span></span>
<span data-ttu-id="1ed27-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ed27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed27-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed27-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed27-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ed27-129">INPUTS</span></span>

## <span data-ttu-id="1ed27-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ed27-130">OUTPUTS</span></span>

### <span data-ttu-id="1ed27-131">Microsoft. AzureStack. Management. Fabric. admin. modeller. FileShare</span><span class="sxs-lookup"><span data-stu-id="1ed27-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="1ed27-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ed27-132">NOTES</span></span>

## <span data-ttu-id="1ed27-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ed27-133">RELATED LINKS</span></span>
