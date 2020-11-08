---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106601"
---
# <span data-ttu-id="5038f-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="5038f-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="5038f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5038f-102">SYNOPSIS</span></span>
<span data-ttu-id="5038f-103">Belirli bir görüntü yapılandırmasından sanal makine platformu resmi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5038f-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="5038f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5038f-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5038f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5038f-105">DESCRIPTION</span></span>
<span data-ttu-id="5038f-106">Bir platform görüntüsü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5038f-106">Add a platform image.</span></span>

## <span data-ttu-id="5038f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5038f-107">EXAMPLES</span></span>

### <span data-ttu-id="5038f-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5038f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="5038f-109">Yeni bir platform görüntüsü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5038f-109">Add a new platform image.</span></span>

## <span data-ttu-id="5038f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5038f-110">PARAMETERS</span></span>

### <span data-ttu-id="5038f-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="5038f-111">-AsJob</span></span>
<span data-ttu-id="5038f-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="5038f-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5038f-113">-Billingpartnumarası</span><span class="sxs-lookup"><span data-stu-id="5038f-113">-BillingPartNumber</span></span>
<span data-ttu-id="5038f-114">Bölüm numarası, Yazılım maliyetlerini faturalamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5038f-114">The part number is used to bill for software costs.</span></span>

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

### <span data-ttu-id="5038f-115">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="5038f-115">-DataDisks</span></span>
<span data-ttu-id="5038f-116">Platform görüntüsü tarafından kullanılan veri diskleri.</span><span class="sxs-lookup"><span data-stu-id="5038f-116">Data disks used by the platform image.</span></span>

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

### <span data-ttu-id="5038f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5038f-117">-Force</span></span>
<span data-ttu-id="5038f-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="5038f-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5038f-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="5038f-119">-Location</span></span>
<span data-ttu-id="5038f-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="5038f-120">Location of the resource.</span></span>

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

### <span data-ttu-id="5038f-121">-Teklif</span><span class="sxs-lookup"><span data-stu-id="5038f-121">-Offer</span></span>
<span data-ttu-id="5038f-122">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="5038f-122">Name of the offer.</span></span>

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

### <span data-ttu-id="5038f-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="5038f-123">-OsType</span></span>
<span data-ttu-id="5038f-124">İşletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="5038f-124">Operating system type.</span></span>

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

### <span data-ttu-id="5038f-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="5038f-125">-OsUri</span></span>
<span data-ttu-id="5038f-126">Diskin konumu.</span><span class="sxs-lookup"><span data-stu-id="5038f-126">Location of the disk.</span></span>

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

### <span data-ttu-id="5038f-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5038f-127">-Publisher</span></span>
<span data-ttu-id="5038f-128">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="5038f-128">Name of the publisher.</span></span>

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

### <span data-ttu-id="5038f-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="5038f-129">-Sku</span></span>
<span data-ttu-id="5038f-130">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="5038f-130">Name of the SKU.</span></span>

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

### <span data-ttu-id="5038f-131">-Version</span><span class="sxs-lookup"><span data-stu-id="5038f-131">-Version</span></span>
<span data-ttu-id="5038f-132">Sanal makine platformu görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="5038f-132">The version of the virtual machine platform image.</span></span>

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

### <span data-ttu-id="5038f-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="5038f-133">-Confirm</span></span>
<span data-ttu-id="5038f-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5038f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5038f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5038f-135">-WhatIf</span></span>
<span data-ttu-id="5038f-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5038f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5038f-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5038f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5038f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5038f-138">CommonParameters</span></span>
<span data-ttu-id="5038f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5038f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5038f-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5038f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5038f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5038f-141">INPUTS</span></span>

## <span data-ttu-id="5038f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5038f-142">OUTPUTS</span></span>

### <span data-ttu-id="5038f-143">Plaformımageobject</span><span class="sxs-lookup"><span data-stu-id="5038f-143">PlatformImageObject</span></span>

## <span data-ttu-id="5038f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5038f-144">NOTES</span></span>

## <span data-ttu-id="5038f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5038f-145">RELATED LINKS</span></span>

