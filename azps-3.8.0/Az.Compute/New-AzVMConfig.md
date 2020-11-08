---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: a53d8cc94ffcc34ddf32d9cfec3b543b0bd006e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096922"
---
# <span data-ttu-id="4be83-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4be83-101">New-AzVMConfig</span></span>

## <span data-ttu-id="4be83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4be83-102">SYNOPSIS</span></span>
<span data-ttu-id="4be83-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4be83-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="4be83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4be83-104">SYNTAX</span></span>

### <span data-ttu-id="4be83-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4be83-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be83-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4be83-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be83-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4be83-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4be83-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4be83-108">DESCRIPTION</span></span>
<span data-ttu-id="4be83-109">**New-AzVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4be83-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="4be83-110">Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-AzVMOSDisk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4be83-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="4be83-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4be83-111">EXAMPLES</span></span>

### <span data-ttu-id="4be83-112">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4be83-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="4be83-113">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4be83-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4be83-114">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4be83-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4be83-115">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="4be83-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4be83-116">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="4be83-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="4be83-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4be83-117">PARAMETERS</span></span>

### <span data-ttu-id="4be83-118">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="4be83-118">-AssignIdentity</span></span>
<span data-ttu-id="4be83-119">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="4be83-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="4be83-120">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="4be83-120">-AvailabilitySetId</span></span>
<span data-ttu-id="4be83-121">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be83-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="4be83-122">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4be83-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="4be83-123">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="4be83-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="4be83-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be83-124">-DefaultProfile</span></span>
<span data-ttu-id="4be83-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4be83-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4be83-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="4be83-126">-EnableUltraSSD</span></span>
<span data-ttu-id="4be83-127">VM 'de UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="4be83-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="4be83-128">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4be83-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="4be83-129">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="4be83-129">-EvictionPolicy</span></span>
<span data-ttu-id="4be83-130">Düşük öncelikli sanal makine için çıkarma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="4be83-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="4be83-131">Yalnızca desteklenen değer ' ayırması '.</span><span class="sxs-lookup"><span data-stu-id="4be83-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="4be83-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="4be83-132">-HostId</span></span>
<span data-ttu-id="4be83-133">Ana bilgisayar kimliği</span><span class="sxs-lookup"><span data-stu-id="4be83-133">The Id of Host</span></span>

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

### <span data-ttu-id="4be83-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4be83-134">-IdentityId</span></span>
<span data-ttu-id="4be83-135">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be83-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4be83-136">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="4be83-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="4be83-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4be83-137">-IdentityType</span></span>
<span data-ttu-id="4be83-138">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="4be83-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="4be83-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4be83-139">-LicenseType</span></span>
<span data-ttu-id="4be83-140">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="4be83-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="4be83-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="4be83-141">-MaxPrice</span></span>
<span data-ttu-id="4be83-142">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be83-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="4be83-143">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="4be83-143">This price is in US Dollars.</span></span> <span data-ttu-id="4be83-144">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="4be83-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="4be83-145">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="4be83-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="4be83-146">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="4be83-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="4be83-147">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="4be83-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="4be83-148">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="4be83-148">Example: 0.01538.</span></span>  <span data-ttu-id="4be83-149">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4be83-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="4be83-150">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="4be83-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="4be83-151">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="4be83-151">-Priority</span></span>
<span data-ttu-id="4be83-152">Sanal makinenin önceliği.</span><span class="sxs-lookup"><span data-stu-id="4be83-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="4be83-153">Yalnızca desteklenen değerler ' Regular ', ' nokta ' ve ' düşük ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="4be83-153">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="4be83-154">' Regular ' normal sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="4be83-154">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="4be83-155">' Spot ', spot sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="4be83-155">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="4be83-156">' Low ', spot sanal makine için de, ancak ' nokta ' ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4be83-156">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="4be83-157">Lütfen ' düşük ' yerine ' nokta ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="4be83-157">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="4be83-158">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4be83-158">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4be83-159">Bu sanal makineyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4be83-159">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="4be83-160">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="4be83-160">-Tags</span></span>
<span data-ttu-id="4be83-161">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="4be83-161">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="4be83-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="4be83-162">-VMName</span></span>
<span data-ttu-id="4be83-163">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be83-163">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="4be83-164">-VMSize</span><span class="sxs-lookup"><span data-stu-id="4be83-164">-VMSize</span></span>
<span data-ttu-id="4be83-165">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be83-165">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="4be83-166">-VmssId</span><span class="sxs-lookup"><span data-stu-id="4be83-166">-VmssId</span></span>
<span data-ttu-id="4be83-167">Sanal makine ölçek kümesi kimliği</span><span class="sxs-lookup"><span data-stu-id="4be83-167">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="4be83-168">-Bölge</span><span class="sxs-lookup"><span data-stu-id="4be83-168">-Zone</span></span>
<span data-ttu-id="4be83-169">Sanal makinenin kullanılabilirlik bölgesi listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be83-169">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="4be83-170">İzin verilen değerler, bölgenin yeteneklerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4be83-170">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="4be83-171">İzin verilen değerler normalde 1, 2, 3 olur.</span><span class="sxs-lookup"><span data-stu-id="4be83-171">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="4be83-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be83-172">CommonParameters</span></span>
<span data-ttu-id="4be83-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4be83-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be83-174">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4be83-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be83-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4be83-175">INPUTS</span></span>

### <span data-ttu-id="4be83-176">System. String</span><span class="sxs-lookup"><span data-stu-id="4be83-176">System.String</span></span>

### <span data-ttu-id="4be83-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="4be83-177">System.String[]</span></span>

### <span data-ttu-id="4be83-178">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4be83-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4be83-179">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4be83-179">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4be83-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4be83-180">OUTPUTS</span></span>

### <span data-ttu-id="4be83-181">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4be83-181">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4be83-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4be83-182">NOTES</span></span>

## <span data-ttu-id="4be83-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4be83-183">RELATED LINKS</span></span>

[<span data-ttu-id="4be83-184">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4be83-184">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="4be83-185">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4be83-185">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="4be83-186">Set-Azvmsourceımage</span><span class="sxs-lookup"><span data-stu-id="4be83-186">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="4be83-187">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4be83-187">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


