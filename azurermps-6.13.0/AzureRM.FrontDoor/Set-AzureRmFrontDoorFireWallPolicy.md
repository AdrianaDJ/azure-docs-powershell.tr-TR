---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761968"
---
# <span data-ttu-id="d4dcd-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="d4dcd-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="d4dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dcd-103">WAF ilkesini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d4dcd-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4dcd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4dcd-104">SYNTAX</span></span>

### <span data-ttu-id="d4dcd-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4dcd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4dcd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4dcd-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4dcd-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d4dcd-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4dcd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4dcd-108">DESCRIPTION</span></span>
<span data-ttu-id="d4dcd-109">**Set-Azurermfrontkapısı** cmdlet 'i mevcut bir WAF ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="d4dcd-110">Giriş parametreleri sağlanmazsa, var olan WAF ilkesindeki eski parametreler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="d4dcd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4dcd-111">EXAMPLES</span></span>

### <span data-ttu-id="d4dcd-112">Örnek 1: var olan WAF ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4dcd-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d4dcd-113">var olan WAF ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4dcd-113">update an existing WAF policy</span></span>

### <span data-ttu-id="d4dcd-114">Örnek 2: var olan bir WAF ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4dcd-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d4dcd-115">var olan WAF ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4dcd-115">update an existing WAF policy</span></span>

### <span data-ttu-id="d4dcd-116">Örnek 3: var olan bir WAF ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4dcd-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d4dcd-117">var olan WAF ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4dcd-117">update an existing WAF policy</span></span>

### <span data-ttu-id="d4dcd-118">Örnek 4: $resourceGroup tüm WAF ilkelerini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d4dcd-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="d4dcd-119">$resourceGroup tüm WAF ilkelerini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d4dcd-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="d4dcd-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4dcd-120">PARAMETERS</span></span>

### <span data-ttu-id="d4dcd-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="d4dcd-121">-Customrule</span></span>
<span data-ttu-id="d4dcd-122">İlkenin içindeki özel kurallar</span><span class="sxs-lookup"><span data-stu-id="d4dcd-122">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="d4dcd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4dcd-123">-DefaultProfile</span></span>
<span data-ttu-id="d4dcd-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4dcd-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d4dcd-125">-EnabledState</span></span>
<span data-ttu-id="d4dcd-126">İlkenin etkin durumda veya devre dışı durumunda olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="d4dcd-127">Olası değerler: ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="d4dcd-127">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="d4dcd-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4dcd-128">-InputObject</span></span>
<span data-ttu-id="d4dcd-129">Güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-129">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="d4dcd-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d4dcd-130">-ManagedRule</span></span>
<span data-ttu-id="d4dcd-131">İlkenin içinde yönetilen kurallar</span><span class="sxs-lookup"><span data-stu-id="d4dcd-131">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="d4dcd-132">-Mod</span><span class="sxs-lookup"><span data-stu-id="d4dcd-132">-Mode</span></span>
<span data-ttu-id="d4dcd-133">Algılama modu 'nda veya koruma modu 'nun ilke düzeyinde olup olmadığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="d4dcd-134">Olası değerler: ' önlemeye yönelik ', ' algılama '</span><span class="sxs-lookup"><span data-stu-id="d4dcd-134">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="d4dcd-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4dcd-135">-Name</span></span>
<span data-ttu-id="d4dcd-136">Güncelleştirilecek güvenlik duvarı Ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-136">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="d4dcd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4dcd-137">-ResourceGroupName</span></span>
<span data-ttu-id="d4dcd-138">Güvenlik Duvarı 'nın ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-138">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="d4dcd-139">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d4dcd-139">-ResourceId</span></span>
<span data-ttu-id="d4dcd-140">Güncelleştirilecek güvenlik duvarı</span><span class="sxs-lookup"><span data-stu-id="d4dcd-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4dcd-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4dcd-141">-Confirm</span></span>
<span data-ttu-id="d4dcd-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4dcd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4dcd-143">-WhatIf</span></span>
<span data-ttu-id="d4dcd-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4dcd-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4dcd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dcd-146">CommonParameters</span></span>
<span data-ttu-id="d4dcd-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4dcd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dcd-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4dcd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dcd-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4dcd-149">INPUTS</span></span>

### <span data-ttu-id="d4dcd-150">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d4dcd-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="d4dcd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d4dcd-151">System.String</span></span>

## <span data-ttu-id="d4dcd-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4dcd-152">OUTPUTS</span></span>

### <span data-ttu-id="d4dcd-153">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d4dcd-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="d4dcd-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4dcd-154">NOTES</span></span>

## <span data-ttu-id="d4dcd-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4dcd-155">RELATED LINKS</span></span>

<span data-ttu-id="d4dcd-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="d4dcd-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
