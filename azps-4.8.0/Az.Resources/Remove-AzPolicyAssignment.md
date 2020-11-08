---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266427"
---
# <span data-ttu-id="80d01-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="80d01-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="80d01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d01-102">SYNOPSIS</span></span>
<span data-ttu-id="80d01-103">İlke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80d01-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="80d01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80d01-104">SYNTAX</span></span>

### <span data-ttu-id="80d01-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="80d01-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d01-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="80d01-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d01-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="80d01-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d01-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="80d01-108">DESCRIPTION</span></span>
<span data-ttu-id="80d01-109">**Remove-AzPolicyAssignment** cmdlet 'i belirtilen ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80d01-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="80d01-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80d01-110">EXAMPLES</span></span>

### <span data-ttu-id="80d01-111">Örnek 1: ad ve kapsamla ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="80d01-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="80d01-112">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="80d01-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="80d01-113">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="80d01-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="80d01-114">İkinci komut, kaynak grup düzeyinde atanmış olan PolicyAssignment07 adlı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80d01-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="80d01-115">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="80d01-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="80d01-116">Örnek 2: KIMLIĞE göre ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="80d01-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="80d01-117">İlk komut ResourceGroup11 adlı bir kaynak grubu alır ve bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="80d01-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="80d01-118">İkinci komut, kaynak grup düzeyindeki ilke atamasını alır ve $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="80d01-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="80d01-119">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="80d01-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="80d01-120">Final komutu, $PolicyAssignment **RESOURCEID** özelliğinin tanımladığı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80d01-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="80d01-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80d01-121">PARAMETERS</span></span>

### <span data-ttu-id="80d01-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="80d01-122">-ApiVersion</span></span>
<span data-ttu-id="80d01-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="80d01-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="80d01-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="80d01-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="80d01-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d01-125">-DefaultProfile</span></span>
<span data-ttu-id="80d01-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="80d01-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80d01-127">-ID</span><span class="sxs-lookup"><span data-stu-id="80d01-127">-Id</span></span>
<span data-ttu-id="80d01-128">Bu cmdlet 'in kaldırdığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="80d01-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d01-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80d01-129">-InputObject</span></span>
<span data-ttu-id="80d01-130">Başka bir cmdlet 'ten çıktı olan kaldırılacak ilke atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="80d01-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80d01-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="80d01-131">-Name</span></span>
<span data-ttu-id="80d01-132">Bu cmdlet 'in kaldırdığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80d01-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d01-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="80d01-133">-Pre</span></span>
<span data-ttu-id="80d01-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="80d01-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="80d01-135">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="80d01-135">-Scope</span></span>
<span data-ttu-id="80d01-136">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="80d01-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d01-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="80d01-137">-Confirm</span></span>
<span data-ttu-id="80d01-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="80d01-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d01-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d01-139">-WhatIf</span></span>
<span data-ttu-id="80d01-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="80d01-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d01-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="80d01-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d01-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d01-142">CommonParameters</span></span>
<span data-ttu-id="80d01-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80d01-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d01-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="80d01-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d01-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80d01-145">INPUTS</span></span>

### <span data-ttu-id="80d01-146">System. String</span><span class="sxs-lookup"><span data-stu-id="80d01-146">System.String</span></span>

## <span data-ttu-id="80d01-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80d01-147">OUTPUTS</span></span>

### <span data-ttu-id="80d01-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80d01-148">System.Boolean</span></span>

## <span data-ttu-id="80d01-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80d01-149">NOTES</span></span>

## <span data-ttu-id="80d01-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80d01-150">RELATED LINKS</span></span>

[<span data-ttu-id="80d01-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="80d01-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="80d01-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="80d01-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="80d01-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="80d01-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


