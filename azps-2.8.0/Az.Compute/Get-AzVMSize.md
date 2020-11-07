---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 2ac1e336161d4cfad1bbef37ec98716456a8143c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752902"
---
# <span data-ttu-id="58ced-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="58ced-101">Get-AzVMSize</span></span>

## <span data-ttu-id="58ced-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ced-102">SYNOPSIS</span></span>
<span data-ttu-id="58ced-103">Kullanılabilir sanal makine boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="58ced-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="58ced-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58ced-104">SYNTAX</span></span>

### <span data-ttu-id="58ced-105">Listvirtualparaminesizeparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58ced-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58ced-106">Listavailablesizesforkullanılabilirliği Bilityset</span><span class="sxs-lookup"><span data-stu-id="58ced-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58ced-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="58ced-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58ced-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="58ced-108">DESCRIPTION</span></span>
<span data-ttu-id="58ced-109">**Get-AzVMSize** cmdlet 'i kullanılabilir sanal makine boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="58ced-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="58ced-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58ced-110">EXAMPLES</span></span>

### <span data-ttu-id="58ced-111">Örnek 1: bir konum için sanal makine boyutlarını alma</span><span class="sxs-lookup"><span data-stu-id="58ced-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="58ced-112">Bu komut, belirtilen konumdaki sanal makinelerin kullanılabilir boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="58ced-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="58ced-113">Örnek 2: kullanılabilirlik kümesi için boyutları alma</span><span class="sxs-lookup"><span data-stu-id="58ced-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="58ced-114">Bu komut, AvailabilitySet17 adlı kullanılabilirlik kümesinde dağıtabileceğiniz sanal makinelerin kullanılabilir boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="58ced-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="58ced-115">Örnek 3: var olan bir sanal makinenin boyutlarını alma</span><span class="sxs-lookup"><span data-stu-id="58ced-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="58ced-116">Bu komut, VirtualMachine12 adındaki mevcut sanal makine için kullanılabilir boyutları alır.</span><span class="sxs-lookup"><span data-stu-id="58ced-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="58ced-117">Bu komutun aldığı boyutlara bu sanal makineyi yeniden boyutlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58ced-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="58ced-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58ced-118">PARAMETERS</span></span>

### <span data-ttu-id="58ced-119">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="58ced-119">-AvailabilitySetName</span></span>
<span data-ttu-id="58ced-120">Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58ced-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ced-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ced-121">-DefaultProfile</span></span>
<span data-ttu-id="58ced-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58ced-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58ced-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="58ced-123">-Location</span></span>
<span data-ttu-id="58ced-124">Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="58ced-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ced-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ced-125">-ResourceGroupName</span></span>
<span data-ttu-id="58ced-126">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58ced-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ced-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="58ced-127">-VMName</span></span>
<span data-ttu-id="58ced-128">Bu cmdlet 'in yeniden boyutlandırma için kullanılabilir sanal makine boyutlarını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58ced-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ced-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ced-129">CommonParameters</span></span>
<span data-ttu-id="58ced-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58ced-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ced-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="58ced-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ced-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58ced-132">INPUTS</span></span>

### <span data-ttu-id="58ced-133">System. String</span><span class="sxs-lookup"><span data-stu-id="58ced-133">System.String</span></span>

## <span data-ttu-id="58ced-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58ced-134">OUTPUTS</span></span>

### <span data-ttu-id="58ced-135">Microsoft. Azure. Commands. COMPUTE. modeller. psvirtualın</span><span class="sxs-lookup"><span data-stu-id="58ced-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="58ced-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58ced-136">NOTES</span></span>

## <span data-ttu-id="58ced-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58ced-137">RELATED LINKS</span></span>

[<span data-ttu-id="58ced-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="58ced-138">Get-AzVM</span></span>](./Get-AzVM.md)


