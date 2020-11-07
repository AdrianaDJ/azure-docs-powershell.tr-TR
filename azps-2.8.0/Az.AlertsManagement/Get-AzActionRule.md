---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: f3904826ef41f271086d048183b8b2035d1b11e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753672"
---
# <span data-ttu-id="903a1-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="903a1-101">Get-AzActionRule</span></span>

## <span data-ttu-id="903a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="903a1-102">SYNOPSIS</span></span>
<span data-ttu-id="903a1-103">Eylem kuralları bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="903a1-103">Get Action Rules Information</span></span>

## <span data-ttu-id="903a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="903a1-104">SYNTAX</span></span>

### <span data-ttu-id="903a1-105">ListActionRules (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="903a1-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="903a1-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="903a1-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="903a1-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="903a1-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="903a1-108">Listactionkuralları Bytargetresourceıd</span><span class="sxs-lookup"><span data-stu-id="903a1-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="903a1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="903a1-109">DESCRIPTION</span></span>
<span data-ttu-id="903a1-110">**Get-AzActionRule** cmdlet 'i, yapılandırılmış işlem kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="903a1-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="903a1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="903a1-111">EXAMPLES</span></span>

### <span data-ttu-id="903a1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="903a1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="903a1-113">Sev2 önem düzeyi ve platform Izleyicisi hizmetinde, kaynak grubunda yapılandırılmış tüm eylem kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="903a1-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="903a1-114">Listedeki her eylem kuralının ayrıntılarını almak için Format-List kullanın.</span><span class="sxs-lookup"><span data-stu-id="903a1-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="903a1-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="903a1-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="903a1-116">Test-RG kaynak grubundaki eylem kuralına sahip eylem kuralını alın-eylem-kural.</span><span class="sxs-lookup"><span data-stu-id="903a1-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="903a1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="903a1-117">PARAMETERS</span></span>

### <span data-ttu-id="903a1-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="903a1-118">-ActionGroup</span></span>
<span data-ttu-id="903a1-119">Eylem grubu</span><span class="sxs-lookup"><span data-stu-id="903a1-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-120">-Alertruleıd</span><span class="sxs-lookup"><span data-stu-id="903a1-120">-AlertRuleId</span></span>
<span data-ttu-id="903a1-121">Uyarı kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="903a1-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903a1-122">-DefaultProfile</span></span>
<span data-ttu-id="903a1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="903a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="903a1-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="903a1-124">-Description</span></span>
<span data-ttu-id="903a1-125">Akıllı grup kimliği olan tüm uyarıları filtreleme</span><span class="sxs-lookup"><span data-stu-id="903a1-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-126">-Impactedscope</span><span class="sxs-lookup"><span data-stu-id="903a1-126">-ImpactedScope</span></span>
<span data-ttu-id="903a1-127">Etkilenen kapsamda filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="903a1-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="903a1-128">-MonitorService</span></span>
<span data-ttu-id="903a1-129">Monitorın hizmetine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="903a1-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="903a1-130">-Name</span></span>
<span data-ttu-id="903a1-131">Eylem kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="903a1-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903a1-132">-ResourceGroupName</span></span>
<span data-ttu-id="903a1-133">Eylem kuralının bulunduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="903a1-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="903a1-134">-ResourceId</span></span>
<span data-ttu-id="903a1-135">Kaynak No 'dan eylem kuralı alın.</span><span class="sxs-lookup"><span data-stu-id="903a1-135">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-136">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="903a1-136">-Severity</span></span>
<span data-ttu-id="903a1-137">Uyarının önem derecesine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="903a1-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="903a1-138">-TargetResourceGroup</span></span>
<span data-ttu-id="903a1-139">Uyarının hedef kaynağının kaynak grubu adına filtre uygulama.</span><span class="sxs-lookup"><span data-stu-id="903a1-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-140">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="903a1-140">-TargetResourceId</span></span>
<span data-ttu-id="903a1-141">Uyarının hedef kaynağının kaynak kimliği 'ne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="903a1-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="903a1-142">-TargetResourceType</span></span>
<span data-ttu-id="903a1-143">Hedef uyarının kaynak türüne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="903a1-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903a1-144">CommonParameters</span></span>
<span data-ttu-id="903a1-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="903a1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903a1-146">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="903a1-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903a1-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="903a1-147">INPUTS</span></span>

### <span data-ttu-id="903a1-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="903a1-148">None</span></span>

## <span data-ttu-id="903a1-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="903a1-149">OUTPUTS</span></span>

### <span data-ttu-id="903a1-150">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="903a1-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="903a1-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="903a1-151">NOTES</span></span>

## <span data-ttu-id="903a1-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="903a1-152">RELATED LINKS</span></span>
