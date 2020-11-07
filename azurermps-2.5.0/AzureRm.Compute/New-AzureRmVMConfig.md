---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
ms.openlocfilehash: 3e42cf7c2be8433d9e1b7e85987e53b9f0050038
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939787"
---
# <span data-ttu-id="25826-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="25826-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="25826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25826-102">SYNOPSIS</span></span>
<span data-ttu-id="25826-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25826-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25826-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25826-104">SYNTAX</span></span>

### <span data-ttu-id="25826-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25826-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25826-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="25826-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25826-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="25826-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25826-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="25826-108">DESCRIPTION</span></span>
<span data-ttu-id="25826-109">**Yeni-AzureRmVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25826-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="25826-110">Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="25826-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="25826-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25826-111">EXAMPLES</span></span>

### <span data-ttu-id="25826-112">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="25826-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="25826-113">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="25826-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="25826-114">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="25826-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="25826-115">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="25826-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="25826-116">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="25826-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="25826-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25826-117">PARAMETERS</span></span>

### <span data-ttu-id="25826-118">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="25826-118">-AssignIdentity</span></span>
<span data-ttu-id="25826-119">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="25826-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25826-120">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="25826-120">-AvailabilitySetId</span></span>
<span data-ttu-id="25826-121">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="25826-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="25826-122">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzureRmAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="25826-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="25826-123">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="25826-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25826-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25826-124">-DefaultProfile</span></span>
<span data-ttu-id="25826-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25826-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25826-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="25826-126">-IdentityId</span></span>
<span data-ttu-id="25826-127">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25826-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="25826-128">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="25826-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25826-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="25826-129">-IdentityType</span></span>
<span data-ttu-id="25826-130">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="25826-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25826-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="25826-131">-LicenseType</span></span>
<span data-ttu-id="25826-132">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="25826-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25826-133">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="25826-133">-Tags</span></span>
<span data-ttu-id="25826-134">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="25826-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25826-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="25826-135">-VMName</span></span>
<span data-ttu-id="25826-136">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="25826-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25826-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="25826-137">-VMSize</span></span>
<span data-ttu-id="25826-138">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="25826-138">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25826-139">-Bölge</span><span class="sxs-lookup"><span data-stu-id="25826-139">-Zone</span></span>
<span data-ttu-id="25826-140">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25826-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25826-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25826-141">CommonParameters</span></span>
<span data-ttu-id="25826-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25826-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25826-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25826-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25826-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25826-144">INPUTS</span></span>

### <span data-ttu-id="25826-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="25826-145">None</span></span>
<span data-ttu-id="25826-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="25826-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25826-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25826-147">OUTPUTS</span></span>

### <span data-ttu-id="25826-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="25826-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="25826-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25826-149">NOTES</span></span>

## <span data-ttu-id="25826-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25826-150">RELATED LINKS</span></span>

[<span data-ttu-id="25826-151">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="25826-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="25826-152">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="25826-152">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="25826-153">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="25826-153">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="25826-154">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="25826-154">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


