---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107166"
---
# <span data-ttu-id="9f79d-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="9f79d-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="9f79d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f79d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f79d-103">Verilen konumda depolama kotaları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f79d-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="9f79d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f79d-104">SYNTAX</span></span>

### <span data-ttu-id="9f79d-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f79d-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9f79d-106">Al</span><span class="sxs-lookup"><span data-stu-id="9f79d-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="9f79d-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="9f79d-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9f79d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f79d-108">DESCRIPTION</span></span>
<span data-ttu-id="9f79d-109">Verilen konumda depolama kotaları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f79d-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="9f79d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f79d-110">EXAMPLES</span></span>

### <span data-ttu-id="9f79d-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="9f79d-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="9f79d-112">Depolama kotaları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="9f79d-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="9f79d-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="9f79d-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="9f79d-114">Belirtilen depolama kotasının ayrıntılarını ada göre edinin.</span><span class="sxs-lookup"><span data-stu-id="9f79d-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="9f79d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f79d-115">PARAMETERS</span></span>

### <span data-ttu-id="9f79d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f79d-116">-Name</span></span>
<span data-ttu-id="9f79d-117">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="9f79d-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="9f79d-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="9f79d-118">-Location</span></span>
<span data-ttu-id="9f79d-119">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="9f79d-119">Resource location.</span></span>

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

### <span data-ttu-id="9f79d-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f79d-120">-ResourceId</span></span>
<span data-ttu-id="9f79d-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9f79d-121">The resource id.</span></span>

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

### <span data-ttu-id="9f79d-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="9f79d-122">-Skip</span></span>
<span data-ttu-id="9f79d-123">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="9f79d-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9f79d-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="9f79d-124">-Top</span></span>
<span data-ttu-id="9f79d-125">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="9f79d-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9f79d-126">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="9f79d-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9f79d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f79d-127">CommonParameters</span></span>
<span data-ttu-id="9f79d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f79d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f79d-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f79d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f79d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f79d-130">INPUTS</span></span>

## <span data-ttu-id="9f79d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f79d-131">OUTPUTS</span></span>

### <span data-ttu-id="9f79d-132">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="9f79d-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="9f79d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f79d-133">NOTES</span></span>

## <span data-ttu-id="9f79d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f79d-134">RELATED LINKS</span></span>
