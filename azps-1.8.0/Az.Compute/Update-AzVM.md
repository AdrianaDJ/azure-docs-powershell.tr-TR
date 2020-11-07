---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917176"
---
# <span data-ttu-id="698b2-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="698b2-101">Update-AzVM</span></span>

## <span data-ttu-id="698b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="698b2-102">SYNOPSIS</span></span>
<span data-ttu-id="698b2-103">Azure sanal makinesinin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="698b2-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="698b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="698b2-104">SYNTAX</span></span>

### <span data-ttu-id="698b2-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="698b2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="698b2-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="698b2-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="698b2-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="698b2-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="698b2-108">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="698b2-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="698b2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="698b2-109">DESCRIPTION</span></span>
<span data-ttu-id="698b2-110">**Update-AzVM** cmdlet 'i, bir Azure sanal makinesinin durumunu sanal makine nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="698b2-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="698b2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="698b2-111">EXAMPLES</span></span>

### <span data-ttu-id="698b2-112">Örnek 1: sanal makineyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="698b2-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="698b2-113">Bu komut ResourceGroup11 'de sanal makineyi güncelleştirir $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="698b2-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="698b2-114">Komut bunu, $VirtualMachine değişkeninde depolanan sanal makine nesnesini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="698b2-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="698b2-115">Sanal makine nesnesi edinmek için **Get-AzVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="698b2-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="698b2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="698b2-116">PARAMETERS</span></span>

### <span data-ttu-id="698b2-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="698b2-117">-AsJob</span></span>
<span data-ttu-id="698b2-118">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="698b2-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="698b2-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="698b2-119">-AssignIdentity</span></span>
<span data-ttu-id="698b2-120">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="698b2-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="698b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698b2-121">-DefaultProfile</span></span>
<span data-ttu-id="698b2-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="698b2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="698b2-123">-ID</span><span class="sxs-lookup"><span data-stu-id="698b2-123">-Id</span></span>
<span data-ttu-id="698b2-124">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="698b2-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="698b2-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="698b2-125">-IdentityId</span></span>
<span data-ttu-id="698b2-126">Sanal makineyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="698b2-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="698b2-127">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="698b2-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="698b2-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="698b2-128">-IdentityType</span></span>
<span data-ttu-id="698b2-129">Sanal makine için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="698b2-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="698b2-130">Geçerli değerler SystemAssigned, Useratandı, Systemassigneduseratandı ve None.</span><span class="sxs-lookup"><span data-stu-id="698b2-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="698b2-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="698b2-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="698b2-132">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="698b2-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="698b2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698b2-133">-ResourceGroupName</span></span>
<span data-ttu-id="698b2-134">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="698b2-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="698b2-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="698b2-135">-Tag</span></span>
<span data-ttu-id="698b2-136">Kaynaklar ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="698b2-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="698b2-137">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="698b2-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="698b2-138">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="698b2-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="698b2-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="698b2-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="698b2-140">VM 'deki UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak üzere bir veya daha fazla yönetilen veri diskine sahip olan bir bayrağı belirleyen bayrak.</span><span class="sxs-lookup"><span data-stu-id="698b2-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="698b2-141">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="698b2-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="698b2-142">-VM</span><span class="sxs-lookup"><span data-stu-id="698b2-142">-VM</span></span>
<span data-ttu-id="698b2-143">Yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="698b2-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="698b2-144">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="698b2-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="698b2-145">Bu sanal makine nesnesi sanal makinenin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="698b2-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="698b2-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="698b2-146">-Confirm</span></span>
<span data-ttu-id="698b2-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="698b2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="698b2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="698b2-148">-WhatIf</span></span>
<span data-ttu-id="698b2-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="698b2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="698b2-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="698b2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="698b2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698b2-151">CommonParameters</span></span>
<span data-ttu-id="698b2-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="698b2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698b2-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698b2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698b2-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="698b2-154">INPUTS</span></span>

### <span data-ttu-id="698b2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="698b2-155">System.String</span></span>

### <span data-ttu-id="698b2-156">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="698b2-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="698b2-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="698b2-157">System.Boolean</span></span>

## <span data-ttu-id="698b2-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="698b2-158">OUTPUTS</span></span>

### <span data-ttu-id="698b2-159">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="698b2-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="698b2-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="698b2-160">NOTES</span></span>

## <span data-ttu-id="698b2-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="698b2-161">RELATED LINKS</span></span>

[<span data-ttu-id="698b2-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="698b2-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="698b2-163">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="698b2-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="698b2-164">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="698b2-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="698b2-165">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="698b2-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="698b2-166">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="698b2-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="698b2-167">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="698b2-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="698b2-168">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="698b2-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


