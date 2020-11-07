---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763631"
---
# <span data-ttu-id="047c8-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="047c8-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="047c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="047c8-102">SYNOPSIS</span></span>
<span data-ttu-id="047c8-103">İlke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="047c8-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="047c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="047c8-104">SYNTAX</span></span>

### <span data-ttu-id="047c8-105">Parametresiz ilke ataması (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="047c8-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="047c8-106">İlke parametresi nesnesi aracılığıyla parametrelere sahip ilke ataması</span><span class="sxs-lookup"><span data-stu-id="047c8-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="047c8-107">İlke parametresi dizesi aracılığıyla parametrelere sahip ilke ataması</span><span class="sxs-lookup"><span data-stu-id="047c8-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="047c8-108">İlke kümesi parametre nesnesi aracılığıyla parametre içeren ilke ataması</span><span class="sxs-lookup"><span data-stu-id="047c8-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="047c8-109">İlke kümesi parametre dizesi aracılığıyla parametre içeren ilke ataması</span><span class="sxs-lookup"><span data-stu-id="047c8-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="047c8-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="047c8-110">DESCRIPTION</span></span>
<span data-ttu-id="047c8-111">**New-AzureRmPolicyAssignment** cmdlet 'i bir ilke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="047c8-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="047c8-112">Bir ilke ve kapsam belirtin.</span><span class="sxs-lookup"><span data-stu-id="047c8-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="047c8-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="047c8-113">EXAMPLES</span></span>

### <span data-ttu-id="047c8-114">Örnek 1: Kaynak Grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="047c8-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="047c8-115">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="047c8-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="047c8-116">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="047c8-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="047c8-117">İkinci komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak VirtualMachinePolicy adındaki ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="047c8-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="047c8-118">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="047c8-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="047c8-119">Son komutu, ilkeyi bir kaynak grubu düzeyinde $Policy atar.</span><span class="sxs-lookup"><span data-stu-id="047c8-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="047c8-120">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="047c8-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="047c8-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="047c8-121">PARAMETERS</span></span>

### <span data-ttu-id="047c8-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="047c8-122">-ApiVersion</span></span>
<span data-ttu-id="047c8-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="047c8-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="047c8-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="047c8-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="047c8-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="047c8-125">-DisplayName</span></span>
<span data-ttu-id="047c8-126">İlke ataması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="047c8-126">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="047c8-127">-InformationAction</span></span>
<span data-ttu-id="047c8-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="047c8-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="047c8-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="047c8-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="047c8-130">'A</span><span class="sxs-lookup"><span data-stu-id="047c8-130">Continue</span></span>
- <span data-ttu-id="047c8-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="047c8-131">Ignore</span></span>
- <span data-ttu-id="047c8-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="047c8-132">Inquire</span></span>
- <span data-ttu-id="047c8-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="047c8-133">SilentlyContinue</span></span>
- <span data-ttu-id="047c8-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="047c8-134">Stop</span></span>
- <span data-ttu-id="047c8-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="047c8-135">Suspend</span></span>

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

### <span data-ttu-id="047c8-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="047c8-136">-InformationVariable</span></span>
<span data-ttu-id="047c8-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="047c8-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="047c8-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="047c8-138">-Name</span></span>
<span data-ttu-id="047c8-139">İlke ataması için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="047c8-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="047c8-140">-NotScope</span></span>
<span data-ttu-id="047c8-141">İlke ataması için olmayan kapsamlar.</span><span class="sxs-lookup"><span data-stu-id="047c8-141">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="047c8-142">-PolicyDefinition</span></span>
<span data-ttu-id="047c8-143">İlke kuralını içeren bir **Psobject** nesnesi olarak bir ilke belirtir.</span><span class="sxs-lookup"><span data-stu-id="047c8-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="047c8-144">-PolicyParameter</span></span>
<span data-ttu-id="047c8-145">İlke parametresi dosya yolu veya ilke parametresi dizesi.</span><span class="sxs-lookup"><span data-stu-id="047c8-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="047c8-146">-PolicyParameterObject</span></span>
<span data-ttu-id="047c8-147">İlke parametresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="047c8-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="047c8-148">-PolicySetDefinition</span></span>
<span data-ttu-id="047c8-149">İlke kümesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="047c8-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-150">-Pre-</span><span class="sxs-lookup"><span data-stu-id="047c8-150">-Pre</span></span>
<span data-ttu-id="047c8-151">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="047c8-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="047c8-152">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="047c8-152">-Scope</span></span>
<span data-ttu-id="047c8-153">İlkenin atanacağı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="047c8-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="047c8-154">Örneğin, kaynak grubuna ilke atamak için aşağıdakileri belirtin:</span><span class="sxs-lookup"><span data-stu-id="047c8-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="047c8-155">`/subscriptions/`abonelik KIMLIĞI `/resourcegroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="047c8-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047c8-156">-DefaultProfile</span></span>
<span data-ttu-id="047c8-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="047c8-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="047c8-158">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="047c8-158">-Description</span></span>
<span data-ttu-id="047c8-159">İlke atamasının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="047c8-159">The description for policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="047c8-160">-Sku</span></span>
<span data-ttu-id="047c8-161">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="047c8-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="047c8-162">Ücretsiz SKU için Varsayılanlar: ad = a0, katman = serbest</span><span class="sxs-lookup"><span data-stu-id="047c8-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c8-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047c8-163">CommonParameters</span></span>
<span data-ttu-id="047c8-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="047c8-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047c8-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047c8-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047c8-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="047c8-166">INPUTS</span></span>

## <span data-ttu-id="047c8-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="047c8-167">OUTPUTS</span></span>

### <span data-ttu-id="047c8-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="047c8-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="047c8-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="047c8-169">NOTES</span></span>

## <span data-ttu-id="047c8-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="047c8-170">RELATED LINKS</span></span>

[<span data-ttu-id="047c8-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="047c8-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="047c8-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="047c8-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="047c8-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="047c8-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="047c8-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="047c8-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


