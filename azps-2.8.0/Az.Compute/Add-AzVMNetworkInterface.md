---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3ac2a0ba40b7bcd6b845bd069fced292e959cba5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752996"
---
# <span data-ttu-id="db71e-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db71e-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="db71e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db71e-102">SYNOPSIS</span></span>
<span data-ttu-id="db71e-103">Sanal makineye ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="db71e-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="db71e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db71e-104">SYNTAX</span></span>

### <span data-ttu-id="db71e-105">GetNicFromNicId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db71e-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db71e-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="db71e-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db71e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="db71e-107">DESCRIPTION</span></span>
<span data-ttu-id="db71e-108">**Add-Azvmnetworkınterface** cmdlet 'i sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="db71e-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="db71e-109">Sanal makine oluştururken veya mevcut bir sanal makineye bir arabirim eklediğinizde arabirim ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db71e-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="db71e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db71e-110">EXAMPLES</span></span>

### <span data-ttu-id="db71e-111">Örnek 1: yeni bir sanal makineye ağ arabirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="db71e-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="db71e-112">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="db71e-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="db71e-113">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="db71e-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="db71e-114">İkinci komut $VirtualMachine depolanan sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="db71e-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="db71e-115">Örnek 2: var olan bir sanal makineye ağ arabirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="db71e-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="db71e-116">İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzVM** cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="db71e-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="db71e-117">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="db71e-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="db71e-118">İkinci komut $VirtualMachine depolanan sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="db71e-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="db71e-119">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="db71e-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="db71e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db71e-120">PARAMETERS</span></span>

### <span data-ttu-id="db71e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db71e-121">-DefaultProfile</span></span>
<span data-ttu-id="db71e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db71e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db71e-123">-ID</span><span class="sxs-lookup"><span data-stu-id="db71e-123">-Id</span></span>
<span data-ttu-id="db71e-124">Sanal makineye eklenecek ağ arabiriminin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="db71e-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="db71e-125">Ağ arabirimi edinmek için [Get-Aznetworkınterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db71e-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db71e-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db71e-126">-NetworkInterface</span></span>
<span data-ttu-id="db71e-127">Ağ arabirimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db71e-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="db71e-128">-Birincil</span><span class="sxs-lookup"><span data-stu-id="db71e-128">-Primary</span></span>
<span data-ttu-id="db71e-129">Bu cmdlet 'in ağ arabirimini birincil arabirim olarak eklediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db71e-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db71e-130">-VM</span><span class="sxs-lookup"><span data-stu-id="db71e-130">-VM</span></span>
<span data-ttu-id="db71e-131">Ağ arabiriminin ekleneceği yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db71e-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="db71e-132">Sanal makine oluşturmak için, **New-AzVMConfig** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="db71e-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="db71e-133">Var olan bir sanal makineyi edinmek için **Get-AzVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="db71e-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

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

### <span data-ttu-id="db71e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db71e-134">CommonParameters</span></span>
<span data-ttu-id="db71e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db71e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db71e-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db71e-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db71e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db71e-137">INPUTS</span></span>

### <span data-ttu-id="db71e-138">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db71e-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="db71e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="db71e-139">System.String</span></span>

### <span data-ttu-id="db71e-140">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="db71e-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="db71e-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db71e-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db71e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db71e-142">OUTPUTS</span></span>

### <span data-ttu-id="db71e-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db71e-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="db71e-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db71e-144">NOTES</span></span>

## <span data-ttu-id="db71e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db71e-145">RELATED LINKS</span></span>

[<span data-ttu-id="db71e-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="db71e-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="db71e-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="db71e-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="db71e-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="db71e-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
