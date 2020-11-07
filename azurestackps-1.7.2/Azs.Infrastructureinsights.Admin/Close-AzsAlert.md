---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934448"
---
# <span data-ttu-id="90a79-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="90a79-101">Close-AzsAlert</span></span>

## <span data-ttu-id="90a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a79-102">SYNOPSIS</span></span>
<span data-ttu-id="90a79-103">Verilen uyarıyı kapatır.</span><span class="sxs-lookup"><span data-stu-id="90a79-103">Closes the given alert.</span></span>

## <span data-ttu-id="90a79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90a79-104">SYNTAX</span></span>

### <span data-ttu-id="90a79-105">Kapat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90a79-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90a79-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="90a79-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a79-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="90a79-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a79-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="90a79-108">DESCRIPTION</span></span>
<span data-ttu-id="90a79-109">Verilen uyarıyı kapatır.</span><span class="sxs-lookup"><span data-stu-id="90a79-109">Closes the given alert.</span></span>

## <span data-ttu-id="90a79-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90a79-110">EXAMPLES</span></span>

### <span data-ttu-id="90a79-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="90a79-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="90a79-112">Bir uyarıyı ada göre kapatma.</span><span class="sxs-lookup"><span data-stu-id="90a79-112">Close an alert by Name.</span></span>

### <span data-ttu-id="90a79-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="90a79-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="90a79-114">Bir uyarıyı boru aracılığıyla kapatma.</span><span class="sxs-lookup"><span data-stu-id="90a79-114">Close an alert through piping.</span></span>

## <span data-ttu-id="90a79-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90a79-115">PARAMETERS</span></span>

### <span data-ttu-id="90a79-116">-Force</span><span class="sxs-lookup"><span data-stu-id="90a79-116">-Force</span></span>
<span data-ttu-id="90a79-117">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="90a79-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="90a79-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90a79-118">-InputObject</span></span>
<span data-ttu-id="90a79-119">Get-AzsAlert 'den döndürülen bir uyarı.</span><span class="sxs-lookup"><span data-stu-id="90a79-119">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="90a79-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="90a79-120">-Location</span></span>
<span data-ttu-id="90a79-121">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="90a79-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a79-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="90a79-122">-Name</span></span>
<span data-ttu-id="90a79-123">Uyarı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="90a79-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a79-124">-ResourceGroupName</span></span>
<span data-ttu-id="90a79-125">Kaynağın bulunduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="90a79-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a79-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="90a79-126">-ResourceId</span></span>
<span data-ttu-id="90a79-127">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="90a79-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a79-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="90a79-128">-Confirm</span></span>
<span data-ttu-id="90a79-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90a79-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a79-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a79-130">-WhatIf</span></span>
<span data-ttu-id="90a79-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90a79-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a79-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90a79-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a79-133">CommonParameters</span></span>
<span data-ttu-id="90a79-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90a79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a79-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a79-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a79-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90a79-136">INPUTS</span></span>

## <span data-ttu-id="90a79-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90a79-137">OUTPUTS</span></span>

### <span data-ttu-id="90a79-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. Alert</span><span class="sxs-lookup"><span data-stu-id="90a79-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="90a79-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90a79-139">NOTES</span></span>

## <span data-ttu-id="90a79-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90a79-140">RELATED LINKS</span></span>

