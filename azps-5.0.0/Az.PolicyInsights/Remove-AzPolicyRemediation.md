---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324556"
---
# <span data-ttu-id="545fa-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="545fa-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="545fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545fa-102">SYNOPSIS</span></span>
<span data-ttu-id="545fa-103">İlke düzeltmesini siler.</span><span class="sxs-lookup"><span data-stu-id="545fa-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="545fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="545fa-104">SYNTAX</span></span>

### <span data-ttu-id="545fa-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="545fa-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545fa-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="545fa-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545fa-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="545fa-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545fa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="545fa-108">DESCRIPTION</span></span>
<span data-ttu-id="545fa-109">**Remove-Azpolicydüzeltme** cmdlet 'i bir ilke düzeltmesini siler.</span><span class="sxs-lookup"><span data-stu-id="545fa-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="545fa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="545fa-110">EXAMPLES</span></span>

### <span data-ttu-id="545fa-111">Örnek 1: kaynak grubu kapsamındaki bir ilke düzeltmesini silme</span><span class="sxs-lookup"><span data-stu-id="545fa-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="545fa-112">Bu komut, ' myRG ' kaynak grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="545fa-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="545fa-113">Örnek 2: yöneltme yoluyla yönetim grubu düzeltmesini silme</span><span class="sxs-lookup"><span data-stu-id="545fa-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="545fa-114">Bu komut, ' MG1 ' yönetim grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="545fa-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="545fa-115">Kaynak silinmeden önce bir onay istemi görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="545fa-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="545fa-116">Örnek 3: ilke düzeltmesini Iptal etme ve silme</span><span class="sxs-lookup"><span data-stu-id="545fa-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="545fa-117">Bu komut, ' myRG ' kaynak grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="545fa-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="545fa-118">Düzeltme devam ediyorsa silinmeden önce iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="545fa-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="545fa-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="545fa-119">PARAMETERS</span></span>

### <span data-ttu-id="545fa-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="545fa-120">-AllowStop</span></span>
<span data-ttu-id="545fa-121">Devam eden devam ediyorsa düzeltmenin iptal edilmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="545fa-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="545fa-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="545fa-122">-AsJob</span></span>
<span data-ttu-id="545fa-123">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="545fa-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="545fa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545fa-124">-DefaultProfile</span></span>
<span data-ttu-id="545fa-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="545fa-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545fa-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="545fa-126">-InputObject</span></span>
<span data-ttu-id="545fa-127">Düzeltme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="545fa-127">The Remediation object.</span></span>

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

### <span data-ttu-id="545fa-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="545fa-128">-ManagementGroupName</span></span>
<span data-ttu-id="545fa-129">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="545fa-129">Management group ID.</span></span>

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

### <span data-ttu-id="545fa-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="545fa-130">-Name</span></span>
<span data-ttu-id="545fa-131">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="545fa-131">Resource name.</span></span>

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

### <span data-ttu-id="545fa-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="545fa-132">-PassThru</span></span>
<span data-ttu-id="545fa-133">Komut başarılı bir şekilde tamamlandığında doğru döner.</span><span class="sxs-lookup"><span data-stu-id="545fa-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="545fa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545fa-134">-ResourceGroupName</span></span>
<span data-ttu-id="545fa-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="545fa-135">Resource group name.</span></span>

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

### <span data-ttu-id="545fa-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="545fa-136">-ResourceId</span></span>
<span data-ttu-id="545fa-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="545fa-137">Resource ID.</span></span>

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

### <span data-ttu-id="545fa-138">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="545fa-138">-Scope</span></span>
<span data-ttu-id="545fa-139">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="545fa-139">Scope of the resource.</span></span>
<span data-ttu-id="545fa-140">Yani.</span><span class="sxs-lookup"><span data-stu-id="545fa-140">E.g.</span></span>
<span data-ttu-id="545fa-141">'/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="545fa-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="545fa-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="545fa-142">-Confirm</span></span>
<span data-ttu-id="545fa-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="545fa-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545fa-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545fa-144">-WhatIf</span></span>
<span data-ttu-id="545fa-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="545fa-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545fa-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="545fa-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545fa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545fa-147">CommonParameters</span></span>
<span data-ttu-id="545fa-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="545fa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545fa-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="545fa-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545fa-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="545fa-150">INPUTS</span></span>

### <span data-ttu-id="545fa-151">System. String</span><span class="sxs-lookup"><span data-stu-id="545fa-151">System.String</span></span>

### <span data-ttu-id="545fa-152">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="545fa-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="545fa-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="545fa-153">OUTPUTS</span></span>

### <span data-ttu-id="545fa-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="545fa-154">System.Boolean</span></span>

## <span data-ttu-id="545fa-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="545fa-155">NOTES</span></span>

## <span data-ttu-id="545fa-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="545fa-156">RELATED LINKS</span></span>
