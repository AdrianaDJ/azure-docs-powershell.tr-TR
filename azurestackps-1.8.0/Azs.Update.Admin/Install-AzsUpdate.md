---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934559"
---
# <span data-ttu-id="a360e-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="a360e-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="a360e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a360e-102">SYNOPSIS</span></span>
<span data-ttu-id="a360e-103">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a360e-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="a360e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a360e-104">SYNTAX</span></span>

### <span data-ttu-id="a360e-105">Uygula (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a360e-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a360e-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a360e-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a360e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a360e-107">DESCRIPTION</span></span>
<span data-ttu-id="a360e-108">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a360e-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="a360e-109">Başlatıldıktan sonra, güncelleştirmenin ilerlemesini değiştirmek için Get-AzsUpdateRun kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a360e-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="a360e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a360e-110">EXAMPLES</span></span>

### <span data-ttu-id="a360e-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a360e-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="a360e-112">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a360e-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="a360e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a360e-113">PARAMETERS</span></span>

### <span data-ttu-id="a360e-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a360e-114">-Name</span></span>
<span data-ttu-id="a360e-115">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="a360e-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a360e-116">-ResourceGroupName</span></span>
<span data-ttu-id="a360e-117">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a360e-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360e-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a360e-118">-Location</span></span>
<span data-ttu-id="a360e-119">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="a360e-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360e-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="a360e-120">-AsJob</span></span>
<span data-ttu-id="a360e-121">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="a360e-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a360e-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a360e-122">-ResourceId</span></span>
<span data-ttu-id="a360e-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a360e-123">The resource id.</span></span>

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

### <span data-ttu-id="a360e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a360e-124">-Force</span></span>
<span data-ttu-id="a360e-125">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="a360e-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="a360e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a360e-126">-WhatIf</span></span>
<span data-ttu-id="a360e-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a360e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a360e-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a360e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a360e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a360e-129">-Confirm</span></span>
<span data-ttu-id="a360e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a360e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a360e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a360e-131">CommonParameters</span></span>
<span data-ttu-id="a360e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a360e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a360e-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a360e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a360e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a360e-134">INPUTS</span></span>

## <span data-ttu-id="a360e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a360e-135">OUTPUTS</span></span>

### <span data-ttu-id="a360e-136">Microsoft. AzureStack. Management. Update. admin. modeller. Update</span><span class="sxs-lookup"><span data-stu-id="a360e-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="a360e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a360e-137">NOTES</span></span>

## <span data-ttu-id="a360e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a360e-138">RELATED LINKS</span></span>
