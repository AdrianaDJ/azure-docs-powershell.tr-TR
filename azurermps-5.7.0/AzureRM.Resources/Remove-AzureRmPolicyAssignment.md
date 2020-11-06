---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589682"
---
# <span data-ttu-id="6452d-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6452d-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="6452d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6452d-102">SYNOPSIS</span></span>
<span data-ttu-id="6452d-103">İlke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6452d-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6452d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6452d-104">SYNTAX</span></span>

### <span data-ttu-id="6452d-105">RemoveByPolicyAssignmentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6452d-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6452d-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="6452d-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6452d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6452d-107">DESCRIPTION</span></span>
<span data-ttu-id="6452d-108">**Remove-AzureRmPolicyAssignment** cmdlet 'i belirtilen ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6452d-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="6452d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6452d-109">EXAMPLES</span></span>

### <span data-ttu-id="6452d-110">Örnek 1: ad ve kapsamla ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6452d-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="6452d-111">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="6452d-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="6452d-112">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6452d-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="6452d-113">İkinci komut, kaynak grup düzeyinde atanmış olan PolicyAssignment07 adlı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6452d-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="6452d-114">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6452d-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="6452d-115">Örnek 2: KIMLIĞE göre ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6452d-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="6452d-116">İlk komut ResourceGroup11 adlı bir kaynak grubu alır ve bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6452d-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="6452d-117">İkinci komut, kaynak grup düzeyindeki ilke atamasını alır ve $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6452d-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="6452d-118">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6452d-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="6452d-119">Final komutu, $PolicyAssignment **RESOURCEID** özelliğinin tanımladığı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6452d-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="6452d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6452d-120">PARAMETERS</span></span>

### <span data-ttu-id="6452d-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="6452d-121">-ApiVersion</span></span>
<span data-ttu-id="6452d-122">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6452d-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6452d-123">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="6452d-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6452d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6452d-124">-DefaultProfile</span></span>
<span data-ttu-id="6452d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6452d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6452d-126">-ID</span><span class="sxs-lookup"><span data-stu-id="6452d-126">-Id</span></span>
<span data-ttu-id="6452d-127">Bu cmdlet 'in kaldırdığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6452d-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6452d-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6452d-128">-InformationAction</span></span>
<span data-ttu-id="6452d-129">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6452d-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6452d-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6452d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6452d-131">'A</span><span class="sxs-lookup"><span data-stu-id="6452d-131">Continue</span></span>
- <span data-ttu-id="6452d-132">Manıza</span><span class="sxs-lookup"><span data-stu-id="6452d-132">Ignore</span></span>
- <span data-ttu-id="6452d-133">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="6452d-133">Inquire</span></span>
- <span data-ttu-id="6452d-134">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="6452d-134">SilentlyContinue</span></span>
- <span data-ttu-id="6452d-135">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="6452d-135">Stop</span></span>
- <span data-ttu-id="6452d-136">Biliriz</span><span class="sxs-lookup"><span data-stu-id="6452d-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6452d-137">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="6452d-137">-InformationVariable</span></span>
<span data-ttu-id="6452d-138">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="6452d-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6452d-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="6452d-139">-Name</span></span>
<span data-ttu-id="6452d-140">Bu cmdlet 'in kaldırdığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6452d-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6452d-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="6452d-141">-Pre</span></span>
<span data-ttu-id="6452d-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6452d-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6452d-143">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="6452d-143">-Scope</span></span>
<span data-ttu-id="6452d-144">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6452d-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6452d-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="6452d-145">-Confirm</span></span>
<span data-ttu-id="6452d-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6452d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6452d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6452d-147">-WhatIf</span></span>
<span data-ttu-id="6452d-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6452d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6452d-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6452d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6452d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6452d-150">CommonParameters</span></span>
<span data-ttu-id="6452d-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6452d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6452d-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6452d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6452d-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6452d-153">INPUTS</span></span>

### <span data-ttu-id="6452d-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6452d-154">None</span></span>
<span data-ttu-id="6452d-155">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6452d-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6452d-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6452d-156">OUTPUTS</span></span>

### <span data-ttu-id="6452d-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6452d-157">System.Boolean</span></span>

## <span data-ttu-id="6452d-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6452d-158">NOTES</span></span>

## <span data-ttu-id="6452d-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6452d-159">RELATED LINKS</span></span>

[<span data-ttu-id="6452d-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6452d-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6452d-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6452d-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6452d-162">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6452d-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


