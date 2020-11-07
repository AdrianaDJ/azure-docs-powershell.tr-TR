---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935106"
---
# <span data-ttu-id="ffa51-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="ffa51-101">Close-AzsAlert</span></span>

## <span data-ttu-id="ffa51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa51-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa51-103">Verilen uyarıyı kapatır.</span><span class="sxs-lookup"><span data-stu-id="ffa51-103">Closes the given alert.</span></span>

## <span data-ttu-id="ffa51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffa51-104">SYNTAX</span></span>

### <span data-ttu-id="ffa51-105">Kapat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ffa51-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ffa51-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ffa51-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa51-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="ffa51-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa51-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffa51-108">DESCRIPTION</span></span>
<span data-ttu-id="ffa51-109">Verilen uyarıyı kapatır.</span><span class="sxs-lookup"><span data-stu-id="ffa51-109">Closes the given alert.</span></span>

## <span data-ttu-id="ffa51-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffa51-110">EXAMPLES</span></span>

### <span data-ttu-id="ffa51-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="ffa51-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="ffa51-112">Bir uyarıyı ada göre kapatma.</span><span class="sxs-lookup"><span data-stu-id="ffa51-112">Close an alert by Name.</span></span>

### <span data-ttu-id="ffa51-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="ffa51-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="ffa51-114">Bir uyarıyı boru aracılığıyla kapatma.</span><span class="sxs-lookup"><span data-stu-id="ffa51-114">Close an alert through piping.</span></span>

## <span data-ttu-id="ffa51-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffa51-115">PARAMETERS</span></span>

### <span data-ttu-id="ffa51-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ffa51-116">-Name</span></span>
<span data-ttu-id="ffa51-117">Uyarı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ffa51-117">The alert identifier.</span></span>

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

### <span data-ttu-id="ffa51-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="ffa51-118">-Location</span></span>
<span data-ttu-id="ffa51-119">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="ffa51-119">Name of the location.</span></span>

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

### <span data-ttu-id="ffa51-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa51-120">-ResourceGroupName</span></span>
<span data-ttu-id="ffa51-121">Uyarının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ffa51-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="ffa51-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffa51-122">-InputObject</span></span>
<span data-ttu-id="ffa51-123">Get-AzsAlert 'den döndürülen bir uyarı.</span><span class="sxs-lookup"><span data-stu-id="ffa51-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="ffa51-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ffa51-124">-ResourceId</span></span>
<span data-ttu-id="ffa51-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ffa51-125">The resource id.</span></span>

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

### <span data-ttu-id="ffa51-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ffa51-126">-Force</span></span>
<span data-ttu-id="ffa51-127">Onayınızı istemeyecektir.</span><span class="sxs-lookup"><span data-stu-id="ffa51-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="ffa51-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa51-128">-WhatIf</span></span>
<span data-ttu-id="ffa51-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffa51-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa51-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffa51-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa51-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffa51-131">-Confirm</span></span>
<span data-ttu-id="ffa51-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffa51-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa51-133">CommonParameters</span></span>
<span data-ttu-id="ffa51-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffa51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa51-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa51-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa51-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffa51-136">INPUTS</span></span>

## <span data-ttu-id="ffa51-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffa51-137">OUTPUTS</span></span>

### <span data-ttu-id="ffa51-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. Alert</span><span class="sxs-lookup"><span data-stu-id="ffa51-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="ffa51-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffa51-139">NOTES</span></span>

## <span data-ttu-id="ffa51-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffa51-140">RELATED LINKS</span></span>
