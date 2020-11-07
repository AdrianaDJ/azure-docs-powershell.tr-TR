---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a63ccb6706f4d43e890b8805af0d00aff350bc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934459"
---
# <span data-ttu-id="775b7-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="775b7-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="775b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="775b7-102">SYNOPSIS</span></span>
<span data-ttu-id="775b7-103">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="775b7-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="775b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="775b7-104">SYNTAX</span></span>

### <span data-ttu-id="775b7-105">Güç kapalı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="775b7-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="775b7-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="775b7-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="775b7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="775b7-107">DESCRIPTION</span></span>
<span data-ttu-id="775b7-108">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="775b7-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="775b7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="775b7-109">EXAMPLES</span></span>

### <span data-ttu-id="775b7-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="775b7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="775b7-111">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="775b7-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="775b7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="775b7-112">PARAMETERS</span></span>

### <span data-ttu-id="775b7-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="775b7-113">-AsJob</span></span>
<span data-ttu-id="775b7-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="775b7-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="775b7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="775b7-115">-Force</span></span>
<span data-ttu-id="775b7-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="775b7-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="775b7-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="775b7-117">-Location</span></span>
<span data-ttu-id="775b7-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="775b7-118">Location of the resource.</span></span>

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

### <span data-ttu-id="775b7-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="775b7-119">-Name</span></span>
<span data-ttu-id="775b7-120">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="775b7-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="775b7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="775b7-121">-ResourceGroupName</span></span>
<span data-ttu-id="775b7-122">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="775b7-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="775b7-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="775b7-123">-ResourceId</span></span>
<span data-ttu-id="775b7-124">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="775b7-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="775b7-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="775b7-125">-Confirm</span></span>
<span data-ttu-id="775b7-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="775b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="775b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="775b7-127">-WhatIf</span></span>
<span data-ttu-id="775b7-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="775b7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="775b7-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="775b7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="775b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775b7-130">CommonParameters</span></span>
<span data-ttu-id="775b7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="775b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775b7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="775b7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775b7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="775b7-133">INPUTS</span></span>

## <span data-ttu-id="775b7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="775b7-134">OUTPUTS</span></span>

## <span data-ttu-id="775b7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="775b7-135">NOTES</span></span>

## <span data-ttu-id="775b7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="775b7-136">RELATED LINKS</span></span>

