---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 6be4e505dfdacdc95e6ab3c9f7229fa4d1e470f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098042"
---
# <span data-ttu-id="e7a09-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7a09-101">Update-AzVM</span></span>

## <span data-ttu-id="e7a09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a09-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a09-103">Azure sanal makinesinin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="e7a09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7a09-104">SYNTAX</span></span>

### <span data-ttu-id="e7a09-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7a09-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a09-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a09-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a09-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a09-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a09-108">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="e7a09-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a09-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7a09-109">DESCRIPTION</span></span>
<span data-ttu-id="e7a09-110">**Update-AzVM** cmdlet 'i, bir Azure sanal makinesinin durumunu sanal makine nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="e7a09-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7a09-111">EXAMPLES</span></span>

### <span data-ttu-id="e7a09-112">Örnek 1: sanal makineyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e7a09-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="e7a09-113">Bu komut ResourceGroup11 'de sanal makineyi güncelleştirir $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e7a09-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="e7a09-114">Komut bunu, $VirtualMachine değişkeninde depolanan sanal makine nesnesini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e7a09-115">Sanal makine nesnesi edinmek için **Get-AzVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7a09-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="e7a09-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7a09-116">PARAMETERS</span></span>

### <span data-ttu-id="e7a09-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="e7a09-117">-AsJob</span></span>
<span data-ttu-id="e7a09-118">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="e7a09-118">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="e7a09-119">-AssignIdentity</span></span>
<span data-ttu-id="e7a09-120">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="e7a09-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="e7a09-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a09-121">-DefaultProfile</span></span>
<span data-ttu-id="e7a09-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7a09-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a09-123">-ID</span><span class="sxs-lookup"><span data-stu-id="e7a09-123">-Id</span></span>
<span data-ttu-id="e7a09-124">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-124">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e7a09-125">-IdentityId</span></span>
<span data-ttu-id="e7a09-126">Sanal makineyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="e7a09-127">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="e7a09-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e7a09-128">-IdentityType</span></span>
<span data-ttu-id="e7a09-129">Sanal makine için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="e7a09-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="e7a09-130">Geçerli değerler SystemAssigned, Useratandı, Systemassigneduseratandı ve None.</span><span class="sxs-lookup"><span data-stu-id="e7a09-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="e7a09-131">-MaxPrice</span></span>
<span data-ttu-id="e7a09-132">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="e7a09-133">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-133">This price is in US Dollars.</span></span> <span data-ttu-id="e7a09-134">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="e7a09-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="e7a09-135">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="e7a09-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="e7a09-136">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e7a09-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="e7a09-137">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="e7a09-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="e7a09-138">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="e7a09-138">Example: 0.01538.</span></span>  <span data-ttu-id="e7a09-139">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="e7a09-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="e7a09-140">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-140">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="e7a09-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e7a09-141">-NoWait</span></span>
<span data-ttu-id="e7a09-142">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="e7a09-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e7a09-143">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7a09-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e7a09-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="e7a09-145">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-146">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e7a09-146">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e7a09-147">Bu sanal makineyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e7a09-147">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a09-148">-ResourceGroupName</span></span>
<span data-ttu-id="e7a09-149">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-149">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e7a09-150">-Tag</span></span>
<span data-ttu-id="e7a09-151">Kaynaklar ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-151">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="e7a09-152">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="e7a09-152">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="e7a09-153">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-153">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-154">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="e7a09-154">-UltraSSDEnabled</span></span>
<span data-ttu-id="e7a09-155">VM 'deki UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak üzere bir veya daha fazla yönetilen veri diskine sahip olan bir bayrağı belirleyen bayrak.</span><span class="sxs-lookup"><span data-stu-id="e7a09-155">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="e7a09-156">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-156">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-157">-VM</span><span class="sxs-lookup"><span data-stu-id="e7a09-157">-VM</span></span>
<span data-ttu-id="e7a09-158">Yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-158">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="e7a09-159">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7a09-159">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="e7a09-160">Bu sanal makine nesnesi sanal makinenin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-160">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7a09-161">-Confirm</span></span>
<span data-ttu-id="e7a09-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7a09-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a09-163">-WhatIf</span></span>
<span data-ttu-id="e7a09-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7a09-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a09-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7a09-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a09-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a09-166">CommonParameters</span></span>
<span data-ttu-id="e7a09-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7a09-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a09-168">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7a09-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a09-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7a09-169">INPUTS</span></span>

### <span data-ttu-id="e7a09-170">System. String</span><span class="sxs-lookup"><span data-stu-id="e7a09-170">System.String</span></span>

### <span data-ttu-id="e7a09-171">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e7a09-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e7a09-172">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7a09-172">System.Boolean</span></span>

## <span data-ttu-id="e7a09-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7a09-173">OUTPUTS</span></span>

### <span data-ttu-id="e7a09-174">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e7a09-174">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e7a09-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7a09-175">NOTES</span></span>

## <span data-ttu-id="e7a09-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7a09-176">RELATED LINKS</span></span>

[<span data-ttu-id="e7a09-177">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7a09-177">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e7a09-178">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7a09-178">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e7a09-179">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7a09-179">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e7a09-180">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7a09-180">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e7a09-181">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7a09-181">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e7a09-182">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7a09-182">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e7a09-183">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e7a09-183">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


