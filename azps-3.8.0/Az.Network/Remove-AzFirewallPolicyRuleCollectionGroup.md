---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104045"
---
# <span data-ttu-id="d622e-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d622e-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d622e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d622e-102">SYNOPSIS</span></span>
<span data-ttu-id="d622e-103">Azure Güvenlik duvarı ilkesinde Azure Güvenlik Duvarı Ilke kuralı koleksiyon grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="d622e-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="d622e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d622e-104">SYNTAX</span></span>

### <span data-ttu-id="d622e-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d622e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d622e-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d622e-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d622e-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d622e-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d622e-108">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d622e-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d622e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d622e-109">DESCRIPTION</span></span>
<span data-ttu-id="d622e-110">**Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet 'i, bir Azure Güvenlik Duvarı ilkesinden bir kural koleksiyonu grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d622e-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d622e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d622e-111">EXAMPLES</span></span>

### <span data-ttu-id="d622e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d622e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="d622e-113">Bu örnekte, güvenlik duvarı ilkesi nesnesinde "testRcGroup" adlı güvenlik duvarı ilkesi kuralı colelction grubu kaldırılır $fp</span><span class="sxs-lookup"><span data-stu-id="d622e-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="d622e-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d622e-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="d622e-115">Bu örnekte, "testRg" kaynak adlı güvenlik duvarında "testRcGroup" adlı güvenlik duvarı ilkesi kuralı colelction grubu kaldırılır</span><span class="sxs-lookup"><span data-stu-id="d622e-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="d622e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d622e-116">PARAMETERS</span></span>

### <span data-ttu-id="d622e-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="d622e-117">-AsJob</span></span>
<span data-ttu-id="d622e-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d622e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d622e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d622e-119">-DefaultProfile</span></span>
<span data-ttu-id="d622e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d622e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="d622e-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="d622e-122">Güvenlik Duvarı ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="d622e-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d622e-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="d622e-124">Güvenlik Duvarı Ilkesi.</span><span class="sxs-lookup"><span data-stu-id="d622e-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d622e-125">-Force</span></span>
<span data-ttu-id="d622e-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="d622e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d622e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d622e-127">-InputObject</span></span>
<span data-ttu-id="d622e-128">Güvenlik Duvarı Ilke kuralı koleksiyonu Grup nesnesi</span><span class="sxs-lookup"><span data-stu-id="d622e-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="d622e-129">-Name</span></span>
<span data-ttu-id="d622e-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d622e-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d622e-131">-PassThru</span></span>
<span data-ttu-id="d622e-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d622e-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d622e-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d622e-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d622e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d622e-134">-ResourceGroupName</span></span>
<span data-ttu-id="d622e-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d622e-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d622e-136">-ResourceId</span></span>
<span data-ttu-id="d622e-137">Kural koleksiyonu grup kimliği</span><span class="sxs-lookup"><span data-stu-id="d622e-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="d622e-138">-Confirm</span></span>
<span data-ttu-id="d622e-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d622e-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d622e-140">-WhatIf</span></span>
<span data-ttu-id="d622e-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d622e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d622e-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d622e-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d622e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d622e-143">CommonParameters</span></span>
<span data-ttu-id="d622e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d622e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d622e-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d622e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d622e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d622e-146">INPUTS</span></span>

### <span data-ttu-id="d622e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d622e-147">System.String</span></span>

### <span data-ttu-id="d622e-148">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d622e-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="d622e-149">Microsoft. Azure. Commands. Network. model. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="d622e-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="d622e-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d622e-150">OUTPUTS</span></span>

### <span data-ttu-id="d622e-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d622e-151">System.Boolean</span></span>

## <span data-ttu-id="d622e-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d622e-152">NOTES</span></span>

## <span data-ttu-id="d622e-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d622e-153">RELATED LINKS</span></span>
