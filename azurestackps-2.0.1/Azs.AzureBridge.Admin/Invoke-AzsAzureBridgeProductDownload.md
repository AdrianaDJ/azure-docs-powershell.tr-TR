---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7ca58f806f4d63f2938e3934838a40cbbb113b2
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2020
ms.locfileid: "94107338"
---
# <span data-ttu-id="73313-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="73313-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="73313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73313-102">SYNOPSIS</span></span>
<span data-ttu-id="73313-103">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="73313-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="73313-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73313-104">SYNTAX</span></span>

### <span data-ttu-id="73313-105">Products_Download (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73313-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73313-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="73313-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73313-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="73313-107">DESCRIPTION</span></span>
<span data-ttu-id="73313-108">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="73313-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="73313-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73313-109">EXAMPLES</span></span>

### <span data-ttu-id="73313-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="73313-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="73313-111">Azure Marketi 'nden bir ürünü indirme</span><span class="sxs-lookup"><span data-stu-id="73313-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="73313-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73313-112">PARAMETERS</span></span>

### <span data-ttu-id="73313-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="73313-113">-ActivationName</span></span>
<span data-ttu-id="73313-114">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="73313-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73313-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="73313-115">-AsJob</span></span>
<span data-ttu-id="73313-116">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="73313-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="73313-117">-Force</span><span class="sxs-lookup"><span data-stu-id="73313-117">-Force</span></span>
<span data-ttu-id="73313-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="73313-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="73313-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="73313-119">-Name</span></span>
<span data-ttu-id="73313-120">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="73313-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73313-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73313-121">-ResourceGroupName</span></span>
<span data-ttu-id="73313-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="73313-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73313-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="73313-123">-ResourceId</span></span>
<span data-ttu-id="73313-124">Azure Bridge ürünü için kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="73313-124">Resource identifier for azure bridge product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73313-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="73313-125">-Confirm</span></span>
<span data-ttu-id="73313-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73313-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73313-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73313-127">-WhatIf</span></span>
<span data-ttu-id="73313-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73313-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73313-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73313-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73313-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73313-130">CommonParameters</span></span>
<span data-ttu-id="73313-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73313-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73313-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73313-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73313-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73313-133">INPUTS</span></span>

## <span data-ttu-id="73313-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73313-134">OUTPUTS</span></span>

## <span data-ttu-id="73313-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73313-135">NOTES</span></span>

## <span data-ttu-id="73313-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73313-136">RELATED LINKS</span></span>

