---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 96afdd5e0bdf336dec5f2ff1b2a9ecfccf8bac12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932822"
---
# <span data-ttu-id="f7f2c-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f7f2c-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="f7f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f2c-103">İlke düzeltmesini siler.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="f7f2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7f2c-104">SYNTAX</span></span>

### <span data-ttu-id="f7f2c-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7f2c-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f2c-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f7f2c-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f2c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7f2c-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f2c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="f7f2c-109">**Remove-Azpolicydüzeltme** cmdlet 'i bir ilke düzeltmesini siler.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="f7f2c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7f2c-110">EXAMPLES</span></span>

### <span data-ttu-id="f7f2c-111">Örnek 1: kaynak grubu kapsamındaki bir ilke düzeltmesini silme</span><span class="sxs-lookup"><span data-stu-id="f7f2c-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="f7f2c-112">Bu komut, ' myRG ' kaynak grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="f7f2c-113">Örnek 2: yöneltme yoluyla yönetim grubu düzeltmesini silme</span><span class="sxs-lookup"><span data-stu-id="f7f2c-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="f7f2c-114">Bu komut, ' MG1 ' yönetim grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="f7f2c-115">Kaynak silinmeden önce bir onay istemi görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="f7f2c-116">Örnek 3: ilke düzeltmesini Iptal etme ve silme</span><span class="sxs-lookup"><span data-stu-id="f7f2c-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="f7f2c-117">Bu komut, ' myRG ' kaynak grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="f7f2c-118">Düzeltme devam ediyorsa silinmeden önce iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="f7f2c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7f2c-119">PARAMETERS</span></span>

### <span data-ttu-id="f7f2c-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="f7f2c-120">-AllowStop</span></span>
<span data-ttu-id="f7f2c-121">Devam eden devam ediyorsa düzeltmenin iptal edilmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="f7f2c-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="f7f2c-122">-AsJob</span></span>
<span data-ttu-id="f7f2c-123">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f7f2c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f2c-124">-DefaultProfile</span></span>
<span data-ttu-id="f7f2c-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f2c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7f2c-126">-InputObject</span></span>
<span data-ttu-id="f7f2c-127">Düzeltme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-127">The Remediation object.</span></span>

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

### <span data-ttu-id="f7f2c-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f2c-128">-ManagementGroupName</span></span>
<span data-ttu-id="f7f2c-129">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-129">Management group ID.</span></span>

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

### <span data-ttu-id="f7f2c-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7f2c-130">-Name</span></span>
<span data-ttu-id="f7f2c-131">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-131">Resource name.</span></span>

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

### <span data-ttu-id="f7f2c-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f7f2c-132">-PassThru</span></span>
<span data-ttu-id="f7f2c-133">Komut başarılı bir şekilde tamamlandığında doğru döner.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="f7f2c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f2c-134">-ResourceGroupName</span></span>
<span data-ttu-id="f7f2c-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-135">Resource group name.</span></span>

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

### <span data-ttu-id="f7f2c-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f7f2c-136">-ResourceId</span></span>
<span data-ttu-id="f7f2c-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-137">Resource ID.</span></span>

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

### <span data-ttu-id="f7f2c-138">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="f7f2c-138">-Scope</span></span>
<span data-ttu-id="f7f2c-139">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-139">Scope of the resource.</span></span>
<span data-ttu-id="f7f2c-140">Yani.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-140">E.g.</span></span>
<span data-ttu-id="f7f2c-141">'/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="f7f2c-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7f2c-142">-Confirm</span></span>
<span data-ttu-id="f7f2c-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f2c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f2c-144">-WhatIf</span></span>
<span data-ttu-id="f7f2c-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f2c-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f2c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f2c-147">CommonParameters</span></span>
<span data-ttu-id="f7f2c-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7f2c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f2c-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f2c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f2c-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7f2c-150">INPUTS</span></span>

### <span data-ttu-id="f7f2c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f7f2c-151">System.String</span></span>

### <span data-ttu-id="f7f2c-152">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="f7f2c-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="f7f2c-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7f2c-153">OUTPUTS</span></span>

### <span data-ttu-id="f7f2c-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7f2c-154">System.Boolean</span></span>

## <span data-ttu-id="f7f2c-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7f2c-155">NOTES</span></span>

## <span data-ttu-id="f7f2c-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7f2c-156">RELATED LINKS</span></span>
