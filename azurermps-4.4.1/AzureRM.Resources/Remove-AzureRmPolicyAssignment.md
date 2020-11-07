---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 9a238515b0482b36dcebd3bdcdf6976aebc64448
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764242"
---
# <span data-ttu-id="fb783-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb783-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="fb783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb783-102">SYNOPSIS</span></span>
<span data-ttu-id="fb783-103">İlke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb783-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb783-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb783-104">SYNTAX</span></span>

### <span data-ttu-id="fb783-105">İlke atama adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="fb783-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="fb783-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="fb783-106">(Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb783-107">İlke atama kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="fb783-107">The policy assignment Id parameter set.</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb783-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb783-108">DESCRIPTION</span></span>
<span data-ttu-id="fb783-109">**Remove-AzureRmPolicyAssignment** cmdlet 'i belirtilen ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb783-109">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="fb783-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb783-110">EXAMPLES</span></span>

### <span data-ttu-id="fb783-111">Örnek 1: ad ve kapsamla ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fb783-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="fb783-112">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="fb783-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="fb783-113">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fb783-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="fb783-114">İkinci komut, kaynak grup düzeyinde atanmış olan PolicyAssignment07 adlı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb783-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="fb783-115">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fb783-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="fb783-116">Örnek 2: KIMLIĞE göre ilke atamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fb783-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="fb783-117">İlk komut ResourceGroup11 adlı bir kaynak grubu alır ve bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fb783-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="fb783-118">İkinci komut, kaynak grup düzeyindeki ilke atamasını alır ve $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fb783-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fb783-119">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fb783-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="fb783-120">Final komutu, $PolicyAssignment **RESOURCEID** özelliğinin tanımladığı ilke atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb783-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="fb783-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb783-121">PARAMETERS</span></span>

### <span data-ttu-id="fb783-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="fb783-122">-ApiVersion</span></span>
<span data-ttu-id="fb783-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb783-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fb783-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="fb783-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fb783-125">-ID</span><span class="sxs-lookup"><span data-stu-id="fb783-125">-Id</span></span>
<span data-ttu-id="fb783-126">Bu cmdlet 'in kaldırdığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb783-126">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb783-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fb783-127">-InformationAction</span></span>
<span data-ttu-id="fb783-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb783-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fb783-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fb783-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb783-130">'A</span><span class="sxs-lookup"><span data-stu-id="fb783-130">Continue</span></span>
- <span data-ttu-id="fb783-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="fb783-131">Ignore</span></span>
- <span data-ttu-id="fb783-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fb783-132">Inquire</span></span>
- <span data-ttu-id="fb783-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fb783-133">SilentlyContinue</span></span>
- <span data-ttu-id="fb783-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fb783-134">Stop</span></span>
- <span data-ttu-id="fb783-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fb783-135">Suspend</span></span>

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

### <span data-ttu-id="fb783-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fb783-136">-InformationVariable</span></span>
<span data-ttu-id="fb783-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb783-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fb783-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb783-138">-Name</span></span>
<span data-ttu-id="fb783-139">Bu cmdlet 'in kaldırdığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb783-139">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb783-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fb783-140">-Pre</span></span>
<span data-ttu-id="fb783-141">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb783-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fb783-142">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="fb783-142">-Scope</span></span>
<span data-ttu-id="fb783-143">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb783-143">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb783-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb783-144">-Confirm</span></span>
<span data-ttu-id="fb783-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb783-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb783-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb783-146">-WhatIf</span></span>
<span data-ttu-id="fb783-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb783-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb783-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb783-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb783-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb783-149">-DefaultProfile</span></span>
<span data-ttu-id="fb783-150">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb783-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb783-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb783-151">CommonParameters</span></span>
<span data-ttu-id="fb783-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb783-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb783-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb783-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb783-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb783-154">INPUTS</span></span>

## <span data-ttu-id="fb783-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb783-155">OUTPUTS</span></span>

### <span data-ttu-id="fb783-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb783-156">System.Boolean</span></span>

## <span data-ttu-id="fb783-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb783-157">NOTES</span></span>

## <span data-ttu-id="fb783-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb783-158">RELATED LINKS</span></span>

[<span data-ttu-id="fb783-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb783-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="fb783-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb783-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="fb783-161">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb783-161">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


