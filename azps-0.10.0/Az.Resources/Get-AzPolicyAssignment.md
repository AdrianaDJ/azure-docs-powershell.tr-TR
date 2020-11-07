---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 160cff39918691c310de6931cd57cb415774d7e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936442"
---
# <span data-ttu-id="95086-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="95086-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="95086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95086-102">SYNOPSIS</span></span>
<span data-ttu-id="95086-103">İlke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="95086-103">Gets policy assignments.</span></span>

## <span data-ttu-id="95086-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95086-104">SYNTAX</span></span>

### <span data-ttu-id="95086-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95086-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95086-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95086-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95086-107">Includeharfin Dentparameterset</span><span class="sxs-lookup"><span data-stu-id="95086-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95086-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="95086-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="95086-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="95086-109">DESCRIPTION</span></span>
<span data-ttu-id="95086-110">**Get-AzPolicyAssignment** cmdlet 'i tüm ilke atamalarını veya belirli atamaları alır.</span><span class="sxs-lookup"><span data-stu-id="95086-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="95086-111">Ad ve kapsam veya KIMLIĞE göre alınacak bir ilke ataması belirleyin.</span><span class="sxs-lookup"><span data-stu-id="95086-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="95086-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95086-112">EXAMPLES</span></span>

### <span data-ttu-id="95086-113">Örnek 1: tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="95086-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="95086-114">Bu komut, tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="95086-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="95086-115">Örnek 2: belirli bir ilke ataması alma</span><span class="sxs-lookup"><span data-stu-id="95086-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="95086-116">İlk komut, Get-AzResourceGroup cmdlet'i kullanarak ResourceGroup11 adlı bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="95086-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="95086-117">İkinci komut, $ResourceGroup **RESOURCEID** özelliğinin tanımladığı kapsam için PolicyAssignment07 adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="95086-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="95086-118">Örnek 3: yönetim grubuna atanan tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="95086-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="95086-119">İlk komut Sorgulanacak yönetim grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="95086-120">İkinci komut, ' myManagementGroup ' KIMLIĞINE sahip yönetim grubuna atanmış tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="95086-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="95086-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95086-121">PARAMETERS</span></span>

### <span data-ttu-id="95086-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="95086-122">-ApiVersion</span></span>
<span data-ttu-id="95086-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="95086-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="95086-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="95086-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95086-125">-DefaultProfile</span></span>
<span data-ttu-id="95086-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="95086-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95086-127">-ID</span><span class="sxs-lookup"><span data-stu-id="95086-127">-Id</span></span>
<span data-ttu-id="95086-128">Bu cmdlet 'in aldığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="95086-129">-Includealt</span><span class="sxs-lookup"><span data-stu-id="95086-129">-IncludeDescendent</span></span>
<span data-ttu-id="95086-130">Döndürülen ilke atamalarının listesinin, üst kapsamlardan ve alt kapsamlardan olanlar da içinde olmak üzere, verilen kapsamla ilgili tüm ödevleri içermesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="95086-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="95086-131">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="95086-131">-InformationAction</span></span>
<span data-ttu-id="95086-132">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="95086-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="95086-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95086-134">'A</span><span class="sxs-lookup"><span data-stu-id="95086-134">Continue</span></span>
- <span data-ttu-id="95086-135">Manıza</span><span class="sxs-lookup"><span data-stu-id="95086-135">Ignore</span></span>
- <span data-ttu-id="95086-136">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="95086-136">Inquire</span></span>
- <span data-ttu-id="95086-137">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="95086-137">SilentlyContinue</span></span>
- <span data-ttu-id="95086-138">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="95086-138">Stop</span></span>
- <span data-ttu-id="95086-139">Biliriz</span><span class="sxs-lookup"><span data-stu-id="95086-139">Suspend</span></span>

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

### <span data-ttu-id="95086-140">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="95086-140">-InformationVariable</span></span>
<span data-ttu-id="95086-141">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="95086-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="95086-142">-Name</span></span>
<span data-ttu-id="95086-143">Bu cmdlet 'in aldığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="95086-144">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="95086-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="95086-145">Bu cmdlet 'in aldığı ilke atamalarının ilke tanımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="95086-146">-Pre-</span><span class="sxs-lookup"><span data-stu-id="95086-146">-Pre</span></span>
<span data-ttu-id="95086-147">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="95086-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="95086-148">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="95086-148">-Scope</span></span>
<span data-ttu-id="95086-149">Bu cmdlet 'in aldığı ödev için ilkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="95086-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="95086-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95086-150">CommonParameters</span></span>
<span data-ttu-id="95086-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95086-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95086-152">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95086-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95086-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95086-153">INPUTS</span></span>

## <span data-ttu-id="95086-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95086-154">OUTPUTS</span></span>

## <span data-ttu-id="95086-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95086-155">NOTES</span></span>

## <span data-ttu-id="95086-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95086-156">RELATED LINKS</span></span>

[<span data-ttu-id="95086-157">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="95086-157">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="95086-158">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="95086-158">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="95086-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="95086-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


