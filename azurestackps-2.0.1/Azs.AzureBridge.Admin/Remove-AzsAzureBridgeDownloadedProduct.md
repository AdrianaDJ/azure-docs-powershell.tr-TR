---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d75764209b56ed0cc05d80e00581de3f982e435
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2020
ms.locfileid: "94107337"
---
# <span data-ttu-id="8d15c-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="8d15c-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="8d15c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d15c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d15c-103">Azure Marketi 'nden indirilen bir ürünü silme.</span><span class="sxs-lookup"><span data-stu-id="8d15c-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="8d15c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d15c-104">SYNTAX</span></span>

### <span data-ttu-id="8d15c-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d15c-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d15c-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="8d15c-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d15c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d15c-107">DESCRIPTION</span></span>
<span data-ttu-id="8d15c-108">Azure Marketi 'nden indirilen bir ürünü silme.</span><span class="sxs-lookup"><span data-stu-id="8d15c-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="8d15c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d15c-109">EXAMPLES</span></span>

### <span data-ttu-id="8d15c-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8d15c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="8d15c-111">Azure Marketi 'nden indirilen bir ürünü silme</span><span class="sxs-lookup"><span data-stu-id="8d15c-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="8d15c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d15c-112">PARAMETERS</span></span>

### <span data-ttu-id="8d15c-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="8d15c-113">-ActivationName</span></span>
<span data-ttu-id="8d15c-114">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="8d15c-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d15c-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8d15c-115">-AsJob</span></span>
<span data-ttu-id="8d15c-116">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="8d15c-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8d15c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8d15c-117">-Force</span></span>
<span data-ttu-id="8d15c-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="8d15c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8d15c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d15c-119">-Name</span></span>
<span data-ttu-id="8d15c-120">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="8d15c-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d15c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d15c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d15c-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8d15c-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d15c-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8d15c-123">-ResourceId</span></span>
<span data-ttu-id="8d15c-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8d15c-124">The resource id.</span></span>

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

### <span data-ttu-id="8d15c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="8d15c-125">-Confirm</span></span>
<span data-ttu-id="8d15c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d15c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d15c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d15c-127">-WhatIf</span></span>
<span data-ttu-id="8d15c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d15c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d15c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8d15c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d15c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d15c-130">CommonParameters</span></span>
<span data-ttu-id="8d15c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d15c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d15c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d15c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d15c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d15c-133">INPUTS</span></span>

## <span data-ttu-id="8d15c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d15c-134">OUTPUTS</span></span>

### <span data-ttu-id="8d15c-135">Microsoft. AzureStack. Management. AzureBridge. admin. modeller. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="8d15c-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="8d15c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d15c-136">NOTES</span></span>

## <span data-ttu-id="8d15c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d15c-137">RELATED LINKS</span></span>

