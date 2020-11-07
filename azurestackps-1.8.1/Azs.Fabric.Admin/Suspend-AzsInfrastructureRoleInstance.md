---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935165"
---
# <span data-ttu-id="a9661-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a9661-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="a9661-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9661-102">SYNOPSIS</span></span>
<span data-ttu-id="a9661-103">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="a9661-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="a9661-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9661-104">SYNTAX</span></span>

### <span data-ttu-id="a9661-105">Kapatma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9661-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9661-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a9661-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9661-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9661-107">DESCRIPTION</span></span>
<span data-ttu-id="a9661-108">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="a9661-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="a9661-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9661-109">EXAMPLES</span></span>

### <span data-ttu-id="a9661-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a9661-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="a9661-111">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="a9661-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="a9661-112">Hatada bir istisna atılır.</span><span class="sxs-lookup"><span data-stu-id="a9661-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="a9661-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9661-113">PARAMETERS</span></span>

### <span data-ttu-id="a9661-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9661-114">-Name</span></span>
<span data-ttu-id="a9661-115">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="a9661-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="a9661-116">-Location</span></span>
<span data-ttu-id="a9661-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="a9661-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9661-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9661-119">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a9661-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a9661-120">-ResourceId</span></span>
<span data-ttu-id="a9661-121">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a9661-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="a9661-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="a9661-122">-AsJob</span></span>
<span data-ttu-id="a9661-123">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="a9661-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a9661-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a9661-124">-Force</span></span>
<span data-ttu-id="a9661-125">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="a9661-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="a9661-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9661-126">-WhatIf</span></span>
<span data-ttu-id="a9661-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9661-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9661-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9661-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9661-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9661-129">-Confirm</span></span>
<span data-ttu-id="a9661-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9661-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9661-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9661-131">CommonParameters</span></span>
<span data-ttu-id="a9661-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9661-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9661-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9661-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9661-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9661-134">INPUTS</span></span>

## <span data-ttu-id="a9661-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9661-135">OUTPUTS</span></span>

## <span data-ttu-id="a9661-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9661-136">NOTES</span></span>

## <span data-ttu-id="a9661-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9661-137">RELATED LINKS</span></span>
