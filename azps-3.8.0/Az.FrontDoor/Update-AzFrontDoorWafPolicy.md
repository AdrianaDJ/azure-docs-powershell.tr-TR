---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096639"
---
# <span data-ttu-id="f99dc-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="f99dc-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="f99dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f99dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f99dc-103">WAF ilkesini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="f99dc-103">Update WAF policy</span></span>

## <span data-ttu-id="f99dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f99dc-104">SYNTAX</span></span>

### <span data-ttu-id="f99dc-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f99dc-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99dc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f99dc-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99dc-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f99dc-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99dc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f99dc-108">DESCRIPTION</span></span>
<span data-ttu-id="f99dc-109">**Update-AzFrontDoorWafPolicy** cmdlet 'i var olan bir WAF ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f99dc-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="f99dc-110">Giriş parametreleri sağlanmazsa, var olan WAF ilkesindeki eski parametreler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f99dc-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="f99dc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f99dc-111">EXAMPLES</span></span>

### <span data-ttu-id="f99dc-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f99dc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="f99dc-113">Var olan WAF ilkesi özel durum kodunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f99dc-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="f99dc-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f99dc-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="f99dc-115">Var olan WAF ilkesi modunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f99dc-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="f99dc-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f99dc-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="f99dc-117">Var olan WAF ilkesi etkin durumunu ve modunu güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="f99dc-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="f99dc-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="f99dc-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="f99dc-119">$resourceGroupName tüm WAF ilkelerini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="f99dc-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="f99dc-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f99dc-120">PARAMETERS</span></span>

### <span data-ttu-id="f99dc-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="f99dc-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="f99dc-122">Özel yanıt gövdesi</span><span class="sxs-lookup"><span data-stu-id="f99dc-122">Custom Response Body</span></span>

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

### <span data-ttu-id="f99dc-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="f99dc-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="f99dc-124">Özel yanıt durum kodu</span><span class="sxs-lookup"><span data-stu-id="f99dc-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="f99dc-125">-Customrule</span></span>
<span data-ttu-id="f99dc-126">İlkenin içindeki özel kurallar</span><span class="sxs-lookup"><span data-stu-id="f99dc-126">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99dc-127">-DefaultProfile</span></span>
<span data-ttu-id="f99dc-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f99dc-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f99dc-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f99dc-129">-EnabledState</span></span>
<span data-ttu-id="f99dc-130">İlkenin etkin durumda veya devre dışı durumunda olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="f99dc-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="f99dc-131">Olası değerler: ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="f99dc-131">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f99dc-132">-InputObject</span></span>
<span data-ttu-id="f99dc-133">Güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="f99dc-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f99dc-134">-ManagedRule</span></span>
<span data-ttu-id="f99dc-135">İlkenin içinde yönetilen kurallar</span><span class="sxs-lookup"><span data-stu-id="f99dc-135">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-136">-Mod</span><span class="sxs-lookup"><span data-stu-id="f99dc-136">-Mode</span></span>
<span data-ttu-id="f99dc-137">Algılama modu 'nda veya koruma modu 'nun ilke düzeyinde olup olmadığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="f99dc-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="f99dc-138">Olası değerler: ' önlemeye yönelik ', ' algılama '</span><span class="sxs-lookup"><span data-stu-id="f99dc-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="f99dc-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="f99dc-139">-Name</span></span>
<span data-ttu-id="f99dc-140">Güncelleştirilecek güvenlik duvarı Ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f99dc-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="f99dc-141">-RedirectUrl</span></span>
<span data-ttu-id="f99dc-142">Yönlendirme URL 'SI</span><span class="sxs-lookup"><span data-stu-id="f99dc-142">Redirect URL</span></span>

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

### <span data-ttu-id="f99dc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f99dc-143">-ResourceGroupName</span></span>
<span data-ttu-id="f99dc-144">Güvenlik Duvarı 'nın ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f99dc-144">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f99dc-145">-ResourceId</span></span>
<span data-ttu-id="f99dc-146">Güncelleştirilecek güvenlik duvarı</span><span class="sxs-lookup"><span data-stu-id="f99dc-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="f99dc-147">-Confirm</span></span>
<span data-ttu-id="f99dc-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f99dc-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99dc-149">-WhatIf</span></span>
<span data-ttu-id="f99dc-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f99dc-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f99dc-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f99dc-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99dc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99dc-152">CommonParameters</span></span>
<span data-ttu-id="f99dc-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f99dc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99dc-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f99dc-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99dc-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f99dc-155">INPUTS</span></span>

### <span data-ttu-id="f99dc-156">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f99dc-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="f99dc-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f99dc-157">System.String</span></span>

## <span data-ttu-id="f99dc-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f99dc-158">OUTPUTS</span></span>

### <span data-ttu-id="f99dc-159">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f99dc-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="f99dc-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f99dc-160">NOTES</span></span>

## <span data-ttu-id="f99dc-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f99dc-161">RELATED LINKS</span></span>

<span data-ttu-id="f99dc-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="f99dc-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>