---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 71f3c6ab80fd0ba44d715cb25b4bf690e44359c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588381"
---
# <span data-ttu-id="ae206-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ae206-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="ae206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae206-102">SYNOPSIS</span></span>
<span data-ttu-id="ae206-103">İlke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="ae206-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae206-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae206-104">SYNTAX</span></span>

### <span data-ttu-id="ae206-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ae206-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ae206-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae206-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ae206-107">Includeharfin Dentparameterset</span><span class="sxs-lookup"><span data-stu-id="ae206-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ae206-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="ae206-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ae206-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae206-109">DESCRIPTION</span></span>
<span data-ttu-id="ae206-110">**Get-AzureRmPolicyAssignment** cmdlet 'i tüm ilke atamalarını veya belirli atamaları alır.</span><span class="sxs-lookup"><span data-stu-id="ae206-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="ae206-111">Ad ve kapsam veya KIMLIĞE göre alınacak bir ilke ataması belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ae206-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="ae206-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae206-112">EXAMPLES</span></span>

### <span data-ttu-id="ae206-113">Örnek 1: tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="ae206-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="ae206-114">Bu komut, tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="ae206-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="ae206-115">Örnek 2: belirli bir ilke ataması alma</span><span class="sxs-lookup"><span data-stu-id="ae206-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="ae206-116">İlk komut, Get-AzureRMResourceGroup cmdlet'i kullanarak ResourceGroup11 adlı bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ae206-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ae206-117">İkinci komut, $ResourceGroup **RESOURCEID** özelliğinin tanımladığı kapsam için PolicyAssignment07 adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="ae206-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="ae206-118">Örnek 3: yönetim grubuna atanan tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="ae206-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="ae206-119">İlk komut Sorgulanacak yönetim grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="ae206-120">İkinci komut, ' myManagementGroup ' KIMLIĞINE sahip yönetim grubuna atanmış tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="ae206-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="ae206-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae206-121">PARAMETERS</span></span>

### <span data-ttu-id="ae206-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ae206-122">-ApiVersion</span></span>
<span data-ttu-id="ae206-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ae206-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="ae206-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ae206-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae206-125">-DefaultProfile</span></span>
<span data-ttu-id="ae206-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ae206-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae206-127">-ID</span><span class="sxs-lookup"><span data-stu-id="ae206-127">-Id</span></span>
<span data-ttu-id="ae206-128">Bu cmdlet 'in aldığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ae206-129">-Includealt</span><span class="sxs-lookup"><span data-stu-id="ae206-129">-IncludeDescendent</span></span>
<span data-ttu-id="ae206-130">Döndürülen ilke atamalarının listesinin, üst kapsamlardan ve alt kapsamlardan olanlar da içinde olmak üzere, verilen kapsamla ilgili tüm ödevleri içermesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ae206-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="ae206-131">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ae206-131">-InformationAction</span></span>
<span data-ttu-id="ae206-132">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ae206-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ae206-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ae206-134">'A</span><span class="sxs-lookup"><span data-stu-id="ae206-134">Continue</span></span>
- <span data-ttu-id="ae206-135">Manıza</span><span class="sxs-lookup"><span data-stu-id="ae206-135">Ignore</span></span>
- <span data-ttu-id="ae206-136">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ae206-136">Inquire</span></span>
- <span data-ttu-id="ae206-137">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ae206-137">SilentlyContinue</span></span>
- <span data-ttu-id="ae206-138">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ae206-138">Stop</span></span>
- <span data-ttu-id="ae206-139">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ae206-139">Suspend</span></span>

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

### <span data-ttu-id="ae206-140">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ae206-140">-InformationVariable</span></span>
<span data-ttu-id="ae206-141">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ae206-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae206-142">-Name</span></span>
<span data-ttu-id="ae206-143">Bu cmdlet 'in aldığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ae206-144">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="ae206-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="ae206-145">Bu cmdlet 'in aldığı ilke atamalarının ilke tanımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ae206-146">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ae206-146">-Pre</span></span>
<span data-ttu-id="ae206-147">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae206-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ae206-148">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ae206-148">-Scope</span></span>
<span data-ttu-id="ae206-149">Bu cmdlet 'in aldığı ödev için ilkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae206-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ae206-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae206-150">CommonParameters</span></span>
<span data-ttu-id="ae206-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae206-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae206-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae206-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae206-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae206-153">INPUTS</span></span>

## <span data-ttu-id="ae206-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae206-154">OUTPUTS</span></span>

## <span data-ttu-id="ae206-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae206-155">NOTES</span></span>

## <span data-ttu-id="ae206-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae206-156">RELATED LINKS</span></span>

[<span data-ttu-id="ae206-157">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ae206-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ae206-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ae206-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ae206-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ae206-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


