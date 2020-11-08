---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93940288"
---
# <span data-ttu-id="f9914-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="f9914-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="f9914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9914-102">SYNOPSIS</span></span>
<span data-ttu-id="f9914-103">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="f9914-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="f9914-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9914-104">SYNTAX</span></span>

### <span data-ttu-id="f9914-105">Products_Download (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9914-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9914-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f9914-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9914-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9914-107">DESCRIPTION</span></span>
<span data-ttu-id="f9914-108">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="f9914-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="f9914-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9914-109">EXAMPLES</span></span>

### <span data-ttu-id="f9914-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="f9914-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="f9914-111">Azure Marketi 'nden bir ürünü indirme</span><span class="sxs-lookup"><span data-stu-id="f9914-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="f9914-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9914-112">PARAMETERS</span></span>

### <span data-ttu-id="f9914-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9914-113">-Name</span></span>
<span data-ttu-id="f9914-114">Ürünün adı</span><span class="sxs-lookup"><span data-stu-id="f9914-114">Name of the product</span></span>

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

### <span data-ttu-id="f9914-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="f9914-115">-ActivationName</span></span>
<span data-ttu-id="f9914-116">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="f9914-116">Name of the activation.</span></span>

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

### <span data-ttu-id="f9914-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9914-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9914-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f9914-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f9914-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f9914-119">-ResourceId</span></span>
<span data-ttu-id="f9914-120">Azure Bridge ürünü için kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f9914-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="f9914-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="f9914-121">-AsJob</span></span>
<span data-ttu-id="f9914-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="f9914-122">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="f9914-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f9914-123">-Force</span></span>
<span data-ttu-id="f9914-124">Değiştir onay sorma</span><span class="sxs-lookup"><span data-stu-id="f9914-124">Switch parameter not to ask for confirmation</span></span>

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

### <span data-ttu-id="f9914-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9914-125">-WhatIf</span></span>
<span data-ttu-id="f9914-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9914-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9914-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9914-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9914-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9914-128">-Confirm</span></span>
<span data-ttu-id="f9914-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9914-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9914-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9914-130">CommonParameters</span></span>
<span data-ttu-id="f9914-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9914-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9914-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9914-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9914-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9914-133">INPUTS</span></span>

## <span data-ttu-id="f9914-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9914-134">OUTPUTS</span></span>

## <span data-ttu-id="f9914-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9914-135">NOTES</span></span>

## <span data-ttu-id="f9914-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9914-136">RELATED LINKS</span></span>
