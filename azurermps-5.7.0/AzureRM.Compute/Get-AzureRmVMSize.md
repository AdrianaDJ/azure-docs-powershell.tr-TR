---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591061"
---
# <span data-ttu-id="784c9-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="784c9-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="784c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="784c9-102">SYNOPSIS</span></span>
<span data-ttu-id="784c9-103">Kullanılabilir sanal makine boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="784c9-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="784c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="784c9-104">SYNTAX</span></span>

### <span data-ttu-id="784c9-105">Listvirtualparaminesizeparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="784c9-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="784c9-106">Listavailablesizesforkullanılabilirliği Bilityset</span><span class="sxs-lookup"><span data-stu-id="784c9-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="784c9-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="784c9-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="784c9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="784c9-108">DESCRIPTION</span></span>
<span data-ttu-id="784c9-109">**Get-AzureRmVMSize** cmdlet 'i kullanılabilir sanal makine boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="784c9-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="784c9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="784c9-110">EXAMPLES</span></span>

### <span data-ttu-id="784c9-111">Örnek 1: bir konum için sanal makine boyutlarını alma</span><span class="sxs-lookup"><span data-stu-id="784c9-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="784c9-112">Bu komut, belirtilen konumdaki sanal makinelerin kullanılabilir boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="784c9-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="784c9-113">Örnek 2: kullanılabilirlik kümesi için boyutları alma</span><span class="sxs-lookup"><span data-stu-id="784c9-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="784c9-114">Bu komut, AvailabilitySet17 adlı kullanılabilirlik kümesinde dağıtabileceğiniz sanal makinelerin kullanılabilir boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="784c9-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="784c9-115">Örnek 3: var olan bir sanal makinenin boyutlarını alma</span><span class="sxs-lookup"><span data-stu-id="784c9-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="784c9-116">Bu komut, VirtualMachine12 adındaki mevcut sanal makine için kullanılabilir boyutları alır.</span><span class="sxs-lookup"><span data-stu-id="784c9-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="784c9-117">Bu komutun aldığı boyutlara bu sanal makineyi yeniden boyutlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="784c9-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="784c9-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="784c9-118">PARAMETERS</span></span>

### <span data-ttu-id="784c9-119">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="784c9-119">-AvailabilitySetName</span></span>
<span data-ttu-id="784c9-120">Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="784c9-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784c9-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="784c9-121">-Location</span></span>
<span data-ttu-id="784c9-122">Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="784c9-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784c9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784c9-123">-ResourceGroupName</span></span>
<span data-ttu-id="784c9-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="784c9-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784c9-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="784c9-125">-VMName</span></span>
<span data-ttu-id="784c9-126">Bu cmdlet 'in yeniden boyutlandırma için kullanılabilir sanal makine boyutlarını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="784c9-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784c9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784c9-127">CommonParameters</span></span>
<span data-ttu-id="784c9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="784c9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784c9-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="784c9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784c9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="784c9-130">INPUTS</span></span>

### <span data-ttu-id="784c9-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="784c9-131">None</span></span>
<span data-ttu-id="784c9-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="784c9-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="784c9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="784c9-133">OUTPUTS</span></span>

## <span data-ttu-id="784c9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="784c9-134">NOTES</span></span>

## <span data-ttu-id="784c9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="784c9-135">RELATED LINKS</span></span>

[<span data-ttu-id="784c9-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="784c9-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


