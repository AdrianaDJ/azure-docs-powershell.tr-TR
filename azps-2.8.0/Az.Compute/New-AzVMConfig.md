---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 5dda2e33496e3391d55e7be20348fef681bc22b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752834"
---
# <span data-ttu-id="be9a4-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="be9a4-101">New-AzVMConfig</span></span>

## <span data-ttu-id="be9a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="be9a4-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be9a4-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="be9a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be9a4-104">SYNTAX</span></span>

### <span data-ttu-id="be9a4-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be9a4-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be9a4-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="be9a4-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be9a4-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="be9a4-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be9a4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="be9a4-108">DESCRIPTION</span></span>
<span data-ttu-id="be9a4-109">**New-AzVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be9a4-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="be9a4-110">Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-AzVMOSDisk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="be9a4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be9a4-111">EXAMPLES</span></span>

### <span data-ttu-id="be9a4-112">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="be9a4-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="be9a4-113">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="be9a4-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="be9a4-114">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="be9a4-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="be9a4-115">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="be9a4-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="be9a4-116">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="be9a4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be9a4-117">PARAMETERS</span></span>

### <span data-ttu-id="be9a4-118">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="be9a4-118">-AssignIdentity</span></span>
<span data-ttu-id="be9a4-119">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="be9a4-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be9a4-120">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="be9a4-120">-AvailabilitySetId</span></span>
<span data-ttu-id="be9a4-121">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="be9a4-122">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="be9a4-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="be9a4-123">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="be9a4-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="be9a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be9a4-124">-DefaultProfile</span></span>
<span data-ttu-id="be9a4-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be9a4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be9a4-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="be9a4-126">-EnableUltraSSD</span></span>
<span data-ttu-id="be9a4-127">VM 'de UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="be9a4-128">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="be9a4-129">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="be9a4-129">-EvictionPolicy</span></span>
<span data-ttu-id="be9a4-130">Düşük öncelikli sanal makine için çıkarma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="be9a4-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="be9a4-131">Yalnızca desteklenen değer ' ayırması '.</span><span class="sxs-lookup"><span data-stu-id="be9a4-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="be9a4-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="be9a4-132">-HostId</span></span>
<span data-ttu-id="be9a4-133">Ana bilgisayar kimliği</span><span class="sxs-lookup"><span data-stu-id="be9a4-133">The Id of Host</span></span>

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

### <span data-ttu-id="be9a4-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="be9a4-134">-IdentityId</span></span>
<span data-ttu-id="be9a4-135">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="be9a4-136">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="be9a4-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="be9a4-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="be9a4-137">-IdentityType</span></span>
<span data-ttu-id="be9a4-138">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="be9a4-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="be9a4-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="be9a4-139">-LicenseType</span></span>
<span data-ttu-id="be9a4-140">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="be9a4-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="be9a4-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="be9a4-141">-MaxPrice</span></span>
<span data-ttu-id="be9a4-142">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="be9a4-143">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-143">This price is in US Dollars.</span></span> <span data-ttu-id="be9a4-144">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="be9a4-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="be9a4-145">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="be9a4-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="be9a4-146">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="be9a4-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="be9a4-147">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="be9a4-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="be9a4-148">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="be9a4-148">Example: 0.01538.</span></span>  <span data-ttu-id="be9a4-149">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="be9a4-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="be9a4-150">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="be9a4-151">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="be9a4-151">-Priority</span></span>
<span data-ttu-id="be9a4-152">Sanal makinenin önceliği.</span><span class="sxs-lookup"><span data-stu-id="be9a4-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="be9a4-153">Yalnızca desteklenen değerler ' Regular ' ve ' Low ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-153">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="be9a4-154">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="be9a4-154">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="be9a4-155">ProximityPlacementGroup kimliği</span><span class="sxs-lookup"><span data-stu-id="be9a4-155">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="be9a4-156">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="be9a4-156">-Tags</span></span>
<span data-ttu-id="be9a4-157">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="be9a4-157">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="be9a4-158">-VMName</span><span class="sxs-lookup"><span data-stu-id="be9a4-158">-VMName</span></span>
<span data-ttu-id="be9a4-159">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-159">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="be9a4-160">-VMSize</span><span class="sxs-lookup"><span data-stu-id="be9a4-160">-VMSize</span></span>
<span data-ttu-id="be9a4-161">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-161">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="be9a4-162">-VmssId</span><span class="sxs-lookup"><span data-stu-id="be9a4-162">-VmssId</span></span>
<span data-ttu-id="be9a4-163">Sanal makine ölçek kümesi kimliği</span><span class="sxs-lookup"><span data-stu-id="be9a4-163">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="be9a4-164">-Bölge</span><span class="sxs-lookup"><span data-stu-id="be9a4-164">-Zone</span></span>
<span data-ttu-id="be9a4-165">Sanal makinenin kullanılabilirlik bölgesi listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be9a4-165">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="be9a4-166">İzin verilen değerler, bölgenin yeteneklerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be9a4-166">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="be9a4-167">İzin verilen değerler normalde 1, 2, 3 olur.</span><span class="sxs-lookup"><span data-stu-id="be9a4-167">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="be9a4-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be9a4-168">CommonParameters</span></span>
<span data-ttu-id="be9a4-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be9a4-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be9a4-170">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be9a4-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be9a4-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be9a4-171">INPUTS</span></span>

### <span data-ttu-id="be9a4-172">System. String</span><span class="sxs-lookup"><span data-stu-id="be9a4-172">System.String</span></span>

### <span data-ttu-id="be9a4-173">System. String []</span><span class="sxs-lookup"><span data-stu-id="be9a4-173">System.String[]</span></span>

### <span data-ttu-id="be9a4-174">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="be9a4-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="be9a4-175">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="be9a4-175">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be9a4-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be9a4-176">OUTPUTS</span></span>

### <span data-ttu-id="be9a4-177">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="be9a4-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="be9a4-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be9a4-178">NOTES</span></span>

## <span data-ttu-id="be9a4-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be9a4-179">RELATED LINKS</span></span>

[<span data-ttu-id="be9a4-180">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="be9a4-180">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="be9a4-181">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="be9a4-181">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="be9a4-182">Set-Azvmsourceımage</span><span class="sxs-lookup"><span data-stu-id="be9a4-182">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="be9a4-183">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="be9a4-183">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


