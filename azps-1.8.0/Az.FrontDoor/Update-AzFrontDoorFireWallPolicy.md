---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 3e0502d3503bdbf95fb81c779829b73e896b150f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916684"
---
# <span data-ttu-id="5b945-101">Update-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="5b945-101">Update-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="5b945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b945-102">SYNOPSIS</span></span>
<span data-ttu-id="5b945-103">WAF ilkesini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="5b945-103">Update WAF policy</span></span>

## <span data-ttu-id="5b945-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b945-104">SYNTAX</span></span>

### <span data-ttu-id="5b945-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5b945-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b945-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b945-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b945-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5b945-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b945-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b945-108">DESCRIPTION</span></span>
<span data-ttu-id="5b945-109">**Update-AzFrontDoorFireWallPolicy** cmdlet 'i var olan bir WAF ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5b945-109">The **Update-AzFrontDoorFireWallPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="5b945-110">Giriş parametreleri sağlanmazsa, var olan WAF ilkesindeki eski parametreler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b945-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="5b945-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b945-111">EXAMPLES</span></span>

### <span data-ttu-id="5b945-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5b945-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="5b945-113">Var olan WAF ilkesi özel durum kodunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="5b945-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="5b945-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5b945-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="5b945-115">Var olan WAF ilkesi modunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="5b945-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="5b945-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5b945-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="5b945-117">Var olan WAF ilkesi etkin durumunu ve modunu güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="5b945-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="5b945-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="5b945-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorFireWallPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="5b945-119">$resourceGroupName tüm WAF ilkelerini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="5b945-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="5b945-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b945-120">PARAMETERS</span></span>

### <span data-ttu-id="5b945-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="5b945-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="5b945-122">Özel yanıt gövdesi</span><span class="sxs-lookup"><span data-stu-id="5b945-122">Custom Response Body</span></span>

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

### <span data-ttu-id="5b945-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="5b945-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="5b945-124">Özel yanıt durum kodu</span><span class="sxs-lookup"><span data-stu-id="5b945-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="5b945-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="5b945-125">-Customrule</span></span>
<span data-ttu-id="5b945-126">İlkenin içindeki özel kurallar</span><span class="sxs-lookup"><span data-stu-id="5b945-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="5b945-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b945-127">-DefaultProfile</span></span>
<span data-ttu-id="5b945-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b945-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b945-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5b945-129">-EnabledState</span></span>
<span data-ttu-id="5b945-130">İlkenin etkin durumda veya devre dışı durumunda olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="5b945-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="5b945-131">Olası değerler: ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="5b945-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="5b945-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b945-132">-InputObject</span></span>
<span data-ttu-id="5b945-133">Güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="5b945-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="5b945-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5b945-134">-ManagedRule</span></span>
<span data-ttu-id="5b945-135">İlkenin içinde yönetilen kurallar</span><span class="sxs-lookup"><span data-stu-id="5b945-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="5b945-136">-Mod</span><span class="sxs-lookup"><span data-stu-id="5b945-136">-Mode</span></span>
<span data-ttu-id="5b945-137">Algılama modu 'nda veya koruma modu 'nun ilke düzeyinde olup olmadığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="5b945-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="5b945-138">Olası değerler: ' önlemeye yönelik ', ' algılama '</span><span class="sxs-lookup"><span data-stu-id="5b945-138">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b945-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b945-139">-Name</span></span>
<span data-ttu-id="5b945-140">Güncelleştirilecek güvenlik duvarı Ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="5b945-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="5b945-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="5b945-141">-RedirectUrl</span></span>
<span data-ttu-id="5b945-142">Yönlendirme URL 'SI</span><span class="sxs-lookup"><span data-stu-id="5b945-142">Redirect URL</span></span>

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

### <span data-ttu-id="5b945-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b945-143">-ResourceGroupName</span></span>
<span data-ttu-id="5b945-144">Güvenlik Duvarı 'nın ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="5b945-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="5b945-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5b945-145">-ResourceId</span></span>
<span data-ttu-id="5b945-146">Güncelleştirilecek güvenlik duvarı</span><span class="sxs-lookup"><span data-stu-id="5b945-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="5b945-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b945-147">-Confirm</span></span>
<span data-ttu-id="5b945-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b945-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b945-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b945-149">-WhatIf</span></span>
<span data-ttu-id="5b945-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b945-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b945-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b945-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b945-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b945-152">CommonParameters</span></span>
<span data-ttu-id="5b945-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b945-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b945-154">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b945-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b945-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b945-155">INPUTS</span></span>

### <span data-ttu-id="5b945-156">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5b945-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="5b945-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5b945-157">System.String</span></span>

## <span data-ttu-id="5b945-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b945-158">OUTPUTS</span></span>

### <span data-ttu-id="5b945-159">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5b945-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="5b945-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b945-160">NOTES</span></span>

## <span data-ttu-id="5b945-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b945-161">RELATED LINKS</span></span>

<span data-ttu-id="5b945-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="5b945-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
