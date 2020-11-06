---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
ms.openlocfilehash: 55f7b56f57bf18c4a3bf3198e8335cff08caae97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586763"
---
# <span data-ttu-id="0c3f2-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="0c3f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c3f2-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3f2-103">Azure sanal makinesinin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c3f2-104">SYNTAX</span></span>

### <span data-ttu-id="0c3f2-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c3f2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c3f2-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3f2-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c3f2-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3f2-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3f2-108">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="0c3f2-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3f2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c3f2-109">DESCRIPTION</span></span>
<span data-ttu-id="0c3f2-110">**Update-AzureRmVM** cmdlet 'i, bir Azure sanal makinesinin durumunu sanal makine nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="0c3f2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c3f2-111">EXAMPLES</span></span>

### <span data-ttu-id="0c3f2-112">Örnek 1: sanal makineyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0c3f2-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="0c3f2-113">Bu komut ResourceGroup11 'de sanal makineyi güncelleştirir $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="0c3f2-114">Komut bunu, $VirtualMachine değişkeninde depolanan sanal makine nesnesini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0c3f2-115">Sanal makine nesnesi edinmek için **Get-AzureRmVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="0c3f2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c3f2-116">PARAMETERS</span></span>

### <span data-ttu-id="0c3f2-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="0c3f2-117">-AsJob</span></span>
<span data-ttu-id="0c3f2-118">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0c3f2-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="0c3f2-119">-AssignIdentity</span></span>
<span data-ttu-id="0c3f2-120">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="0c3f2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3f2-121">-DefaultProfile</span></span>
<span data-ttu-id="0c3f2-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c3f2-123">-ID</span><span class="sxs-lookup"><span data-stu-id="0c3f2-123">-Id</span></span>
<span data-ttu-id="0c3f2-124">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="0c3f2-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="0c3f2-125">-IdentityId</span></span>
<span data-ttu-id="0c3f2-126">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="0c3f2-127">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="0c3f2-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="0c3f2-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0c3f2-128">-IdentityType</span></span>
<span data-ttu-id="0c3f2-129">Sanal makine için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="0c3f2-130">Şu anda tek desteklenen tür, örtülü olarak bir kimlik oluşturan ' SystemAssigned '.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="0c3f2-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0c3f2-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="0c3f2-132">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="0c3f2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3f2-133">-ResourceGroupName</span></span>
<span data-ttu-id="0c3f2-134">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0c3f2-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0c3f2-135">-Tag</span></span>
<span data-ttu-id="0c3f2-136">Kaynaklar ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="0c3f2-137">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="0c3f2-138">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="0c3f2-139">-VM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-139">-VM</span></span>
<span data-ttu-id="0c3f2-140">Yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="0c3f2-141">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-141">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="0c3f2-142">Bu sanal makine nesnesi sanal makinenin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="0c3f2-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c3f2-143">-Confirm</span></span>
<span data-ttu-id="0c3f2-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3f2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3f2-145">-WhatIf</span></span>
<span data-ttu-id="0c3f2-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0c3f2-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3f2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3f2-148">CommonParameters</span></span>
<span data-ttu-id="0c3f2-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c3f2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3f2-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3f2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3f2-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c3f2-151">INPUTS</span></span>

### <span data-ttu-id="0c3f2-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0c3f2-152">PSVirtualMachine</span></span>
<span data-ttu-id="0c3f2-153">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0c3f2-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="0c3f2-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c3f2-154">OUTPUTS</span></span>

### <span data-ttu-id="0c3f2-155">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0c3f2-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0c3f2-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c3f2-156">NOTES</span></span>

## <span data-ttu-id="0c3f2-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c3f2-157">RELATED LINKS</span></span>

[<span data-ttu-id="0c3f2-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0c3f2-159">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-159">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="0c3f2-160">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-160">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="0c3f2-161">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-161">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="0c3f2-162">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-162">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="0c3f2-163">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c3f2-163">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="0c3f2-164">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0c3f2-164">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


