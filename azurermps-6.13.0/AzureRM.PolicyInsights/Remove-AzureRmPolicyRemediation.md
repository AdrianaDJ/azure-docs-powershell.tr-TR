---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762301"
---
# <span data-ttu-id="d9b89-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d9b89-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="d9b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9b89-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b89-103">İlke düzeltmesini siler.</span><span class="sxs-lookup"><span data-stu-id="d9b89-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9b89-104">SYNTAX</span></span>

### <span data-ttu-id="d9b89-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d9b89-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b89-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d9b89-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b89-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9b89-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b89-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9b89-108">DESCRIPTION</span></span>
<span data-ttu-id="d9b89-109">**Remove-AzureRmPolicyRemediation** cmdlet 'i bir ilke düzeltmesini siler.</span><span class="sxs-lookup"><span data-stu-id="d9b89-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="d9b89-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9b89-110">EXAMPLES</span></span>

### <span data-ttu-id="d9b89-111">Örnek 1: kaynak grubu kapsamındaki bir ilke düzeltmesini silme</span><span class="sxs-lookup"><span data-stu-id="d9b89-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="d9b89-112">Bu komut, ' myRG ' kaynak grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="d9b89-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="d9b89-113">Örnek 2: yöneltme yoluyla yönetim grubu düzeltmesini silme</span><span class="sxs-lookup"><span data-stu-id="d9b89-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="d9b89-114">Bu komut, ' MG1 ' yönetim grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="d9b89-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="d9b89-115">Kaynak silinmeden önce bir onay istemi görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="d9b89-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="d9b89-116">Örnek 3: ilke düzeltmesini Iptal etme ve silme</span><span class="sxs-lookup"><span data-stu-id="d9b89-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="d9b89-117">Bu komut, ' myRG ' kaynak grubundaki ' remediation1 ' adındaki düzeltmeyi siler.</span><span class="sxs-lookup"><span data-stu-id="d9b89-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="d9b89-118">Düzeltme devam ediyorsa silinmeden önce iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="d9b89-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="d9b89-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9b89-119">PARAMETERS</span></span>

### <span data-ttu-id="d9b89-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="d9b89-120">-AllowStop</span></span>
<span data-ttu-id="d9b89-121">Devam eden devam ediyorsa düzeltmenin iptal edilmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="d9b89-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="d9b89-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="d9b89-122">-AsJob</span></span>
<span data-ttu-id="d9b89-123">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d9b89-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d9b89-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b89-124">-DefaultProfile</span></span>
<span data-ttu-id="d9b89-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9b89-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9b89-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9b89-126">-InputObject</span></span>
<span data-ttu-id="d9b89-127">Düzeltme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d9b89-127">The Remediation object.</span></span>

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

### <span data-ttu-id="d9b89-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b89-128">-ManagementGroupName</span></span>
<span data-ttu-id="d9b89-129">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d9b89-129">Management group ID.</span></span>

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

### <span data-ttu-id="d9b89-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9b89-130">-Name</span></span>
<span data-ttu-id="d9b89-131">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d9b89-131">Resource name.</span></span>

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

### <span data-ttu-id="d9b89-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d9b89-132">-PassThru</span></span>
<span data-ttu-id="d9b89-133">Komut başarılı bir şekilde tamamlandığında doğru döner.</span><span class="sxs-lookup"><span data-stu-id="d9b89-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="d9b89-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b89-134">-ResourceGroupName</span></span>
<span data-ttu-id="d9b89-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d9b89-135">Resource group name.</span></span>

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

### <span data-ttu-id="d9b89-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d9b89-136">-ResourceId</span></span>
<span data-ttu-id="d9b89-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d9b89-137">Resource ID.</span></span>

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

### <span data-ttu-id="d9b89-138">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="d9b89-138">-Scope</span></span>
<span data-ttu-id="d9b89-139">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="d9b89-139">Scope of the resource.</span></span>
<span data-ttu-id="d9b89-140">Yani.</span><span class="sxs-lookup"><span data-stu-id="d9b89-140">E.g.</span></span>
<span data-ttu-id="d9b89-141">'/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="d9b89-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="d9b89-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9b89-142">-Confirm</span></span>
<span data-ttu-id="d9b89-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9b89-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b89-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b89-144">-WhatIf</span></span>
<span data-ttu-id="d9b89-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9b89-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b89-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9b89-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b89-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b89-147">CommonParameters</span></span>
<span data-ttu-id="d9b89-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9b89-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b89-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b89-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b89-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9b89-150">INPUTS</span></span>

### <span data-ttu-id="d9b89-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d9b89-151">System.String</span></span>

### <span data-ttu-id="d9b89-152">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="d9b89-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="d9b89-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9b89-153">OUTPUTS</span></span>

### <span data-ttu-id="d9b89-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9b89-154">System.Boolean</span></span>

## <span data-ttu-id="d9b89-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9b89-155">NOTES</span></span>

## <span data-ttu-id="d9b89-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9b89-156">RELATED LINKS</span></span>
