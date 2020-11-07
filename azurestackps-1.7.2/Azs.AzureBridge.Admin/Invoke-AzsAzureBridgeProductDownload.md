---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ebe9c71560f18ba9e4d7fb52514a4f5b7007bfb
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93940270"
---
# <span data-ttu-id="8f5bb-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="8f5bb-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="8f5bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5bb-103">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="8f5bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f5bb-104">SYNTAX</span></span>

### <span data-ttu-id="8f5bb-105">Products_Download (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f5bb-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f5bb-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="8f5bb-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f5bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f5bb-107">DESCRIPTION</span></span>
<span data-ttu-id="8f5bb-108">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="8f5bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f5bb-109">EXAMPLES</span></span>

### <span data-ttu-id="8f5bb-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8f5bb-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="8f5bb-111">Azure Marketi 'nden bir ürünü indirme</span><span class="sxs-lookup"><span data-stu-id="8f5bb-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="8f5bb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f5bb-112">PARAMETERS</span></span>

### <span data-ttu-id="8f5bb-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="8f5bb-113">-ActivationName</span></span>
<span data-ttu-id="8f5bb-114">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-114">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5bb-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8f5bb-115">-AsJob</span></span>
<span data-ttu-id="8f5bb-116">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8f5bb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8f5bb-117">-Force</span></span>
<span data-ttu-id="8f5bb-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8f5bb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f5bb-119">-Name</span></span>
<span data-ttu-id="8f5bb-120">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-120">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f5bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="8f5bb-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5bb-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8f5bb-123">-ResourceId</span></span>
<span data-ttu-id="8f5bb-124">Azure Bridge ürünü için kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="8f5bb-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f5bb-125">-Confirm</span></span>
<span data-ttu-id="8f5bb-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5bb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5bb-127">-WhatIf</span></span>
<span data-ttu-id="8f5bb-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f5bb-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5bb-130">CommonParameters</span></span>
<span data-ttu-id="8f5bb-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f5bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5bb-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5bb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5bb-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f5bb-133">INPUTS</span></span>

## <span data-ttu-id="8f5bb-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f5bb-134">OUTPUTS</span></span>

## <span data-ttu-id="8f5bb-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f5bb-135">NOTES</span></span>

## <span data-ttu-id="8f5bb-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f5bb-136">RELATED LINKS</span></span>

