---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939484"
---
# <span data-ttu-id="0f441-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f441-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="0f441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f441-102">SYNOPSIS</span></span>
<span data-ttu-id="0f441-103">İlke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0f441-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f441-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f441-104">SYNTAX</span></span>

### <span data-ttu-id="0f441-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f441-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f441-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f441-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f441-107">Includeharfin Dentparameterset</span><span class="sxs-lookup"><span data-stu-id="0f441-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f441-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="0f441-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f441-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f441-109">DESCRIPTION</span></span>
<span data-ttu-id="0f441-110">**Get-AzureRmPolicyAssignment** cmdlet 'i tüm ilke atamalarını veya belirli atamaları alır.</span><span class="sxs-lookup"><span data-stu-id="0f441-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="0f441-111">Ad ve kapsam veya KIMLIĞE göre alınacak bir ilke ataması belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0f441-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="0f441-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f441-112">EXAMPLES</span></span>

### <span data-ttu-id="0f441-113">Örnek 1: tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="0f441-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="0f441-114">Bu komut, tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0f441-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="0f441-115">Örnek 2: belirli bir ilke ataması alma</span><span class="sxs-lookup"><span data-stu-id="0f441-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="0f441-116">İlk komut, Get-AzureRMResourceGroup cmdlet'i kullanarak ResourceGroup11 adlı bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0f441-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0f441-117">İkinci komut, $ResourceGroup **RESOURCEID** özelliğinin tanımladığı kapsam için PolicyAssignment07 adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="0f441-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="0f441-118">Örnek 3: yönetim grubuna atanan tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="0f441-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="0f441-119">İlk komut Sorgulanacak yönetim grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="0f441-120">İkinci komut, ' myManagementGroup ' KIMLIĞINE sahip yönetim grubuna atanmış tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0f441-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="0f441-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f441-121">PARAMETERS</span></span>

### <span data-ttu-id="0f441-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0f441-122">-ApiVersion</span></span>
<span data-ttu-id="0f441-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0f441-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0f441-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0f441-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f441-125">-DefaultProfile</span></span>
<span data-ttu-id="0f441-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0f441-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f441-127">-ID</span><span class="sxs-lookup"><span data-stu-id="0f441-127">-Id</span></span>
<span data-ttu-id="0f441-128">Bu cmdlet 'in aldığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f441-129">-Includealt</span><span class="sxs-lookup"><span data-stu-id="0f441-129">-IncludeDescendent</span></span>
<span data-ttu-id="0f441-130">Döndürülen ilke atamalarının listesinin, üst kapsamlardan ve alt kapsamlardan olanlar da içinde olmak üzere, verilen kapsamla ilgili tüm ödevleri içermesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0f441-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f441-131">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0f441-131">-InformationAction</span></span>
<span data-ttu-id="0f441-132">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0f441-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0f441-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0f441-134">'A</span><span class="sxs-lookup"><span data-stu-id="0f441-134">Continue</span></span>
- <span data-ttu-id="0f441-135">Manıza</span><span class="sxs-lookup"><span data-stu-id="0f441-135">Ignore</span></span>
- <span data-ttu-id="0f441-136">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="0f441-136">Inquire</span></span>
- <span data-ttu-id="0f441-137">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="0f441-137">SilentlyContinue</span></span>
- <span data-ttu-id="0f441-138">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="0f441-138">Stop</span></span>
- <span data-ttu-id="0f441-139">Biliriz</span><span class="sxs-lookup"><span data-stu-id="0f441-139">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f441-140">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="0f441-140">-InformationVariable</span></span>
<span data-ttu-id="0f441-141">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-141">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f441-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f441-142">-Name</span></span>
<span data-ttu-id="0f441-143">Bu cmdlet 'in aldığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f441-144">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="0f441-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="0f441-145">Bu cmdlet 'in aldığı ilke atamalarının ilke tanımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f441-146">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0f441-146">-Pre</span></span>
<span data-ttu-id="0f441-147">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f441-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0f441-148">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0f441-148">-Scope</span></span>
<span data-ttu-id="0f441-149">Bu cmdlet 'in aldığı ödev için ilkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f441-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f441-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f441-150">CommonParameters</span></span>
<span data-ttu-id="0f441-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f441-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f441-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f441-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f441-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f441-153">INPUTS</span></span>

## <span data-ttu-id="0f441-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f441-154">OUTPUTS</span></span>

## <span data-ttu-id="0f441-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f441-155">NOTES</span></span>

## <span data-ttu-id="0f441-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f441-156">RELATED LINKS</span></span>

[<span data-ttu-id="0f441-157">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f441-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="0f441-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f441-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="0f441-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f441-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


