---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751108"
---
# <span data-ttu-id="da86d-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="da86d-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="da86d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da86d-102">SYNOPSIS</span></span>
<span data-ttu-id="da86d-103">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="da86d-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="da86d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da86d-104">SYNTAX</span></span>

### <span data-ttu-id="da86d-105">Uygula (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="da86d-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da86d-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="da86d-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da86d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="da86d-107">DESCRIPTION</span></span>
<span data-ttu-id="da86d-108">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="da86d-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="da86d-109">Başlatıldıktan sonra, güncelleştirmenin ilerlemesini değiştirmek için Get-AzsUpdateRun kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="da86d-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="da86d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da86d-110">EXAMPLES</span></span>

### <span data-ttu-id="da86d-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="da86d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="da86d-112">Güncelleştirme konumunda belirli bir güncelleştirme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="da86d-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="da86d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da86d-113">PARAMETERS</span></span>

### <span data-ttu-id="da86d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="da86d-114">-AsJob</span></span>
<span data-ttu-id="da86d-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="da86d-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="da86d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="da86d-116">-Force</span></span>
<span data-ttu-id="da86d-117">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="da86d-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="da86d-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="da86d-118">-Location</span></span>
<span data-ttu-id="da86d-119">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="da86d-119">The name of the update location.</span></span>

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

### <span data-ttu-id="da86d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="da86d-120">-Name</span></span>
<span data-ttu-id="da86d-121">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="da86d-121">Name of the update.</span></span>

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

### <span data-ttu-id="da86d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da86d-122">-ResourceGroupName</span></span>
<span data-ttu-id="da86d-123">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="da86d-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="da86d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="da86d-124">-ResourceId</span></span>
<span data-ttu-id="da86d-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="da86d-125">The resource id.</span></span>

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

### <span data-ttu-id="da86d-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="da86d-126">-Confirm</span></span>
<span data-ttu-id="da86d-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da86d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da86d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da86d-128">-WhatIf</span></span>
<span data-ttu-id="da86d-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da86d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da86d-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da86d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da86d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da86d-131">CommonParameters</span></span>
<span data-ttu-id="da86d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da86d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da86d-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da86d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da86d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da86d-134">INPUTS</span></span>

## <span data-ttu-id="da86d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da86d-135">OUTPUTS</span></span>

### <span data-ttu-id="da86d-136">Microsoft. AzureStack. Management. Update. admin. modeller. Update</span><span class="sxs-lookup"><span data-stu-id="da86d-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="da86d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da86d-137">NOTES</span></span>

## <span data-ttu-id="da86d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da86d-138">RELATED LINKS</span></span>

