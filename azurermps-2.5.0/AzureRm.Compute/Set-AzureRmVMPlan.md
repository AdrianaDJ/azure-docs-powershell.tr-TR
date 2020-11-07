---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940174"
---
# <span data-ttu-id="167b9-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="167b9-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="167b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="167b9-102">SYNOPSIS</span></span>
<span data-ttu-id="167b9-103">Sanal makinedeki Market planı bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="167b9-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="167b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="167b9-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="167b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="167b9-105">DESCRIPTION</span></span>
<span data-ttu-id="167b9-106">**Set-AzureRmVMPlan** cmdlet 'i, sanal makine Için Azure Market planı bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="167b9-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="167b9-107">Bir Pazaryeri yansımasını komut satırı aracılığıyla dağıtabilmek için, programlı erişimin etkinleştirilmiş olması veya sanal makinenin Azure portalı kullanılarak dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="167b9-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="167b9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="167b9-108">EXAMPLES</span></span>

## <span data-ttu-id="167b9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="167b9-109">PARAMETERS</span></span>

### <span data-ttu-id="167b9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167b9-110">-DefaultProfile</span></span>
<span data-ttu-id="167b9-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="167b9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167b9-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="167b9-112">-Name</span></span>
<span data-ttu-id="167b9-113">Marketten resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="167b9-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="167b9-114">Bu, Get-AzureRmVMImageSku cmdlet tarafından döndürülen değerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="167b9-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="167b9-115">Görüntü bilgilerini bulma hakkında daha fazla bilgi için, PowerShell ve Azure CLı ile Azure sanal makine görüntülerini seçme https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/)</span><span class="sxs-lookup"><span data-stu-id="167b9-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167b9-116">-Ürün</span><span class="sxs-lookup"><span data-stu-id="167b9-116">-Product</span></span>
<span data-ttu-id="167b9-117">Marketten resmin çarpımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="167b9-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="167b9-118">Bu, **ImageReference** öğesinin **teklif** değeriyle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="167b9-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167b9-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="167b9-119">-PromotionCode</span></span>
<span data-ttu-id="167b9-120">Promosyon kodu belirtir.</span><span class="sxs-lookup"><span data-stu-id="167b9-120">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167b9-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="167b9-121">-Publisher</span></span>
<span data-ttu-id="167b9-122">Resmin yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="167b9-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="167b9-123">Bu bilgileri Get-AzureRmVMImagePublisher cmdlet 'i kullanarak bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="167b9-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167b9-124">-VM</span><span class="sxs-lookup"><span data-stu-id="167b9-124">-VM</span></span>
<span data-ttu-id="167b9-125">Market planı ayarlanacak sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="167b9-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="167b9-126">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="167b9-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="167b9-127">Sanal makine nesnesi oluşturmak için New-AzureRmVMConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="167b9-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="167b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167b9-128">CommonParameters</span></span>
<span data-ttu-id="167b9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="167b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167b9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167b9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="167b9-131">INPUTS</span></span>

### <span data-ttu-id="167b9-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="167b9-132">PSVirtualMachine</span></span>
<span data-ttu-id="167b9-133">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="167b9-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="167b9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="167b9-134">OUTPUTS</span></span>

### <span data-ttu-id="167b9-135">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="167b9-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="167b9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="167b9-136">NOTES</span></span>

## <span data-ttu-id="167b9-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="167b9-137">RELATED LINKS</span></span>

[<span data-ttu-id="167b9-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="167b9-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="167b9-139">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="167b9-139">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="167b9-140">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="167b9-140">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="167b9-141">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="167b9-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
