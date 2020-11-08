---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: e1eb623fcb4b77dda95fe3f849c86e20ad5d1601
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096686"
---
# <span data-ttu-id="53412-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="53412-101">Get-AzActionRule</span></span>

## <span data-ttu-id="53412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53412-102">SYNOPSIS</span></span>
<span data-ttu-id="53412-103">Eylem kuralları bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="53412-103">Get Action Rules Information</span></span>

## <span data-ttu-id="53412-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53412-104">SYNTAX</span></span>

### <span data-ttu-id="53412-105">ListActionRules (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="53412-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53412-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="53412-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53412-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="53412-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53412-108">Listactionkuralları Bytargetresourceıd</span><span class="sxs-lookup"><span data-stu-id="53412-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53412-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="53412-109">DESCRIPTION</span></span>
<span data-ttu-id="53412-110">**Get-AzActionRule** cmdlet 'i, yapılandırılmış işlem kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="53412-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="53412-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53412-111">EXAMPLES</span></span>

### <span data-ttu-id="53412-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53412-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="53412-113">Sev2 önem düzeyi ve platform Izleyicisi hizmetinde, kaynak grubunda yapılandırılmış tüm eylem kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="53412-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="53412-114">Listedeki her eylem kuralının ayrıntılarını almak için Format-List kullanın.</span><span class="sxs-lookup"><span data-stu-id="53412-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="53412-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="53412-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="53412-116">Test-RG kaynak grubundaki eylem kuralına sahip eylem kuralını alın-eylem-kural.</span><span class="sxs-lookup"><span data-stu-id="53412-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="53412-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53412-117">PARAMETERS</span></span>

### <span data-ttu-id="53412-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="53412-118">-ActionGroup</span></span>
<span data-ttu-id="53412-119">Eylem grubu</span><span class="sxs-lookup"><span data-stu-id="53412-119">Action group</span></span>

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

### <span data-ttu-id="53412-120">-Alertruleıd</span><span class="sxs-lookup"><span data-stu-id="53412-120">-AlertRuleId</span></span>
<span data-ttu-id="53412-121">Uyarı kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="53412-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="53412-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53412-122">-DefaultProfile</span></span>
<span data-ttu-id="53412-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53412-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53412-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="53412-124">-Description</span></span>
<span data-ttu-id="53412-125">Akıllı grup kimliği olan tüm uyarıları filtreleme</span><span class="sxs-lookup"><span data-stu-id="53412-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="53412-126">-Impactedscope</span><span class="sxs-lookup"><span data-stu-id="53412-126">-ImpactedScope</span></span>
<span data-ttu-id="53412-127">Etkilenen kapsamda filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="53412-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="53412-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="53412-128">-MonitorService</span></span>
<span data-ttu-id="53412-129">Monitorın hizmetine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="53412-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="53412-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="53412-130">-Name</span></span>
<span data-ttu-id="53412-131">Eylem kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="53412-131">Name of action rule.</span></span>

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

### <span data-ttu-id="53412-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53412-132">-ResourceGroupName</span></span>
<span data-ttu-id="53412-133">Eylem kuralının bulunduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="53412-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="53412-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="53412-134">-ResourceId</span></span>
<span data-ttu-id="53412-135">Kaynak No 'dan eylem kuralı alın.</span><span class="sxs-lookup"><span data-stu-id="53412-135">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="53412-136">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="53412-136">-Severity</span></span>
<span data-ttu-id="53412-137">Uyarının önem derecesine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="53412-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="53412-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53412-138">-TargetResourceGroup</span></span>
<span data-ttu-id="53412-139">Uyarının hedef kaynağının kaynak grubu adına filtre uygulama.</span><span class="sxs-lookup"><span data-stu-id="53412-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="53412-140">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="53412-140">-TargetResourceId</span></span>
<span data-ttu-id="53412-141">Uyarının hedef kaynağının kaynak kimliği 'ne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="53412-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="53412-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="53412-142">-TargetResourceType</span></span>
<span data-ttu-id="53412-143">Hedef uyarının kaynak türüne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="53412-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="53412-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53412-144">CommonParameters</span></span>
<span data-ttu-id="53412-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53412-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53412-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="53412-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53412-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53412-147">INPUTS</span></span>

### <span data-ttu-id="53412-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="53412-148">None</span></span>

## <span data-ttu-id="53412-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53412-149">OUTPUTS</span></span>

### <span data-ttu-id="53412-150">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="53412-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="53412-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53412-151">NOTES</span></span>

## <span data-ttu-id="53412-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53412-152">RELATED LINKS</span></span>
