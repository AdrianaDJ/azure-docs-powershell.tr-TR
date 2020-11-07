---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935117"
---
# <span data-ttu-id="76fb2-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="76fb2-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="76fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="76fb2-103">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="76fb2-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="76fb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76fb2-104">SYNTAX</span></span>

### <span data-ttu-id="76fb2-105">Güç kapalı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76fb2-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fb2-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="76fb2-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76fb2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76fb2-107">DESCRIPTION</span></span>
<span data-ttu-id="76fb2-108">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="76fb2-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="76fb2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76fb2-109">EXAMPLES</span></span>

### <span data-ttu-id="76fb2-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="76fb2-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="76fb2-111">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="76fb2-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="76fb2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76fb2-112">PARAMETERS</span></span>

### <span data-ttu-id="76fb2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="76fb2-113">-Name</span></span>
<span data-ttu-id="76fb2-114">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="76fb2-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fb2-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="76fb2-115">-Location</span></span>
<span data-ttu-id="76fb2-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="76fb2-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fb2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fb2-117">-ResourceGroupName</span></span>
<span data-ttu-id="76fb2-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="76fb2-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fb2-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="76fb2-119">-ResourceId</span></span>
<span data-ttu-id="76fb2-120">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="76fb2-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="76fb2-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="76fb2-121">-AsJob</span></span>
<span data-ttu-id="76fb2-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="76fb2-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="76fb2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="76fb2-123">-Force</span></span>
<span data-ttu-id="76fb2-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="76fb2-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="76fb2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76fb2-125">-WhatIf</span></span>
<span data-ttu-id="76fb2-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76fb2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76fb2-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76fb2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76fb2-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="76fb2-128">-Confirm</span></span>
<span data-ttu-id="76fb2-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76fb2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76fb2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fb2-130">CommonParameters</span></span>
<span data-ttu-id="76fb2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76fb2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fb2-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76fb2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fb2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76fb2-133">INPUTS</span></span>

## <span data-ttu-id="76fb2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76fb2-134">OUTPUTS</span></span>

## <span data-ttu-id="76fb2-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76fb2-135">NOTES</span></span>

## <span data-ttu-id="76fb2-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76fb2-136">RELATED LINKS</span></span>
