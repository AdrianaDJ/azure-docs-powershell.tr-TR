---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934539"
---
# <span data-ttu-id="03526-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="03526-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="03526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03526-102">SYNOPSIS</span></span>
<span data-ttu-id="03526-103">Verilen uyarıyı onarır.</span><span class="sxs-lookup"><span data-stu-id="03526-103">Repairs the given alert.</span></span>

## <span data-ttu-id="03526-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03526-104">SYNTAX</span></span>

### <span data-ttu-id="03526-105">Onar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03526-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03526-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="03526-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03526-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="03526-107">DESCRIPTION</span></span>
<span data-ttu-id="03526-108">Verilen uyarıyı onarır.</span><span class="sxs-lookup"><span data-stu-id="03526-108">Repairs the given alert.</span></span>

## <span data-ttu-id="03526-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03526-109">EXAMPLES</span></span>

### <span data-ttu-id="03526-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03526-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="03526-111">Uyarıyı adıyla onarır.</span><span class="sxs-lookup"><span data-stu-id="03526-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="03526-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="03526-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="03526-113">Bir uyarıyı boru üzerinden onarır.</span><span class="sxs-lookup"><span data-stu-id="03526-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="03526-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03526-114">PARAMETERS</span></span>

### <span data-ttu-id="03526-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03526-115">-Force</span></span>
<span data-ttu-id="03526-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="03526-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="03526-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03526-117">-InputObject</span></span>
<span data-ttu-id="03526-118">Get-AzsAlert 'den döndürülen bir uyarı.</span><span class="sxs-lookup"><span data-stu-id="03526-118">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03526-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="03526-119">-Location</span></span>
<span data-ttu-id="03526-120">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="03526-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03526-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="03526-121">-Name</span></span>
<span data-ttu-id="03526-122">Uyarı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="03526-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03526-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03526-123">-ResourceGroupName</span></span>
<span data-ttu-id="03526-124">Kaynağın bulunduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="03526-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03526-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="03526-125">-Confirm</span></span>
<span data-ttu-id="03526-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03526-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03526-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03526-127">-WhatIf</span></span>
<span data-ttu-id="03526-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03526-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03526-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03526-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03526-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03526-130">CommonParameters</span></span>
<span data-ttu-id="03526-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03526-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03526-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03526-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03526-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03526-133">INPUTS</span></span>

## <span data-ttu-id="03526-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03526-134">OUTPUTS</span></span>

## <span data-ttu-id="03526-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03526-135">NOTES</span></span>

## <span data-ttu-id="03526-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03526-136">RELATED LINKS</span></span>

