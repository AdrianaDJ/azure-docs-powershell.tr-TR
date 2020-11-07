---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 112403f4cb742c5df39538eb2d8d8fac629d3379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939810"
---
# <span data-ttu-id="a2c5c-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2c5c-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="a2c5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c5c-103">Sanal makineye ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2c5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2c5c-104">SYNTAX</span></span>

### <span data-ttu-id="a2c5c-105">GetNicFromNicId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2c5c-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c5c-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="a2c5c-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c5c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2c5c-107">DESCRIPTION</span></span>
<span data-ttu-id="a2c5c-108">**Add-Azurermvmnetworkınterface** cmdlet 'i sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="a2c5c-109">Sanal makine oluştururken veya mevcut bir sanal makineye bir arabirim eklediğinizde arabirim ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="a2c5c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2c5c-110">EXAMPLES</span></span>

### <span data-ttu-id="a2c5c-111">Örnek 1: yeni bir sanal makineye ağ arabirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="a2c5c-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="a2c5c-112">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a2c5c-113">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="a2c5c-114">İkinci komut $VirtualMachine depolanan sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="a2c5c-115">Örnek 2: var olan bir sanal makineye ağ arabirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="a2c5c-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="a2c5c-116">İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzureRmVM** cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="a2c5c-117">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="a2c5c-118">İkinci komut $VirtualMachine depolanan sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="a2c5c-119">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="a2c5c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2c5c-120">PARAMETERS</span></span>

### <span data-ttu-id="a2c5c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c5c-121">-DefaultProfile</span></span>
<span data-ttu-id="a2c5c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c5c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a2c5c-123">-Id</span></span>
<span data-ttu-id="a2c5c-124">Sanal makineye eklenecek ağ arabiriminin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="a2c5c-125">Ağ arabirimi edinmek için [Get-Azurermnetworkınterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c5c-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2c5c-126">-NetworkInterface</span></span>
<span data-ttu-id="a2c5c-127">Ağ arabirimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c5c-128">-Birincil</span><span class="sxs-lookup"><span data-stu-id="a2c5c-128">-Primary</span></span>
<span data-ttu-id="a2c5c-129">Bu cmdlet 'in ağ arabirimini birincil arabirim olarak eklediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c5c-130">-VM</span><span class="sxs-lookup"><span data-stu-id="a2c5c-130">-VM</span></span>
<span data-ttu-id="a2c5c-131">Ağ arabiriminin ekleneceği yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="a2c5c-132">Sanal makine oluşturmak için, **New-AzureRmVMConfig** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="a2c5c-133">Var olan bir sanal makineyi edinmek için **Get-AzureRmVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="a2c5c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c5c-134">CommonParameters</span></span>
<span data-ttu-id="a2c5c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2c5c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c5c-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c5c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c5c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2c5c-137">INPUTS</span></span>

### <span data-ttu-id="a2c5c-138">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface]</span><span class="sxs-lookup"><span data-stu-id="a2c5c-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="a2c5c-139">' NetworkInterface ' parametresi ' System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Network. model. PSNetworkInterface] ' türünün değerini ardışık düzene kabul eder</span><span class="sxs-lookup"><span data-stu-id="a2c5c-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="a2c5c-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a2c5c-140">PSVirtualMachine</span></span>
<span data-ttu-id="a2c5c-141">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a2c5c-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="a2c5c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2c5c-142">OUTPUTS</span></span>

### <span data-ttu-id="a2c5c-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a2c5c-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a2c5c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2c5c-144">NOTES</span></span>

## <span data-ttu-id="a2c5c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2c5c-145">RELATED LINKS</span></span>

[<span data-ttu-id="a2c5c-146">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="a2c5c-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="a2c5c-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a2c5c-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a2c5c-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a2c5c-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
