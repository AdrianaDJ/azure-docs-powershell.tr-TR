---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: 6972d4df51222804843aa965577f7044ed4bf987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940001"
---
# <span data-ttu-id="415d1-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="415d1-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="415d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="415d1-102">SYNOPSIS</span></span>
<span data-ttu-id="415d1-103">İlke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="415d1-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="415d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="415d1-104">SYNTAX</span></span>

### <span data-ttu-id="415d1-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="415d1-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="415d1-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="415d1-106">IdParameterSet</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="415d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="415d1-107">DESCRIPTION</span></span>
<span data-ttu-id="415d1-108">**Remove-AzureRmPolicyAssignment** cmdlet 'i belirtilen ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="415d1-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="415d1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="415d1-109">EXAMPLES</span></span>

### <span data-ttu-id="415d1-110">Örnek 1: ad ve kapsamla ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="415d1-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="415d1-111">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="415d1-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="415d1-112">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="415d1-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="415d1-113">İkinci komut, kaynak grup düzeyinde atanmış olan PolicyAssignment07 adlı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="415d1-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="415d1-114">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="415d1-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="415d1-115">Örnek 2: KIMLIĞE göre ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="415d1-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="415d1-116">İlk komut ResourceGroup11 adlı bir kaynak grubu alır ve bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="415d1-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="415d1-117">İkinci komut, kaynak grup düzeyindeki ilke atamasını alır ve $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="415d1-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="415d1-118">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="415d1-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="415d1-119">Final komutu, $PolicyAssignment **RESOURCEID** özelliğinin tanımladığı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="415d1-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="415d1-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="415d1-120">PARAMETERS</span></span>

### <span data-ttu-id="415d1-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="415d1-121">-ApiVersion</span></span>
<span data-ttu-id="415d1-122">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="415d1-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="415d1-123">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="415d1-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="415d1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415d1-124">-DefaultProfile</span></span>
<span data-ttu-id="415d1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="415d1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="415d1-126">-ID</span><span class="sxs-lookup"><span data-stu-id="415d1-126">-Id</span></span>
<span data-ttu-id="415d1-127">Bu cmdlet 'in kaldırdığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="415d1-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="415d1-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="415d1-128">-InformationAction</span></span>
<span data-ttu-id="415d1-129">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="415d1-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="415d1-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="415d1-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="415d1-131">'A</span><span class="sxs-lookup"><span data-stu-id="415d1-131">Continue</span></span>
- <span data-ttu-id="415d1-132">Manıza</span><span class="sxs-lookup"><span data-stu-id="415d1-132">Ignore</span></span>
- <span data-ttu-id="415d1-133">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="415d1-133">Inquire</span></span>
- <span data-ttu-id="415d1-134">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="415d1-134">SilentlyContinue</span></span>
- <span data-ttu-id="415d1-135">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="415d1-135">Stop</span></span>
- <span data-ttu-id="415d1-136">Biliriz</span><span class="sxs-lookup"><span data-stu-id="415d1-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415d1-137">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="415d1-137">-InformationVariable</span></span>
<span data-ttu-id="415d1-138">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="415d1-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415d1-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="415d1-139">-Name</span></span>
<span data-ttu-id="415d1-140">Bu cmdlet 'in kaldırdığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="415d1-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="415d1-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="415d1-141">-Pre</span></span>
<span data-ttu-id="415d1-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="415d1-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="415d1-143">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="415d1-143">-Scope</span></span>
<span data-ttu-id="415d1-144">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="415d1-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="415d1-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="415d1-145">-Confirm</span></span>
<span data-ttu-id="415d1-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="415d1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415d1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415d1-147">-WhatIf</span></span>
<span data-ttu-id="415d1-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="415d1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415d1-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="415d1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415d1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415d1-150">CommonParameters</span></span>
<span data-ttu-id="415d1-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="415d1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415d1-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415d1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415d1-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="415d1-153">INPUTS</span></span>

## <span data-ttu-id="415d1-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="415d1-154">OUTPUTS</span></span>

## <span data-ttu-id="415d1-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="415d1-155">NOTES</span></span>

## <span data-ttu-id="415d1-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="415d1-156">RELATED LINKS</span></span>

[<span data-ttu-id="415d1-157">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="415d1-157">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="415d1-158">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="415d1-158">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="415d1-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="415d1-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


