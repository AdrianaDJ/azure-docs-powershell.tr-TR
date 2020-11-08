---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267896"
---
# <span data-ttu-id="9bd3f-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9bd3f-101">New-AzVMConfig</span></span>

## <span data-ttu-id="9bd3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd3f-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="9bd3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bd3f-104">SYNTAX</span></span>

### <span data-ttu-id="9bd3f-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9bd3f-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd3f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd3f-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd3f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bd3f-107">DESCRIPTION</span></span>
<span data-ttu-id="9bd3f-108">**New-AzVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="9bd3f-109">Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-AzVMOSDisk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="9bd3f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bd3f-110">EXAMPLES</span></span>

### <span data-ttu-id="9bd3f-111">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9bd3f-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="9bd3f-112">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="9bd3f-113">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9bd3f-114">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9bd3f-115">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="9bd3f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bd3f-116">PARAMETERS</span></span>

### <span data-ttu-id="9bd3f-117">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="9bd3f-117">-AvailabilitySetId</span></span>
<span data-ttu-id="9bd3f-118">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="9bd3f-119">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="9bd3f-120">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="9bd3f-121">Aynı Kullanılabilirlik kümesinde belirtilen sanal makineler, kullanılabilirliği en üst düzeye çıkarmak için farklı düğümlere tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="9bd3f-122">Kullanılabilirlik kümeleri hakkında daha fazla bilgi için bkz: [sanal makinelerin kullanılabilirliğini yönetme](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="9bd3f-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="9bd3f-123">Azure planlı bakımı hakkında daha fazla bilgi için, [Azure 'da sanal makinelerin planlı Bakımı](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) konusuna bakın</span><span class="sxs-lookup"><span data-stu-id="9bd3f-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="9bd3f-124">Şu anda, bir VM yalnızca Oluşturulma sırasında kullanılabilirlik kümesine eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="9bd3f-125">VM 'nin eklendiği kullanılabilirlik kümesi, kullanılabilirlik kümesi kaynağıyla aynı kaynak grubunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="9bd3f-126">Mevcut bir VM, kullanılabilirlik kümesine eklenemez.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="9bd3f-127">Bu özellik, null olmayan özellikler. virtualMachineScaleSet başvurusu ile birlikte olamaz.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="9bd3f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd3f-128">-DefaultProfile</span></span>
<span data-ttu-id="9bd3f-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bd3f-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="9bd3f-130">-EnableUltraSSD</span></span>
<span data-ttu-id="9bd3f-131">VM 'de UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="9bd3f-132">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-133">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="9bd3f-133">-EvictionPolicy</span></span>
<span data-ttu-id="9bd3f-134">Azure spot sanal makinesi için çıkarma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="9bd3f-135">Desteklenen değerler ' ayırması ' ve ' Sil ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="9bd3f-136">-HostId</span></span>
<span data-ttu-id="9bd3f-137">Ana bilgisayar kimliği</span><span class="sxs-lookup"><span data-stu-id="9bd3f-137">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="9bd3f-138">-IdentityId</span></span>
<span data-ttu-id="9bd3f-139">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="9bd3f-140">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="9bd3f-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9bd3f-141">-IdentityType</span></span>
<span data-ttu-id="9bd3f-142">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9bd3f-143">-LicenseType</span></span>
<span data-ttu-id="9bd3f-144">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-144">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="9bd3f-145">-MaxPrice</span></span>
<span data-ttu-id="9bd3f-146">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="9bd3f-147">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-147">This price is in US Dollars.</span></span> <span data-ttu-id="9bd3f-148">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="9bd3f-149">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="9bd3f-150">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="9bd3f-151">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="9bd3f-152">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-152">Example: 0.01538.</span></span>  <span data-ttu-id="9bd3f-153">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="9bd3f-154">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-154">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="9bd3f-155">-EncryptionAtHost</span></span>
<span data-ttu-id="9bd3f-156">EncryptionAtHost özelliği, sanal makine veya sanal makine ölçek kümesi için konak şifrelemeyi etkinleştirmek veya devre dışı bırakmak amacıyla istekte bulunan Kullanıcı tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="9bd3f-157">Bu, konaktaki kaynak/Temp diski dahil tüm disklerde şifrelemeyi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="9bd3f-158">Varsayılan: Bu özellik kaynak için doğru olarak ayarlanmadıkça konaktaki şifreleme devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-159">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="9bd3f-159">-Priority</span></span>
<span data-ttu-id="9bd3f-160">Sanal makinenin önceliği.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="9bd3f-161">Yalnızca desteklenen değerler ' Regular ', ' nokta ' ve ' düşük ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="9bd3f-162">' Regular ' normal sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="9bd3f-163">' Spot ', spot sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="9bd3f-164">' Low ', spot sanal makine için de, ancak ' nokta ' ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="9bd3f-165">Lütfen ' düşük ' yerine ' nokta ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-165">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="9bd3f-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="9bd3f-167">Bu sanal makineyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-168">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="9bd3f-168">-Tags</span></span>
<span data-ttu-id="9bd3f-169">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-169">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="9bd3f-170">-VMName</span></span>
<span data-ttu-id="9bd3f-171">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-171">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="9bd3f-172">-VMSize</span></span>
<span data-ttu-id="9bd3f-173">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-173">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="9bd3f-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="9bd3f-174">-VmssId</span></span>
<span data-ttu-id="9bd3f-175">Sanal makine ölçek kümesi kimliği</span><span class="sxs-lookup"><span data-stu-id="9bd3f-175">The Id of virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-176">-Bölge</span><span class="sxs-lookup"><span data-stu-id="9bd3f-176">-Zone</span></span>
<span data-ttu-id="9bd3f-177">Sanal makinenin kullanılabilirlik bölgesi listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="9bd3f-178">İzin verilen değerler, bölgenin yeteneklerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="9bd3f-179">İzin verilen değerler normalde 1, 2, 3 olur.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-179">Allowed values will normally be 1,2,3.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd3f-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd3f-180">CommonParameters</span></span>
<span data-ttu-id="9bd3f-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd3f-182">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9bd3f-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd3f-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bd3f-183">INPUTS</span></span>

### <span data-ttu-id="9bd3f-184">System. String</span><span class="sxs-lookup"><span data-stu-id="9bd3f-184">System.String</span></span>

### <span data-ttu-id="9bd3f-185">System. String []</span><span class="sxs-lookup"><span data-stu-id="9bd3f-185">System.String[]</span></span>

### <span data-ttu-id="9bd3f-186">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9bd3f-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9bd3f-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9bd3f-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9bd3f-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bd3f-188">OUTPUTS</span></span>

### <span data-ttu-id="9bd3f-189">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9bd3f-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9bd3f-190">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bd3f-190">NOTES</span></span>

## <span data-ttu-id="9bd3f-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bd3f-191">RELATED LINKS</span></span>

[<span data-ttu-id="9bd3f-192">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9bd3f-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="9bd3f-193">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9bd3f-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="9bd3f-194">Set-Azvmsourceımage</span><span class="sxs-lookup"><span data-stu-id="9bd3f-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="9bd3f-195">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9bd3f-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


