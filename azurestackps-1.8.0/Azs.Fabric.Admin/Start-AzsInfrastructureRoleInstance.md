---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934606"
---
# <span data-ttu-id="2de31-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="2de31-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="2de31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de31-102">SYNOPSIS</span></span>
<span data-ttu-id="2de31-103">Altyapı rolü örneğindeki güç.</span><span class="sxs-lookup"><span data-stu-id="2de31-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="2de31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2de31-104">SYNTAX</span></span>

### <span data-ttu-id="2de31-105">PowerOn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2de31-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de31-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2de31-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2de31-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2de31-107">DESCRIPTION</span></span>
<span data-ttu-id="2de31-108">Altyapı rolü örneğindeki güç.</span><span class="sxs-lookup"><span data-stu-id="2de31-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="2de31-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2de31-109">EXAMPLES</span></span>

### <span data-ttu-id="2de31-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="2de31-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="2de31-111">Altyapı rolü örneğindeki güç.</span><span class="sxs-lookup"><span data-stu-id="2de31-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="2de31-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2de31-112">PARAMETERS</span></span>

### <span data-ttu-id="2de31-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2de31-113">-Name</span></span>
<span data-ttu-id="2de31-114">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="2de31-114">Name of the infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de31-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="2de31-115">-Location</span></span>
<span data-ttu-id="2de31-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2de31-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de31-117">-ResourceGroupName</span></span>
<span data-ttu-id="2de31-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2de31-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de31-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2de31-119">-ResourceId</span></span>
<span data-ttu-id="2de31-120">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2de31-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="2de31-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="2de31-121">-AsJob</span></span>
<span data-ttu-id="2de31-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="2de31-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2de31-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2de31-123">-Force</span></span>
<span data-ttu-id="2de31-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="2de31-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2de31-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de31-125">-WhatIf</span></span>
<span data-ttu-id="2de31-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de31-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de31-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2de31-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de31-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="2de31-128">-Confirm</span></span>
<span data-ttu-id="2de31-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2de31-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de31-130">CommonParameters</span></span>
<span data-ttu-id="2de31-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2de31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de31-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de31-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de31-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2de31-133">INPUTS</span></span>

## <span data-ttu-id="2de31-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2de31-134">OUTPUTS</span></span>

## <span data-ttu-id="2de31-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2de31-135">NOTES</span></span>

## <span data-ttu-id="2de31-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2de31-136">RELATED LINKS</span></span>