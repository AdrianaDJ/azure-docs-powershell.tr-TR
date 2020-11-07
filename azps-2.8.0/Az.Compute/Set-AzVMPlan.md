---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 39ee23006490ce1dfbca1387a1e058df49850c5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752678"
---
# <span data-ttu-id="4b678-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="4b678-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="4b678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b678-102">SYNOPSIS</span></span>
<span data-ttu-id="4b678-103">Sanal makinedeki Market planı bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b678-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="4b678-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b678-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b678-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b678-105">DESCRIPTION</span></span>
<span data-ttu-id="4b678-106">**Set-AzVMPlan** cmdlet 'i sanal makine Için Azure Market planı bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b678-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="4b678-107">Bir Pazaryeri yansımasını komut satırı aracılığıyla dağıtabilmek için, programlı erişimin etkinleştirilmiş olması veya sanal makinenin Azure portalı kullanılarak dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b678-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="4b678-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b678-108">EXAMPLES</span></span>

## <span data-ttu-id="4b678-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b678-109">PARAMETERS</span></span>

### <span data-ttu-id="4b678-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b678-110">-DefaultProfile</span></span>
<span data-ttu-id="4b678-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b678-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b678-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b678-112">-Name</span></span>
<span data-ttu-id="4b678-113">Marketten resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b678-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="4b678-114">Bu, Get-AzVMImageSku cmdlet tarafından döndürülen değerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="4b678-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="4b678-115">Görüntü bilgilerini bulma hakkında daha fazla bilgi için, PowerShell ve Azure CLı ile Azure sanal makine görüntülerini seçme https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/)</span><span class="sxs-lookup"><span data-stu-id="4b678-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b678-116">-Ürün</span><span class="sxs-lookup"><span data-stu-id="4b678-116">-Product</span></span>
<span data-ttu-id="4b678-117">Marketten resmin çarpımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b678-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="4b678-118">Bu, **ImageReference** öğesinin **teklif** değeriyle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="4b678-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b678-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="4b678-119">-PromotionCode</span></span>
<span data-ttu-id="4b678-120">Promosyon kodu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b678-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b678-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4b678-121">-Publisher</span></span>
<span data-ttu-id="4b678-122">Resmin yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b678-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="4b678-123">Bu bilgileri Get-AzVMImagePublisher cmdlet 'i kullanarak bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b678-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b678-124">-VM</span><span class="sxs-lookup"><span data-stu-id="4b678-124">-VM</span></span>
<span data-ttu-id="4b678-125">Market planı ayarlanacak sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b678-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="4b678-126">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b678-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="4b678-127">Sanal makine nesnesi oluşturmak için New-AzVMConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b678-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b678-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b678-128">CommonParameters</span></span>
<span data-ttu-id="4b678-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b678-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b678-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b678-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b678-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b678-131">INPUTS</span></span>

### <span data-ttu-id="4b678-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4b678-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4b678-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4b678-133">System.String</span></span>

## <span data-ttu-id="4b678-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b678-134">OUTPUTS</span></span>

### <span data-ttu-id="4b678-135">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4b678-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4b678-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b678-136">NOTES</span></span>

## <span data-ttu-id="4b678-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b678-137">RELATED LINKS</span></span>

[<span data-ttu-id="4b678-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b678-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4b678-139">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="4b678-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="4b678-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4b678-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="4b678-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4b678-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)