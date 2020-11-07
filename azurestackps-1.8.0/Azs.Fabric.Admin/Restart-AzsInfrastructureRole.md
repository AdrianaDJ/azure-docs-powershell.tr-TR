---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934601"
---
# <span data-ttu-id="ca54e-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="ca54e-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="ca54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca54e-102">SYNOPSIS</span></span>
<span data-ttu-id="ca54e-103">Requestd altyapısı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="ca54e-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="ca54e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca54e-104">SYNTAX</span></span>

### <span data-ttu-id="ca54e-105">Yeniden Başlat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca54e-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca54e-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="ca54e-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca54e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca54e-107">DESCRIPTION</span></span>
<span data-ttu-id="ca54e-108">Requestd altyapısı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="ca54e-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="ca54e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca54e-109">EXAMPLES</span></span>

### <span data-ttu-id="ca54e-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="ca54e-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="ca54e-111">Kilitlendi bir altyapı rolünü yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="ca54e-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="ca54e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca54e-112">PARAMETERS</span></span>

### <span data-ttu-id="ca54e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca54e-113">-Name</span></span>
<span data-ttu-id="ca54e-114">Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="ca54e-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="ca54e-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="ca54e-115">-Location</span></span>
<span data-ttu-id="ca54e-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="ca54e-116">Location of the resource.</span></span>

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

### <span data-ttu-id="ca54e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca54e-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca54e-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="ca54e-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ca54e-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ca54e-119">-ResourceId</span></span>
<span data-ttu-id="ca54e-120">Altyapı rolü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ca54e-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="ca54e-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="ca54e-121">-AsJob</span></span>
<span data-ttu-id="ca54e-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="ca54e-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ca54e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ca54e-123">-Force</span></span>
<span data-ttu-id="ca54e-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="ca54e-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ca54e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca54e-125">-WhatIf</span></span>
<span data-ttu-id="ca54e-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca54e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca54e-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca54e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca54e-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca54e-128">-Confirm</span></span>
<span data-ttu-id="ca54e-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca54e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca54e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca54e-130">CommonParameters</span></span>
<span data-ttu-id="ca54e-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca54e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca54e-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca54e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca54e-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca54e-133">INPUTS</span></span>

## <span data-ttu-id="ca54e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca54e-134">OUTPUTS</span></span>

## <span data-ttu-id="ca54e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca54e-135">NOTES</span></span>

## <span data-ttu-id="ca54e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca54e-136">RELATED LINKS</span></span>
