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
ms.locfileid: "93940284"
---
# <span data-ttu-id="667aa-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="667aa-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="667aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667aa-102">SYNOPSIS</span></span>
<span data-ttu-id="667aa-103">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="667aa-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="667aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="667aa-104">SYNTAX</span></span>

### <span data-ttu-id="667aa-105">Products_Download (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="667aa-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667aa-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="667aa-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="667aa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="667aa-107">DESCRIPTION</span></span>
<span data-ttu-id="667aa-108">Azure Marketi 'nden bir ürünü indirir.</span><span class="sxs-lookup"><span data-stu-id="667aa-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="667aa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="667aa-109">EXAMPLES</span></span>

### <span data-ttu-id="667aa-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="667aa-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="667aa-111">Azure Marketi 'nden bir ürünü indirme</span><span class="sxs-lookup"><span data-stu-id="667aa-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="667aa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="667aa-112">PARAMETERS</span></span>

### <span data-ttu-id="667aa-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="667aa-113">-Name</span></span>
<span data-ttu-id="667aa-114">Ürünün adı</span><span class="sxs-lookup"><span data-stu-id="667aa-114">Name of the product</span></span>

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

### <span data-ttu-id="667aa-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="667aa-115">-ActivationName</span></span>
<span data-ttu-id="667aa-116">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="667aa-116">Name of the activation.</span></span>

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

### <span data-ttu-id="667aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="667aa-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="667aa-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="667aa-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="667aa-119">-ResourceId</span></span>
<span data-ttu-id="667aa-120">Azure Bridge ürünü için kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="667aa-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="667aa-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="667aa-121">-AsJob</span></span>
<span data-ttu-id="667aa-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="667aa-122">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="667aa-123">-Force</span><span class="sxs-lookup"><span data-stu-id="667aa-123">-Force</span></span>
<span data-ttu-id="667aa-124">Değiştir onay sorma</span><span class="sxs-lookup"><span data-stu-id="667aa-124">Switch parameter not to ask for confirmation</span></span>

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

### <span data-ttu-id="667aa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667aa-125">-WhatIf</span></span>
<span data-ttu-id="667aa-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="667aa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667aa-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="667aa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667aa-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="667aa-128">-Confirm</span></span>
<span data-ttu-id="667aa-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="667aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667aa-130">CommonParameters</span></span>
<span data-ttu-id="667aa-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="667aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667aa-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667aa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667aa-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="667aa-133">INPUTS</span></span>

## <span data-ttu-id="667aa-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="667aa-134">OUTPUTS</span></span>

## <span data-ttu-id="667aa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="667aa-135">NOTES</span></span>

## <span data-ttu-id="667aa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="667aa-136">RELATED LINKS</span></span>
