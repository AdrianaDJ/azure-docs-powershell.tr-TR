---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934596"
---
# <span data-ttu-id="6f8ae-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="6f8ae-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="6f8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8ae-103">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="6f8ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f8ae-104">SYNTAX</span></span>

### <span data-ttu-id="6f8ae-105">Güç kapalı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f8ae-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8ae-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="6f8ae-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f8ae-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f8ae-107">DESCRIPTION</span></span>
<span data-ttu-id="6f8ae-108">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="6f8ae-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f8ae-109">EXAMPLES</span></span>

### <span data-ttu-id="6f8ae-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="6f8ae-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="6f8ae-111">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="6f8ae-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f8ae-112">PARAMETERS</span></span>

### <span data-ttu-id="6f8ae-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f8ae-113">-Name</span></span>
<span data-ttu-id="6f8ae-114">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="6f8ae-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="6f8ae-115">-Location</span></span>
<span data-ttu-id="6f8ae-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-116">Location of the resource.</span></span>

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

### <span data-ttu-id="6f8ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f8ae-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6f8ae-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6f8ae-119">-ResourceId</span></span>
<span data-ttu-id="6f8ae-120">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="6f8ae-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="6f8ae-121">-AsJob</span></span>
<span data-ttu-id="6f8ae-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6f8ae-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6f8ae-123">-Force</span></span>
<span data-ttu-id="6f8ae-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6f8ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8ae-125">-WhatIf</span></span>
<span data-ttu-id="6f8ae-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f8ae-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8ae-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f8ae-128">-Confirm</span></span>
<span data-ttu-id="6f8ae-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8ae-130">CommonParameters</span></span>
<span data-ttu-id="6f8ae-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8ae-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8ae-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8ae-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f8ae-133">INPUTS</span></span>

## <span data-ttu-id="6f8ae-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f8ae-134">OUTPUTS</span></span>

## <span data-ttu-id="6f8ae-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f8ae-135">NOTES</span></span>

## <span data-ttu-id="6f8ae-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f8ae-136">RELATED LINKS</span></span>
