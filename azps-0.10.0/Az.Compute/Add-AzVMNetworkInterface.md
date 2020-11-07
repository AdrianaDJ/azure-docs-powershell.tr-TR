---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: aaf1162cdeeb007a680a3e9de325cbd10fadef94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937095"
---
# <span data-ttu-id="ab166-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ab166-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="ab166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab166-102">SYNOPSIS</span></span>
<span data-ttu-id="ab166-103">Sanal makineye ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="ab166-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="ab166-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab166-104">SYNTAX</span></span>

### <span data-ttu-id="ab166-105">GetNicFromNicId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ab166-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab166-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="ab166-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab166-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab166-107">DESCRIPTION</span></span>
<span data-ttu-id="ab166-108">**Add-Azvmnetworkınterface** cmdlet 'i sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="ab166-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="ab166-109">Sanal makine oluştururken veya mevcut bir sanal makineye bir arabirim eklediğinizde arabirim ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab166-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="ab166-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab166-110">EXAMPLES</span></span>

### <span data-ttu-id="ab166-111">Örnek 1: yeni bir sanal makineye ağ arabirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="ab166-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="ab166-112">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ab166-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ab166-113">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="ab166-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="ab166-114">İkinci komut $VirtualMachine depolanan sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="ab166-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="ab166-115">Örnek 2: var olan bir sanal makineye ağ arabirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="ab166-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="ab166-116">İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzVM** cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="ab166-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="ab166-117">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="ab166-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ab166-118">İkinci komut $VirtualMachine depolanan sanal makineye bir ağ arabirimi ekler.</span><span class="sxs-lookup"><span data-stu-id="ab166-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="ab166-119">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ab166-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="ab166-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab166-120">PARAMETERS</span></span>

### <span data-ttu-id="ab166-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab166-121">-DefaultProfile</span></span>
<span data-ttu-id="ab166-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab166-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab166-123">-ID</span><span class="sxs-lookup"><span data-stu-id="ab166-123">-Id</span></span>
<span data-ttu-id="ab166-124">Sanal makineye eklenecek ağ arabiriminin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab166-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="ab166-125">Ağ arabirimi edinmek için [Get-Aznetworkınterface](/powershell/module/azurerm.network/get-aznetworkinterface) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab166-125">You can use the [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="ab166-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ab166-126">-NetworkInterface</span></span>
<span data-ttu-id="ab166-127">Ağ arabirimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab166-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="ab166-128">-Birincil</span><span class="sxs-lookup"><span data-stu-id="ab166-128">-Primary</span></span>
<span data-ttu-id="ab166-129">Bu cmdlet 'in ağ arabirimini birincil arabirim olarak eklediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab166-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="ab166-130">-VM</span><span class="sxs-lookup"><span data-stu-id="ab166-130">-VM</span></span>
<span data-ttu-id="ab166-131">Ağ arabiriminin ekleneceği yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab166-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="ab166-132">Sanal makine oluşturmak için, **New-AzVMConfig** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ab166-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="ab166-133">Var olan bir sanal makineyi edinmek için **Get-AzVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ab166-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

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

### <span data-ttu-id="ab166-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab166-134">CommonParameters</span></span>
<span data-ttu-id="ab166-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab166-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab166-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab166-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab166-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab166-137">INPUTS</span></span>

### <span data-ttu-id="ab166-138">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface]</span><span class="sxs-lookup"><span data-stu-id="ab166-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="ab166-139">' NetworkInterface ' parametresi ' System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Network. model. PSNetworkInterface] ' türünün değerini ardışık düzene kabul eder</span><span class="sxs-lookup"><span data-stu-id="ab166-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="ab166-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ab166-140">PSVirtualMachine</span></span>
<span data-ttu-id="ab166-141">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ab166-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ab166-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab166-142">OUTPUTS</span></span>

### <span data-ttu-id="ab166-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ab166-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ab166-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab166-144">NOTES</span></span>

## <span data-ttu-id="ab166-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab166-145">RELATED LINKS</span></span>

[<span data-ttu-id="ab166-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ab166-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="ab166-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab166-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ab166-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ab166-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
