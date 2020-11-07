---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934550"
---
# <span data-ttu-id="023d6-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="023d6-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="023d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="023d6-102">SYNOPSIS</span></span>
<span data-ttu-id="023d6-103">Belirli bir görüntü yapılandırmasından sanal makine platformu resmi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="023d6-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="023d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="023d6-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="023d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="023d6-105">DESCRIPTION</span></span>
<span data-ttu-id="023d6-106">Bir platform görüntüsü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="023d6-106">Add a platform image.</span></span>

## <span data-ttu-id="023d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="023d6-107">EXAMPLES</span></span>

### <span data-ttu-id="023d6-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="023d6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="023d6-109">Yeni bir platform görüntüsü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="023d6-109">Add a new platform image.</span></span>

## <span data-ttu-id="023d6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="023d6-110">PARAMETERS</span></span>

### <span data-ttu-id="023d6-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="023d6-111">-AsJob</span></span>
<span data-ttu-id="023d6-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="023d6-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-113">-Billingpartnumarası</span><span class="sxs-lookup"><span data-stu-id="023d6-113">-BillingPartNumber</span></span>
<span data-ttu-id="023d6-114">Bölüm numarası, Yazılım maliyetlerini faturalamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="023d6-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-115">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="023d6-115">-DataDisks</span></span>
<span data-ttu-id="023d6-116">Platform görüntüsü tarafından kullanılan veri diskleri.</span><span class="sxs-lookup"><span data-stu-id="023d6-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="023d6-117">-Force</span></span>
<span data-ttu-id="023d6-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="023d6-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="023d6-119">-Location</span></span>
<span data-ttu-id="023d6-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="023d6-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-121">-Teklif</span><span class="sxs-lookup"><span data-stu-id="023d6-121">-Offer</span></span>
<span data-ttu-id="023d6-122">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="023d6-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="023d6-123">-OsType</span></span>
<span data-ttu-id="023d6-124">İşletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="023d6-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="023d6-125">-OsUri</span></span>
<span data-ttu-id="023d6-126">Diskin konumu.</span><span class="sxs-lookup"><span data-stu-id="023d6-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="023d6-127">-Publisher</span></span>
<span data-ttu-id="023d6-128">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="023d6-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="023d6-129">-Sku</span></span>
<span data-ttu-id="023d6-130">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="023d6-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-131">-Version</span><span class="sxs-lookup"><span data-stu-id="023d6-131">-Version</span></span>
<span data-ttu-id="023d6-132">Sanal makine platformu görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="023d6-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="023d6-133">-Confirm</span></span>
<span data-ttu-id="023d6-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="023d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="023d6-135">-WhatIf</span></span>
<span data-ttu-id="023d6-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="023d6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="023d6-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="023d6-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="023d6-138">CommonParameters</span></span>
<span data-ttu-id="023d6-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="023d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="023d6-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="023d6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="023d6-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="023d6-141">INPUTS</span></span>

## <span data-ttu-id="023d6-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="023d6-142">OUTPUTS</span></span>

### <span data-ttu-id="023d6-143">Plaformımageobject</span><span class="sxs-lookup"><span data-stu-id="023d6-143">PlatformImageObject</span></span>

## <span data-ttu-id="023d6-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="023d6-144">NOTES</span></span>

## <span data-ttu-id="023d6-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="023d6-145">RELATED LINKS</span></span>

