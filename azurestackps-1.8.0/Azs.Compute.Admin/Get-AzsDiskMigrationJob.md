---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934673"
---
# <span data-ttu-id="4b07f-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4b07f-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="4b07f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b07f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b07f-103">Yönetilen disk geçiş işlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b07f-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="4b07f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b07f-104">SYNTAX</span></span>

### <span data-ttu-id="4b07f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b07f-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="4b07f-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4b07f-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="4b07f-107">Al</span><span class="sxs-lookup"><span data-stu-id="4b07f-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="4b07f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b07f-108">DESCRIPTION</span></span>
<span data-ttu-id="4b07f-109">Disk geçiş işlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b07f-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="4b07f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b07f-110">EXAMPLES</span></span>

### <span data-ttu-id="4b07f-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4b07f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="4b07f-112">Belirli bir yönetilen disk geçiş işi edinin.</span><span class="sxs-lookup"><span data-stu-id="4b07f-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="4b07f-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4b07f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="4b07f-114">Yerel konumda yönetilen disk geçiş işlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b07f-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="4b07f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b07f-115">PARAMETERS</span></span>

### <span data-ttu-id="4b07f-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="4b07f-116">-Location</span></span>
<span data-ttu-id="4b07f-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4b07f-117">Location of the resource.</span></span>

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

### <span data-ttu-id="4b07f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b07f-118">-Name</span></span>
<span data-ttu-id="4b07f-119">Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="4b07f-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b07f-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4b07f-120">-ResourceId</span></span>
<span data-ttu-id="4b07f-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4b07f-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b07f-122">-Durum</span><span class="sxs-lookup"><span data-stu-id="4b07f-122">-Status</span></span>
<span data-ttu-id="4b07f-123">Disk geçiş işinin parametreleri.</span><span class="sxs-lookup"><span data-stu-id="4b07f-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="4b07f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b07f-124">CommonParameters</span></span>
<span data-ttu-id="4b07f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b07f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b07f-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b07f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b07f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b07f-127">INPUTS</span></span>

## <span data-ttu-id="4b07f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b07f-128">OUTPUTS</span></span>

### <span data-ttu-id="4b07f-129">Microsoft. AzureStack. Management. COMPUTE. admin. modeller. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4b07f-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="4b07f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b07f-130">NOTES</span></span>

## <span data-ttu-id="4b07f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b07f-131">RELATED LINKS</span></span>

