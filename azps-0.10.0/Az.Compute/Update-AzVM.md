---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935938"
---
# <span data-ttu-id="74176-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="74176-101">Update-AzVM</span></span>

## <span data-ttu-id="74176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74176-102">SYNOPSIS</span></span>
<span data-ttu-id="74176-103">Azure sanal makinesinin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74176-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="74176-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74176-104">SYNTAX</span></span>

### <span data-ttu-id="74176-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74176-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74176-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="74176-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74176-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="74176-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74176-108">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="74176-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74176-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="74176-109">DESCRIPTION</span></span>
<span data-ttu-id="74176-110">**Update-AzVM** cmdlet 'i, bir Azure sanal makinesinin durumunu sanal makine nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74176-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="74176-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74176-111">EXAMPLES</span></span>

### <span data-ttu-id="74176-112">Örnek 1: sanal makineyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="74176-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="74176-113">Bu komut ResourceGroup11 'de sanal makineyi güncelleştirir $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="74176-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="74176-114">Komut bunu, $VirtualMachine değişkeninde depolanan sanal makine nesnesini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74176-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="74176-115">Sanal makine nesnesi edinmek için **Get-AzVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="74176-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="74176-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74176-116">PARAMETERS</span></span>

### <span data-ttu-id="74176-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="74176-117">-AsJob</span></span>
<span data-ttu-id="74176-118">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="74176-118">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74176-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="74176-119">-AssignIdentity</span></span>
<span data-ttu-id="74176-120">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="74176-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="74176-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74176-121">-DefaultProfile</span></span>
<span data-ttu-id="74176-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74176-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74176-123">-ID</span><span class="sxs-lookup"><span data-stu-id="74176-123">-Id</span></span>
<span data-ttu-id="74176-124">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="74176-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74176-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="74176-125">-IdentityId</span></span>
<span data-ttu-id="74176-126">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74176-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="74176-127">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="74176-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74176-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="74176-128">-IdentityType</span></span>
<span data-ttu-id="74176-129">Sanal makine için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="74176-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="74176-130">Şu anda tek desteklenen tür, örtülü olarak bir kimlik oluşturan ' SystemAssigned '.</span><span class="sxs-lookup"><span data-stu-id="74176-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74176-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="74176-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="74176-132">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74176-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74176-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74176-133">-ResourceGroupName</span></span>
<span data-ttu-id="74176-134">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74176-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74176-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="74176-135">-Tag</span></span>
<span data-ttu-id="74176-136">Kaynaklar ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74176-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="74176-137">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="74176-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="74176-138">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="74176-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74176-139">-VM</span><span class="sxs-lookup"><span data-stu-id="74176-139">-VM</span></span>
<span data-ttu-id="74176-140">Yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74176-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="74176-141">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="74176-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="74176-142">Bu sanal makine nesnesi sanal makinenin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="74176-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74176-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="74176-143">-Confirm</span></span>
<span data-ttu-id="74176-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74176-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74176-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74176-145">-WhatIf</span></span>
<span data-ttu-id="74176-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74176-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="74176-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74176-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74176-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74176-148">CommonParameters</span></span>
<span data-ttu-id="74176-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74176-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74176-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74176-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74176-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74176-151">INPUTS</span></span>

### <span data-ttu-id="74176-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="74176-152">PSVirtualMachine</span></span>
<span data-ttu-id="74176-153">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="74176-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="74176-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74176-154">OUTPUTS</span></span>

### <span data-ttu-id="74176-155">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="74176-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="74176-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74176-156">NOTES</span></span>

## <span data-ttu-id="74176-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74176-157">RELATED LINKS</span></span>

[<span data-ttu-id="74176-158">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="74176-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="74176-159">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="74176-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="74176-160">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="74176-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="74176-161">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="74176-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="74176-162">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="74176-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="74176-163">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="74176-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="74176-164">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="74176-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


