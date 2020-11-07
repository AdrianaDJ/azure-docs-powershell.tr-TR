---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsize
schema: 2.0.0
ms.openlocfilehash: 77e4de344e3dd89eac09b1ebefb6ba49071dcbf2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940191"
---
# <span data-ttu-id="6f5bc-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="6f5bc-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="6f5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5bc-103">Kullanılabilir sanal makine boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f5bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f5bc-104">SYNTAX</span></span>

### <span data-ttu-id="6f5bc-105">Listvirtualparaminesizeparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f5bc-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f5bc-106">Listavailablesizesforkullanılabilirliği Bilityset</span><span class="sxs-lookup"><span data-stu-id="6f5bc-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f5bc-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6f5bc-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f5bc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f5bc-108">DESCRIPTION</span></span>
<span data-ttu-id="6f5bc-109">**Get-AzureRmVMSize** cmdlet 'i kullanılabilir sanal makine boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="6f5bc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f5bc-110">EXAMPLES</span></span>

### <span data-ttu-id="6f5bc-111">Örnek 1: bir konum için sanal makine boyutlarını alma</span><span class="sxs-lookup"><span data-stu-id="6f5bc-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="6f5bc-112">Bu komut, belirtilen konumdaki sanal makinelerin kullanılabilir boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="6f5bc-113">Örnek 2: kullanılabilirlik kümesi için boyutları alma</span><span class="sxs-lookup"><span data-stu-id="6f5bc-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="6f5bc-114">Bu komut, AvailabilitySet17 adlı kullanılabilirlik kümesinde dağıtabileceğiniz sanal makinelerin kullanılabilir boyutlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="6f5bc-115">Örnek 3: var olan bir sanal makinenin boyutlarını alma</span><span class="sxs-lookup"><span data-stu-id="6f5bc-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="6f5bc-116">Bu komut, VirtualMachine12 adındaki mevcut sanal makine için kullanılabilir boyutları alır.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="6f5bc-117">Bu komutun aldığı boyutlara bu sanal makineyi yeniden boyutlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="6f5bc-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f5bc-118">PARAMETERS</span></span>

### <span data-ttu-id="6f5bc-119">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="6f5bc-119">-AvailabilitySetName</span></span>
<span data-ttu-id="6f5bc-120">Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="6f5bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5bc-121">-DefaultProfile</span></span>
<span data-ttu-id="6f5bc-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f5bc-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="6f5bc-123">-Location</span></span>
<span data-ttu-id="6f5bc-124">Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="6f5bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f5bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f5bc-126">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6f5bc-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f5bc-127">-VMName</span></span>
<span data-ttu-id="6f5bc-128">Bu cmdlet 'in yeniden boyutlandırma için kullanılabilir sanal makine boyutlarını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="6f5bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5bc-129">CommonParameters</span></span>
<span data-ttu-id="6f5bc-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5bc-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5bc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5bc-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f5bc-132">INPUTS</span></span>

### <span data-ttu-id="6f5bc-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f5bc-133">None</span></span>
<span data-ttu-id="6f5bc-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6f5bc-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f5bc-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f5bc-135">OUTPUTS</span></span>

### <span data-ttu-id="6f5bc-136">Microsoft. Azure. Commands. COMPUTE. modeller. psvirtualın</span><span class="sxs-lookup"><span data-stu-id="6f5bc-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="6f5bc-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f5bc-137">NOTES</span></span>

## <span data-ttu-id="6f5bc-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f5bc-138">RELATED LINKS</span></span>

[<span data-ttu-id="6f5bc-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6f5bc-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


