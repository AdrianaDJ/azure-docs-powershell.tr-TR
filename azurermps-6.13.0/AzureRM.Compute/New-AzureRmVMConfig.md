---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592042"
---
# <span data-ttu-id="046e9-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="046e9-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="046e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="046e9-102">SYNOPSIS</span></span>
<span data-ttu-id="046e9-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="046e9-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="046e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="046e9-104">SYNTAX</span></span>

### <span data-ttu-id="046e9-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="046e9-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="046e9-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="046e9-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="046e9-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="046e9-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="046e9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="046e9-108">DESCRIPTION</span></span>
<span data-ttu-id="046e9-109">**Yeni-AzureRmVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="046e9-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="046e9-110">Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="046e9-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="046e9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="046e9-111">EXAMPLES</span></span>

### <span data-ttu-id="046e9-112">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="046e9-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="046e9-113">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="046e9-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="046e9-114">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="046e9-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="046e9-115">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="046e9-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="046e9-116">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="046e9-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="046e9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="046e9-117">PARAMETERS</span></span>

### <span data-ttu-id="046e9-118">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="046e9-118">-AssignIdentity</span></span>
<span data-ttu-id="046e9-119">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="046e9-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="046e9-120">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="046e9-120">-AvailabilitySetId</span></span>
<span data-ttu-id="046e9-121">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="046e9-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="046e9-122">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzureRmAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="046e9-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="046e9-123">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="046e9-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="046e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046e9-124">-DefaultProfile</span></span>
<span data-ttu-id="046e9-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="046e9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046e9-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="046e9-126">-EnableUltraSSD</span></span>
<span data-ttu-id="046e9-127">VM 'de UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="046e9-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="046e9-128">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="046e9-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="046e9-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="046e9-129">-IdentityId</span></span>
<span data-ttu-id="046e9-130">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="046e9-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="046e9-131">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="046e9-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="046e9-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="046e9-132">-IdentityType</span></span>
<span data-ttu-id="046e9-133">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="046e9-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="046e9-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="046e9-134">-LicenseType</span></span>
<span data-ttu-id="046e9-135">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="046e9-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="046e9-136">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="046e9-136">-Tags</span></span>
<span data-ttu-id="046e9-137">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="046e9-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="046e9-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="046e9-138">-VMName</span></span>
<span data-ttu-id="046e9-139">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="046e9-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="046e9-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="046e9-140">-VMSize</span></span>
<span data-ttu-id="046e9-141">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="046e9-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="046e9-142">-Bölge</span><span class="sxs-lookup"><span data-stu-id="046e9-142">-Zone</span></span>
<span data-ttu-id="046e9-143">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="046e9-143">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="046e9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046e9-144">CommonParameters</span></span>
<span data-ttu-id="046e9-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="046e9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046e9-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046e9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046e9-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="046e9-147">INPUTS</span></span>

### <span data-ttu-id="046e9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="046e9-148">System.String</span></span>

### <span data-ttu-id="046e9-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="046e9-149">System.String[]</span></span>

### <span data-ttu-id="046e9-150">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="046e9-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="046e9-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="046e9-151">OUTPUTS</span></span>

### <span data-ttu-id="046e9-152">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="046e9-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="046e9-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="046e9-153">NOTES</span></span>

## <span data-ttu-id="046e9-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="046e9-154">RELATED LINKS</span></span>

[<span data-ttu-id="046e9-155">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="046e9-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="046e9-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="046e9-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="046e9-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="046e9-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="046e9-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="046e9-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


