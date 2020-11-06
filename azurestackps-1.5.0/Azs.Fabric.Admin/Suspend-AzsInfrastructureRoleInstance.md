---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572449"
---
# <span data-ttu-id="1f98b-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="1f98b-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="1f98b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f98b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f98b-103">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="1f98b-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="1f98b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f98b-104">SYNTAX</span></span>

### <span data-ttu-id="1f98b-105">Kapatma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f98b-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f98b-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1f98b-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f98b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f98b-107">DESCRIPTION</span></span>
<span data-ttu-id="1f98b-108">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="1f98b-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="1f98b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f98b-109">EXAMPLES</span></span>

### <span data-ttu-id="1f98b-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1f98b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="1f98b-111">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="1f98b-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="1f98b-112">Hatada bir istisna atılır.</span><span class="sxs-lookup"><span data-stu-id="1f98b-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="1f98b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f98b-113">PARAMETERS</span></span>

### <span data-ttu-id="1f98b-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="1f98b-114">-AsJob</span></span>
<span data-ttu-id="1f98b-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="1f98b-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1f98b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1f98b-116">-Force</span></span>
<span data-ttu-id="1f98b-117">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="1f98b-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="1f98b-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="1f98b-118">-Location</span></span>
<span data-ttu-id="1f98b-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1f98b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1f98b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f98b-120">-Name</span></span>
<span data-ttu-id="1f98b-121">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="1f98b-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="1f98b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f98b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f98b-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1f98b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1f98b-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1f98b-124">-ResourceId</span></span>
<span data-ttu-id="1f98b-125">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1f98b-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="1f98b-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f98b-126">-Confirm</span></span>
<span data-ttu-id="1f98b-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f98b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f98b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f98b-128">-WhatIf</span></span>
<span data-ttu-id="1f98b-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f98b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f98b-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f98b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f98b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f98b-131">CommonParameters</span></span>
<span data-ttu-id="1f98b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f98b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f98b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f98b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f98b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f98b-134">INPUTS</span></span>

## <span data-ttu-id="1f98b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f98b-135">OUTPUTS</span></span>

## <span data-ttu-id="1f98b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f98b-136">NOTES</span></span>

## <span data-ttu-id="1f98b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f98b-137">RELATED LINKS</span></span>

