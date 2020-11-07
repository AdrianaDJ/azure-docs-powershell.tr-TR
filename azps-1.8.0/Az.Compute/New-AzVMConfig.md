---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761306"
---
# <span data-ttu-id="2280d-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2280d-101">New-AzVMConfig</span></span>

## <span data-ttu-id="2280d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2280d-102">SYNOPSIS</span></span>
<span data-ttu-id="2280d-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2280d-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="2280d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2280d-104">SYNTAX</span></span>

### <span data-ttu-id="2280d-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2280d-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2280d-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2280d-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2280d-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2280d-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2280d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2280d-108">DESCRIPTION</span></span>
<span data-ttu-id="2280d-109">**New-AzVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2280d-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="2280d-110">Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-AzVMOSDisk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2280d-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="2280d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2280d-111">EXAMPLES</span></span>

### <span data-ttu-id="2280d-112">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2280d-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="2280d-113">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2280d-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2280d-114">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2280d-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2280d-115">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="2280d-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2280d-116">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="2280d-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="2280d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2280d-117">PARAMETERS</span></span>

### <span data-ttu-id="2280d-118">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="2280d-118">-AssignIdentity</span></span>
<span data-ttu-id="2280d-119">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="2280d-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="2280d-120">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="2280d-120">-AvailabilitySetId</span></span>
<span data-ttu-id="2280d-121">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2280d-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="2280d-122">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2280d-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="2280d-123">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="2280d-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="2280d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2280d-124">-DefaultProfile</span></span>
<span data-ttu-id="2280d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2280d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2280d-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="2280d-126">-EnableUltraSSD</span></span>
<span data-ttu-id="2280d-127">VM 'de UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="2280d-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="2280d-128">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="2280d-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="2280d-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="2280d-129">-IdentityId</span></span>
<span data-ttu-id="2280d-130">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2280d-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2280d-131">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="2280d-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="2280d-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2280d-132">-IdentityType</span></span>
<span data-ttu-id="2280d-133">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="2280d-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="2280d-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2280d-134">-LicenseType</span></span>
<span data-ttu-id="2280d-135">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="2280d-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="2280d-136">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="2280d-136">-Tags</span></span>
<span data-ttu-id="2280d-137">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="2280d-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="2280d-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="2280d-138">-VMName</span></span>
<span data-ttu-id="2280d-139">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="2280d-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="2280d-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="2280d-140">-VMSize</span></span>
<span data-ttu-id="2280d-141">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2280d-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="2280d-142">-Bölge</span><span class="sxs-lookup"><span data-stu-id="2280d-142">-Zone</span></span>
<span data-ttu-id="2280d-143">Sanal makinenin kullanılabilirlik bölgesi listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2280d-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="2280d-144">İzin verilen değerler, bölgenin yeteneklerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2280d-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="2280d-145">İzin verilen değerler normalde 1, 2, 3 olur.</span><span class="sxs-lookup"><span data-stu-id="2280d-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="2280d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2280d-146">CommonParameters</span></span>
<span data-ttu-id="2280d-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2280d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2280d-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2280d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2280d-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2280d-149">INPUTS</span></span>

### <span data-ttu-id="2280d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2280d-150">System.String</span></span>

### <span data-ttu-id="2280d-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="2280d-151">System.String[]</span></span>

### <span data-ttu-id="2280d-152">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2280d-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2280d-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2280d-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2280d-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2280d-154">OUTPUTS</span></span>

### <span data-ttu-id="2280d-155">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2280d-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2280d-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2280d-156">NOTES</span></span>

## <span data-ttu-id="2280d-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2280d-157">RELATED LINKS</span></span>

[<span data-ttu-id="2280d-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2280d-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="2280d-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2280d-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="2280d-160">Set-Azvmsourceımage</span><span class="sxs-lookup"><span data-stu-id="2280d-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="2280d-161">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2280d-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

