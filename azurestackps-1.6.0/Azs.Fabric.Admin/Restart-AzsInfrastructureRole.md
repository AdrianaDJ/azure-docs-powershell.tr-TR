---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571501"
---
# <span data-ttu-id="75eda-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="75eda-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="75eda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75eda-102">SYNOPSIS</span></span>
<span data-ttu-id="75eda-103">İstenen altyapı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="75eda-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="75eda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75eda-104">SYNTAX</span></span>

### <span data-ttu-id="75eda-105">Yeniden Başlat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75eda-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75eda-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="75eda-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75eda-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="75eda-107">DESCRIPTION</span></span>
<span data-ttu-id="75eda-108">İstenen altyapı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="75eda-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="75eda-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75eda-109">EXAMPLES</span></span>

### <span data-ttu-id="75eda-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75eda-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="75eda-111">Kilitlendi bir altyapı rolünü yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="75eda-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="75eda-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75eda-112">PARAMETERS</span></span>

### <span data-ttu-id="75eda-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="75eda-113">-AsJob</span></span>
<span data-ttu-id="75eda-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="75eda-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="75eda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="75eda-115">-Force</span></span>
<span data-ttu-id="75eda-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="75eda-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="75eda-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="75eda-117">-Location</span></span>
<span data-ttu-id="75eda-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="75eda-118">Location of the resource.</span></span>

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

### <span data-ttu-id="75eda-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="75eda-119">-Name</span></span>
<span data-ttu-id="75eda-120">Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="75eda-120">Infrastructure role name.</span></span>

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

### <span data-ttu-id="75eda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75eda-121">-ResourceGroupName</span></span>
<span data-ttu-id="75eda-122">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="75eda-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="75eda-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="75eda-123">-ResourceId</span></span>
<span data-ttu-id="75eda-124">Altyapı rolü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="75eda-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="75eda-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="75eda-125">-Confirm</span></span>
<span data-ttu-id="75eda-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75eda-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75eda-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75eda-127">-WhatIf</span></span>
<span data-ttu-id="75eda-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75eda-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75eda-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75eda-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75eda-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75eda-130">CommonParameters</span></span>
<span data-ttu-id="75eda-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75eda-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75eda-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75eda-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75eda-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75eda-133">INPUTS</span></span>

## <span data-ttu-id="75eda-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75eda-134">OUTPUTS</span></span>

## <span data-ttu-id="75eda-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75eda-135">NOTES</span></span>

## <span data-ttu-id="75eda-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75eda-136">RELATED LINKS</span></span>

