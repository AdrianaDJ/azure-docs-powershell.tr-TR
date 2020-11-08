---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274709"
---
# <span data-ttu-id="0b2b6-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0b2b6-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="0b2b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2b6-103">Devam eden bir ilke düzeltmesini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="0b2b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b2b6-104">SYNTAX</span></span>

### <span data-ttu-id="0b2b6-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b2b6-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2b6-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0b2b6-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2b6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b2b6-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2b6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b2b6-108">DESCRIPTION</span></span>
<span data-ttu-id="0b2b6-109">**Stop-Azpolicydüzeltme** cmdlet 'i devam eden bir ilke düzeltmesini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="0b2b6-110">Etkin dağıtımlar iptal edilecek ve Yeni dağıtımlar oluşturulmayacak.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="0b2b6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b2b6-111">EXAMPLES</span></span>

### <span data-ttu-id="0b2b6-112">Örnek 1: kaynak grubu kapsamındaki bir ilke düzeltmesini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="0b2b6-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="0b2b6-113">Bu komut, ' myRG ' kaynak grubundaki ' remediation1 ' adındaki düzeltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="0b2b6-114">Örnek 2: bir yönetim grubu düzeltmesini boru aracılığıyla Iptal etme</span><span class="sxs-lookup"><span data-stu-id="0b2b6-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="0b2b6-115">Bu komut, ' MG1 ' yönetim grubundaki ' remediation1 ' adındaki düzeltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="0b2b6-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b2b6-116">PARAMETERS</span></span>

### <span data-ttu-id="0b2b6-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="0b2b6-117">-AsJob</span></span>
<span data-ttu-id="0b2b6-118">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0b2b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2b6-119">-DefaultProfile</span></span>
<span data-ttu-id="0b2b6-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2b6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b2b6-121">-InputObject</span></span>
<span data-ttu-id="0b2b6-122">Düzeltme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b6-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2b6-123">-ManagementGroupName</span></span>
<span data-ttu-id="0b2b6-124">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b6-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b2b6-125">-Name</span></span>
<span data-ttu-id="0b2b6-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b6-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0b2b6-127">-PassThru</span></span>
<span data-ttu-id="0b2b6-128">Komut başarılı bir şekilde tamamlandığında doğru döner.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="0b2b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="0b2b6-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b6-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0b2b6-131">-ResourceId</span></span>
<span data-ttu-id="0b2b6-132">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b6-133">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0b2b6-133">-Scope</span></span>
<span data-ttu-id="0b2b6-134">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-134">Scope of the resource.</span></span>
<span data-ttu-id="0b2b6-135">Yani.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-135">E.g.</span></span>
<span data-ttu-id="0b2b6-136">'/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b6-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b2b6-137">-Confirm</span></span>
<span data-ttu-id="0b2b6-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2b6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2b6-139">-WhatIf</span></span>
<span data-ttu-id="0b2b6-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2b6-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2b6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2b6-142">CommonParameters</span></span>
<span data-ttu-id="0b2b6-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2b6-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b2b6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2b6-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b2b6-145">INPUTS</span></span>

### <span data-ttu-id="0b2b6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0b2b6-146">System.String</span></span>

### <span data-ttu-id="0b2b6-147">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="0b2b6-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="0b2b6-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b2b6-148">OUTPUTS</span></span>

### <span data-ttu-id="0b2b6-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b2b6-149">System.Boolean</span></span>

## <span data-ttu-id="0b2b6-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b2b6-150">NOTES</span></span>

## <span data-ttu-id="0b2b6-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b2b6-151">RELATED LINKS</span></span>
