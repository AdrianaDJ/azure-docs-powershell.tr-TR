---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106961"
---
# <span data-ttu-id="89796-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="89796-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="89796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89796-102">SYNOPSIS</span></span>
<span data-ttu-id="89796-103">Belirli bir konumdaki tüm doku dosyası paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="89796-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="89796-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89796-104">SYNTAX</span></span>

### <span data-ttu-id="89796-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89796-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="89796-106">Al</span><span class="sxs-lookup"><span data-stu-id="89796-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="89796-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="89796-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="89796-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="89796-108">DESCRIPTION</span></span>
<span data-ttu-id="89796-109">Belirli bir konumdaki tüm doku dosyası paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="89796-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="89796-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89796-110">EXAMPLES</span></span>

### <span data-ttu-id="89796-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="89796-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="89796-112">Tüm dosya paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="89796-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="89796-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="89796-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="89796-114">Ada dayalı bir dosya paylaşımı döndürür.</span><span class="sxs-lookup"><span data-stu-id="89796-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="89796-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89796-115">PARAMETERS</span></span>

### <span data-ttu-id="89796-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="89796-116">-Name</span></span>
<span data-ttu-id="89796-117">Doku dosyası paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="89796-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="89796-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="89796-118">-Location</span></span>
<span data-ttu-id="89796-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="89796-119">Location of the resource.</span></span>

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

### <span data-ttu-id="89796-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89796-120">-ResourceGroupName</span></span>
<span data-ttu-id="89796-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="89796-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="89796-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89796-122">-ResourceId</span></span>
<span data-ttu-id="89796-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="89796-123">The resource id.</span></span>

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

### <span data-ttu-id="89796-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="89796-124">-Filter</span></span>
<span data-ttu-id="89796-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="89796-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="89796-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89796-126">CommonParameters</span></span>
<span data-ttu-id="89796-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89796-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89796-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89796-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89796-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89796-129">INPUTS</span></span>

## <span data-ttu-id="89796-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89796-130">OUTPUTS</span></span>

### <span data-ttu-id="89796-131">Microsoft. AzureStack. Management. Fabric. admin. modeller. FileShare</span><span class="sxs-lookup"><span data-stu-id="89796-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="89796-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89796-132">NOTES</span></span>

## <span data-ttu-id="89796-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89796-133">RELATED LINKS</span></span>
