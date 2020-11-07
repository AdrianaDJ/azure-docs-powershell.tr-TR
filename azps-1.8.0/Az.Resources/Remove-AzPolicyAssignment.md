---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 18ca6ad068c5478bdb7177a8f53742f90d555dee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759339"
---
# <span data-ttu-id="f6b03-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6b03-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="f6b03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b03-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b03-103">İlke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6b03-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="f6b03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6b03-104">SYNTAX</span></span>

### <span data-ttu-id="f6b03-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6b03-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b03-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="f6b03-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6b03-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6b03-107">DESCRIPTION</span></span>
<span data-ttu-id="f6b03-108">**Remove-AzPolicyAssignment** cmdlet 'i belirtilen ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6b03-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="f6b03-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6b03-109">EXAMPLES</span></span>

### <span data-ttu-id="f6b03-110">Örnek 1: ad ve kapsamla ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f6b03-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="f6b03-111">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="f6b03-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f6b03-112">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f6b03-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f6b03-113">İkinci komut, kaynak grup düzeyinde atanmış olan PolicyAssignment07 adlı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6b03-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="f6b03-114">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f6b03-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="f6b03-115">Örnek 2: KIMLIĞE göre ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f6b03-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="f6b03-116">İlk komut ResourceGroup11 adlı bir kaynak grubu alır ve bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f6b03-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f6b03-117">İkinci komut, kaynak grup düzeyindeki ilke atamasını alır ve $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f6b03-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="f6b03-118">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f6b03-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="f6b03-119">Final komutu, $PolicyAssignment **RESOURCEID** özelliğinin tanımladığı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6b03-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="f6b03-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6b03-120">PARAMETERS</span></span>

### <span data-ttu-id="f6b03-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f6b03-121">-ApiVersion</span></span>
<span data-ttu-id="f6b03-122">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6b03-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f6b03-123">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="f6b03-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f6b03-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b03-124">-DefaultProfile</span></span>
<span data-ttu-id="f6b03-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f6b03-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6b03-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f6b03-126">-Id</span></span>
<span data-ttu-id="f6b03-127">Bu cmdlet 'in kaldırdığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6b03-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f6b03-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6b03-128">-Name</span></span>
<span data-ttu-id="f6b03-129">Bu cmdlet 'in kaldırdığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6b03-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f6b03-130">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f6b03-130">-Pre</span></span>
<span data-ttu-id="f6b03-131">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6b03-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f6b03-132">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="f6b03-132">-Scope</span></span>
<span data-ttu-id="f6b03-133">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6b03-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="f6b03-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6b03-134">-Confirm</span></span>
<span data-ttu-id="f6b03-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6b03-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6b03-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b03-136">-WhatIf</span></span>
<span data-ttu-id="f6b03-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6b03-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6b03-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6b03-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6b03-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b03-139">CommonParameters</span></span>
<span data-ttu-id="f6b03-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6b03-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b03-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b03-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b03-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6b03-142">INPUTS</span></span>

### <span data-ttu-id="f6b03-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f6b03-143">System.String</span></span>

## <span data-ttu-id="f6b03-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6b03-144">OUTPUTS</span></span>

### <span data-ttu-id="f6b03-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6b03-145">System.Boolean</span></span>

## <span data-ttu-id="f6b03-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6b03-146">NOTES</span></span>

## <span data-ttu-id="f6b03-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6b03-147">RELATED LINKS</span></span>

[<span data-ttu-id="f6b03-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6b03-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="f6b03-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6b03-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="f6b03-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6b03-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)

