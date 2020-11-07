---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933925"
---
# <span data-ttu-id="34ea5-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="34ea5-101">Get-AzsDisk</span></span>

## <span data-ttu-id="34ea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="34ea5-103">Belirtilen paylaşıma geçirilebileceğiniz yönetilen disklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="34ea5-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="34ea5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34ea5-104">SYNTAX</span></span>

### <span data-ttu-id="34ea5-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34ea5-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="34ea5-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="34ea5-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="34ea5-107">Al</span><span class="sxs-lookup"><span data-stu-id="34ea5-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="34ea5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34ea5-108">DESCRIPTION</span></span>
<span data-ttu-id="34ea5-109">Disklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="34ea5-109">Returns a list of disks.</span></span>

## <span data-ttu-id="34ea5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34ea5-110">EXAMPLES</span></span>

### <span data-ttu-id="34ea5-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="34ea5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="34ea5-112">Yerel konumda yönetilen disklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="34ea5-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="34ea5-113">Varsayılan olarak, ilk 100 disk olur</span><span class="sxs-lookup"><span data-stu-id="34ea5-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="34ea5-114">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="34ea5-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="34ea5-115">Belirli bir yönetilen disk edinin.</span><span class="sxs-lookup"><span data-stu-id="34ea5-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="34ea5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34ea5-116">PARAMETERS</span></span>

### <span data-ttu-id="34ea5-117">-Sayı</span><span class="sxs-lookup"><span data-stu-id="34ea5-117">-Count</span></span>
<span data-ttu-id="34ea5-118">Döndürülecek en fazla disk sayısı.</span><span class="sxs-lookup"><span data-stu-id="34ea5-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ea5-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="34ea5-119">-Location</span></span>
<span data-ttu-id="34ea5-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="34ea5-120">Location of the resource.</span></span>

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

### <span data-ttu-id="34ea5-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="34ea5-121">-Name</span></span>
<span data-ttu-id="34ea5-122">Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="34ea5-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ea5-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34ea5-123">-ResourceId</span></span>
<span data-ttu-id="34ea5-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="34ea5-124">The resource id.</span></span>

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

### <span data-ttu-id="34ea5-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="34ea5-125">-SharePath</span></span>
<span data-ttu-id="34ea5-126">Kaynağın ait olduğu kaynak paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="34ea5-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="34ea5-127">-Başlangıç</span><span class="sxs-lookup"><span data-stu-id="34ea5-127">-Start</span></span>
<span data-ttu-id="34ea5-128">Sorgudaki disklerin başlangıç dizini.</span><span class="sxs-lookup"><span data-stu-id="34ea5-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ea5-129">-Durum</span><span class="sxs-lookup"><span data-stu-id="34ea5-129">-Status</span></span>
<span data-ttu-id="34ea5-130">Disk durumunun parametreleri.</span><span class="sxs-lookup"><span data-stu-id="34ea5-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="34ea5-131">-Usersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="34ea5-131">-UserSubscriptionId</span></span>
<span data-ttu-id="34ea5-132">Kaynağın ait olduğu kiracı aboneliği kimliği.</span><span class="sxs-lookup"><span data-stu-id="34ea5-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="34ea5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ea5-133">CommonParameters</span></span>
<span data-ttu-id="34ea5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34ea5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ea5-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ea5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ea5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34ea5-136">INPUTS</span></span>

## <span data-ttu-id="34ea5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34ea5-137">OUTPUTS</span></span>

### <span data-ttu-id="34ea5-138">Microsoft. AzureStack. Management. COMPUTE. admin. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="34ea5-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="34ea5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34ea5-139">NOTES</span></span>

## <span data-ttu-id="34ea5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34ea5-140">RELATED LINKS</span></span>

