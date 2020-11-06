---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592027"
---
# <span data-ttu-id="1bab9-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bab9-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="1bab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bab9-102">SYNOPSIS</span></span>
<span data-ttu-id="1bab9-103">Azure sanal makinesinin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bab9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1bab9-104">SYNTAX</span></span>

### <span data-ttu-id="1bab9-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1bab9-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bab9-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bab9-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bab9-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bab9-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bab9-108">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="1bab9-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bab9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bab9-109">DESCRIPTION</span></span>
<span data-ttu-id="1bab9-110">**Update-AzureRmVM** cmdlet 'i, bir Azure sanal makinesinin durumunu sanal makine nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="1bab9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1bab9-111">EXAMPLES</span></span>

### <span data-ttu-id="1bab9-112">Örnek 1: sanal makineyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1bab9-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="1bab9-113">Bu komut ResourceGroup11 'de sanal makineyi güncelleştirir $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1bab9-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="1bab9-114">Komut bunu, $VirtualMachine değişkeninde depolanan sanal makine nesnesini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1bab9-115">Sanal makine nesnesi edinmek için **Get-AzureRmVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1bab9-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="1bab9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1bab9-116">PARAMETERS</span></span>

### <span data-ttu-id="1bab9-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="1bab9-117">-AsJob</span></span>
<span data-ttu-id="1bab9-118">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="1bab9-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1bab9-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="1bab9-119">-AssignIdentity</span></span>
<span data-ttu-id="1bab9-120">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="1bab9-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="1bab9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bab9-121">-DefaultProfile</span></span>
<span data-ttu-id="1bab9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1bab9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bab9-123">-ID</span><span class="sxs-lookup"><span data-stu-id="1bab9-123">-Id</span></span>
<span data-ttu-id="1bab9-124">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1bab9-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="1bab9-125">-IdentityId</span></span>
<span data-ttu-id="1bab9-126">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="1bab9-127">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="1bab9-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="1bab9-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1bab9-128">-IdentityType</span></span>
<span data-ttu-id="1bab9-129">Sanal makine için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="1bab9-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="1bab9-130">Şu anda tek desteklenen tür, örtülü olarak bir kimlik oluşturan ' SystemAssigned '.</span><span class="sxs-lookup"><span data-stu-id="1bab9-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="1bab9-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1bab9-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="1bab9-132">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="1bab9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bab9-133">-ResourceGroupName</span></span>
<span data-ttu-id="1bab9-134">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1bab9-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1bab9-135">-Tag</span></span>
<span data-ttu-id="1bab9-136">Kaynaklar ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="1bab9-137">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="1bab9-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="1bab9-138">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="1bab9-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="1bab9-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="1bab9-140">VM 'deki UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak üzere bir veya daha fazla yönetilen veri diskine sahip olan bir bayrağı belirleyen bayrak.</span><span class="sxs-lookup"><span data-stu-id="1bab9-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="1bab9-141">Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="1bab9-142">-VM</span><span class="sxs-lookup"><span data-stu-id="1bab9-142">-VM</span></span>
<span data-ttu-id="1bab9-143">Yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="1bab9-144">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1bab9-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="1bab9-145">Bu sanal makine nesnesi sanal makinenin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="1bab9-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="1bab9-146">-Confirm</span></span>
<span data-ttu-id="1bab9-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1bab9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bab9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bab9-148">-WhatIf</span></span>
<span data-ttu-id="1bab9-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1bab9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bab9-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1bab9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bab9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bab9-151">CommonParameters</span></span>
<span data-ttu-id="1bab9-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1bab9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bab9-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bab9-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bab9-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1bab9-154">INPUTS</span></span>

### <span data-ttu-id="1bab9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1bab9-155">System.String</span></span>

### <span data-ttu-id="1bab9-156">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1bab9-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1bab9-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1bab9-157">OUTPUTS</span></span>

### <span data-ttu-id="1bab9-158">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1bab9-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1bab9-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1bab9-159">NOTES</span></span>

## <span data-ttu-id="1bab9-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1bab9-160">RELATED LINKS</span></span>

[<span data-ttu-id="1bab9-161">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bab9-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="1bab9-162">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bab9-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="1bab9-163">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bab9-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="1bab9-164">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bab9-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="1bab9-165">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bab9-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="1bab9-166">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bab9-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="1bab9-167">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="1bab9-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


