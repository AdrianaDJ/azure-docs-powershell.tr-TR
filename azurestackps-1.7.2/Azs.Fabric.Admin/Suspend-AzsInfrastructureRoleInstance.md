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
ms.locfileid: "93934458"
---
# <span data-ttu-id="62539-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="62539-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="62539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62539-102">SYNOPSIS</span></span>
<span data-ttu-id="62539-103">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="62539-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="62539-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62539-104">SYNTAX</span></span>

### <span data-ttu-id="62539-105">Kapatma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62539-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62539-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="62539-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62539-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="62539-107">DESCRIPTION</span></span>
<span data-ttu-id="62539-108">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="62539-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="62539-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62539-109">EXAMPLES</span></span>

### <span data-ttu-id="62539-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="62539-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="62539-111">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="62539-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="62539-112">Hatada bir istisna atılır.</span><span class="sxs-lookup"><span data-stu-id="62539-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="62539-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62539-113">PARAMETERS</span></span>

### <span data-ttu-id="62539-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="62539-114">-AsJob</span></span>
<span data-ttu-id="62539-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="62539-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="62539-116">-Force</span><span class="sxs-lookup"><span data-stu-id="62539-116">-Force</span></span>
<span data-ttu-id="62539-117">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="62539-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="62539-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="62539-118">-Location</span></span>
<span data-ttu-id="62539-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="62539-119">Location of the resource.</span></span>

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

### <span data-ttu-id="62539-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="62539-120">-Name</span></span>
<span data-ttu-id="62539-121">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="62539-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="62539-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62539-122">-ResourceGroupName</span></span>
<span data-ttu-id="62539-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="62539-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="62539-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="62539-124">-ResourceId</span></span>
<span data-ttu-id="62539-125">Altyapı rolü örneği kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="62539-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="62539-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="62539-126">-Confirm</span></span>
<span data-ttu-id="62539-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62539-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62539-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62539-128">-WhatIf</span></span>
<span data-ttu-id="62539-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62539-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62539-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62539-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62539-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62539-131">CommonParameters</span></span>
<span data-ttu-id="62539-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62539-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62539-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62539-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62539-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62539-134">INPUTS</span></span>

## <span data-ttu-id="62539-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62539-135">OUTPUTS</span></span>

## <span data-ttu-id="62539-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62539-136">NOTES</span></span>

## <span data-ttu-id="62539-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62539-137">RELATED LINKS</span></span>

