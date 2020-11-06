---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591788"
---
# <span data-ttu-id="71759-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71759-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="71759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71759-102">SYNOPSIS</span></span>
<span data-ttu-id="71759-103">Azure sanal makinesinin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="71759-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71759-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71759-104">SYNTAX</span></span>

### <span data-ttu-id="71759-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="71759-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71759-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="71759-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71759-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="71759-107">DESCRIPTION</span></span>
<span data-ttu-id="71759-108">**Update-AzureRmVM** cmdlet 'i, bir Azure sanal makinesinin durumunu sanal makine nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="71759-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="71759-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71759-109">EXAMPLES</span></span>

### <span data-ttu-id="71759-110">Örnek 1: sanal makineyi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="71759-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="71759-111">Bu komut ResourceGroup11 'de sanal makineyi güncelleştirir $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="71759-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="71759-112">Komut bunu, $VirtualMachine değişkeninde depolanan sanal makine nesnesini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="71759-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="71759-113">Sanal makine nesnesi edinmek için **Get-AzureRmVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="71759-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="71759-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71759-114">PARAMETERS</span></span>

### <span data-ttu-id="71759-115">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="71759-115">-AssignIdentity</span></span>
<span data-ttu-id="71759-116">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="71759-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71759-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71759-117">-DefaultProfile</span></span>
<span data-ttu-id="71759-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71759-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71759-119">-ID</span><span class="sxs-lookup"><span data-stu-id="71759-119">-Id</span></span>
<span data-ttu-id="71759-120">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="71759-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="71759-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="71759-121">-IdentityType</span></span>
<span data-ttu-id="71759-122">Sanal makine için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="71759-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="71759-123">Şu anda tek desteklenen tür, örtülü olarak bir kimlik oluşturan ' SystemAssigned '.</span><span class="sxs-lookup"><span data-stu-id="71759-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71759-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71759-124">-ResourceGroupName</span></span>
<span data-ttu-id="71759-125">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71759-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71759-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="71759-126">-Tags</span></span>
<span data-ttu-id="71759-127">Kaynaklar ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="71759-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="71759-128">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="71759-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="71759-129">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="71759-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="71759-130">-VM</span><span class="sxs-lookup"><span data-stu-id="71759-130">-VM</span></span>
<span data-ttu-id="71759-131">Yerel bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="71759-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="71759-132">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="71759-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="71759-133">Bu sanal makine nesnesi sanal makinenin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="71759-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="71759-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="71759-134">-Confirm</span></span>
<span data-ttu-id="71759-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="71759-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71759-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71759-136">-WhatIf</span></span>
<span data-ttu-id="71759-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="71759-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="71759-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="71759-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71759-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71759-139">CommonParameters</span></span>
<span data-ttu-id="71759-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71759-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71759-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71759-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71759-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71759-142">INPUTS</span></span>

## <span data-ttu-id="71759-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71759-143">OUTPUTS</span></span>

## <span data-ttu-id="71759-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71759-144">NOTES</span></span>

## <span data-ttu-id="71759-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71759-145">RELATED LINKS</span></span>

[<span data-ttu-id="71759-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71759-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="71759-147">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71759-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="71759-148">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71759-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="71759-149">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71759-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="71759-150">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71759-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="71759-151">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71759-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="71759-152">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="71759-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


