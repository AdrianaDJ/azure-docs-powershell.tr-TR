---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934609"
---
# <span data-ttu-id="0766b-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="0766b-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="0766b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0766b-102">SYNOPSIS</span></span>
<span data-ttu-id="0766b-103">Altyapı rolü örneğini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="0766b-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="0766b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0766b-104">SYNTAX</span></span>

### <span data-ttu-id="0766b-105">Yeniden Başlat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0766b-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0766b-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="0766b-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0766b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0766b-107">DESCRIPTION</span></span>
<span data-ttu-id="0766b-108">Altyapı rolü örneğini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="0766b-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="0766b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0766b-109">EXAMPLES</span></span>

### <span data-ttu-id="0766b-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="0766b-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="0766b-111">Altyapı rolü örneğini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="0766b-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="0766b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0766b-112">PARAMETERS</span></span>

### <span data-ttu-id="0766b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0766b-113">-Name</span></span>
<span data-ttu-id="0766b-114">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="0766b-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="0766b-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="0766b-115">-Location</span></span>
<span data-ttu-id="0766b-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="0766b-116">Location of the resource.</span></span>

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

### <span data-ttu-id="0766b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0766b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0766b-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="0766b-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0766b-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0766b-119">-ResourceId</span></span>
<span data-ttu-id="0766b-120">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0766b-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="0766b-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="0766b-121">-AsJob</span></span>
<span data-ttu-id="0766b-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="0766b-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0766b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0766b-123">-Force</span></span>
<span data-ttu-id="0766b-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="0766b-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0766b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0766b-125">-WhatIf</span></span>
<span data-ttu-id="0766b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0766b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0766b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0766b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0766b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0766b-128">-Confirm</span></span>
<span data-ttu-id="0766b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0766b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0766b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0766b-130">CommonParameters</span></span>
<span data-ttu-id="0766b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0766b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0766b-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0766b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0766b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0766b-133">INPUTS</span></span>

## <span data-ttu-id="0766b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0766b-134">OUTPUTS</span></span>

## <span data-ttu-id="0766b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0766b-135">NOTES</span></span>

## <span data-ttu-id="0766b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0766b-136">RELATED LINKS</span></span>
