---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6e7801a2188fe80577bc6cef9315069b0207f91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571982"
---
# <span data-ttu-id="bb070-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="bb070-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="bb070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb070-102">SYNOPSIS</span></span>
<span data-ttu-id="bb070-103">Altyapı rolü örneğini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="bb070-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="bb070-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb070-104">SYNTAX</span></span>

### <span data-ttu-id="bb070-105">Yeniden Başlat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb070-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb070-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bb070-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb070-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb070-107">DESCRIPTION</span></span>
<span data-ttu-id="bb070-108">Altyapı rolü örneğini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="bb070-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="bb070-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb070-109">EXAMPLES</span></span>

### <span data-ttu-id="bb070-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bb070-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="bb070-111">Altyapı rolü örneğini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="bb070-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="bb070-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb070-112">PARAMETERS</span></span>

### <span data-ttu-id="bb070-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="bb070-113">-AsJob</span></span>
<span data-ttu-id="bb070-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="bb070-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bb070-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bb070-115">-Force</span></span>
<span data-ttu-id="bb070-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="bb070-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bb070-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="bb070-117">-Location</span></span>
<span data-ttu-id="bb070-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="bb070-118">Location of the resource.</span></span>

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

### <span data-ttu-id="bb070-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb070-119">-Name</span></span>
<span data-ttu-id="bb070-120">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="bb070-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="bb070-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb070-121">-ResourceGroupName</span></span>
<span data-ttu-id="bb070-122">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bb070-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bb070-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb070-123">-ResourceId</span></span>
<span data-ttu-id="bb070-124">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bb070-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="bb070-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb070-125">-Confirm</span></span>
<span data-ttu-id="bb070-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb070-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb070-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb070-127">-WhatIf</span></span>
<span data-ttu-id="bb070-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb070-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb070-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb070-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb070-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb070-130">CommonParameters</span></span>
<span data-ttu-id="bb070-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb070-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb070-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb070-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb070-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb070-133">INPUTS</span></span>

## <span data-ttu-id="bb070-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb070-134">OUTPUTS</span></span>

## <span data-ttu-id="bb070-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb070-135">NOTES</span></span>

## <span data-ttu-id="bb070-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb070-136">RELATED LINKS</span></span>

