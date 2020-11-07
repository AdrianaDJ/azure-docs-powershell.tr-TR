---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934950"
---
# <span data-ttu-id="db30d-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="db30d-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="db30d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db30d-102">SYNOPSIS</span></span>
<span data-ttu-id="db30d-103">Requestd altyapısı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="db30d-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="db30d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db30d-104">SYNTAX</span></span>

### <span data-ttu-id="db30d-105">Yeniden Başlat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db30d-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db30d-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="db30d-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db30d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="db30d-107">DESCRIPTION</span></span>
<span data-ttu-id="db30d-108">Requestd altyapısı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="db30d-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="db30d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db30d-109">EXAMPLES</span></span>

### <span data-ttu-id="db30d-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="db30d-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="db30d-111">Kilitlendi bir altyapı rolünü yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="db30d-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="db30d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db30d-112">PARAMETERS</span></span>

### <span data-ttu-id="db30d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="db30d-113">-Name</span></span>
<span data-ttu-id="db30d-114">Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="db30d-114">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db30d-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="db30d-115">-Location</span></span>
<span data-ttu-id="db30d-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="db30d-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db30d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db30d-117">-ResourceGroupName</span></span>
<span data-ttu-id="db30d-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="db30d-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db30d-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="db30d-119">-ResourceId</span></span>
<span data-ttu-id="db30d-120">Altyapı rolü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="db30d-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="db30d-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="db30d-121">-AsJob</span></span>
<span data-ttu-id="db30d-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="db30d-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="db30d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="db30d-123">-Force</span></span>
<span data-ttu-id="db30d-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="db30d-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="db30d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db30d-125">-WhatIf</span></span>
<span data-ttu-id="db30d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db30d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db30d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db30d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db30d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="db30d-128">-Confirm</span></span>
<span data-ttu-id="db30d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db30d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db30d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db30d-130">CommonParameters</span></span>
<span data-ttu-id="db30d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db30d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db30d-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db30d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db30d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db30d-133">INPUTS</span></span>

## <span data-ttu-id="db30d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db30d-134">OUTPUTS</span></span>

## <span data-ttu-id="db30d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db30d-135">NOTES</span></span>

## <span data-ttu-id="db30d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db30d-136">RELATED LINKS</span></span>
