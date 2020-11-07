---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b88fa6ea7a44d17843b72da162eec374e2c861f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759389"
---
# <span data-ttu-id="c6fe8-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c6fe8-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="c6fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fe8-103">İlke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="c6fe8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6fe8-104">SYNTAX</span></span>

### <span data-ttu-id="c6fe8-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c6fe8-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6fe8-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6fe8-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6fe8-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6fe8-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6fe8-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6fe8-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6fe8-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6fe8-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6fe8-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6fe8-110">DESCRIPTION</span></span>
<span data-ttu-id="c6fe8-111">**New-AzPolicyAssignment** cmdlet 'i bir ilke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="c6fe8-112">Bir ilke ve kapsam belirtin.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="c6fe8-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6fe8-113">EXAMPLES</span></span>

### <span data-ttu-id="c6fe8-114">Örnek 1: Kaynak Grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="c6fe8-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c6fe8-115">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c6fe8-116">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c6fe8-117">Son komut, $ResourceGroup **RESOURCEID** özelliğiyle tanımlanan kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="c6fe8-118">Örnek 2: ilke parametresi nesnesiyle kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="c6fe8-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="c6fe8-119">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c6fe8-120">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c6fe8-121">İkinci komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c6fe8-122">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="c6fe8-123">Üçüncü ve dördüncü komutlar, ad içinde "Doğu" ile tüm Azure bölgelerini içeren bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="c6fe8-124">Komutlar bu nesneyi $AllowedLocations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="c6fe8-125">Son komutu, $AllowedLocations ilke parametre nesnesini kullanarak kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="c6fe8-126">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c6fe8-127">Örnek 3: ilke parametresi dosyası olan kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="c6fe8-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="c6fe8-128">Yerel çalışma dizininde aşağıdaki içerikle _AllowedLocations.js_ adlı bir dosya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="c6fe8-129">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c6fe8-130">İkinci komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c6fe8-131">Son komut, ilkeyi, yerel çalışma dizininden AllowedLocations.jsilke parametre dosyasını kullanarak $ResourceGroup **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki $Policy atar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="c6fe8-132">Örnek 4: yönetilen kimlikte Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="c6fe8-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="c6fe8-133">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c6fe8-134">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c6fe8-135">Son komut $Policy ilkeyi kaynak grubuna atar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="c6fe8-136">Yönetilen kimlik otomatik olarak oluşturulur ve ilke atamalarına atanır.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="c6fe8-137">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6fe8-137">PARAMETERS</span></span>

### <span data-ttu-id="c6fe8-138">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c6fe8-138">-ApiVersion</span></span>
<span data-ttu-id="c6fe8-139">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c6fe8-140">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c6fe8-141">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="c6fe8-141">-AssignIdentity</span></span>
<span data-ttu-id="c6fe8-142">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="c6fe8-143">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="c6fe8-144">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="c6fe8-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fe8-145">-DefaultProfile</span></span>
<span data-ttu-id="c6fe8-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c6fe8-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6fe8-147">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c6fe8-147">-Description</span></span>
<span data-ttu-id="c6fe8-148">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="c6fe8-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="c6fe8-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6fe8-149">-DisplayName</span></span>
<span data-ttu-id="c6fe8-150">İlke ataması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="c6fe8-151">-Konum</span><span class="sxs-lookup"><span data-stu-id="c6fe8-151">-Location</span></span>
<span data-ttu-id="c6fe8-152">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-152">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="c6fe8-153">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-153">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="c6fe8-154">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c6fe8-154">-Metadata</span></span>
<span data-ttu-id="c6fe8-155">Yeni ilke atamasının meta verileri.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-155">The metadata for the new policy assignment.</span></span> <span data-ttu-id="c6fe8-156">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-156">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="c6fe8-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6fe8-157">-Name</span></span>
<span data-ttu-id="c6fe8-158">İlke ataması için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-158">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="c6fe8-159">-NotScope</span><span class="sxs-lookup"><span data-stu-id="c6fe8-159">-NotScope</span></span>
<span data-ttu-id="c6fe8-160">İlke ataması için olmayan kapsamlar.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-160">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="c6fe8-161">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6fe8-161">-PolicyDefinition</span></span>
<span data-ttu-id="c6fe8-162">İlke kuralını içeren **Pspolicydefinition** nesnesi olarak bir ilke belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-162">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fe8-163">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="c6fe8-163">-PolicyParameter</span></span>
<span data-ttu-id="c6fe8-164">İlke parametresi dosya yolu veya ilke parametresi dizesi.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-164">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fe8-165">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="c6fe8-165">-PolicyParameterObject</span></span>
<span data-ttu-id="c6fe8-166">İlke parametresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-166">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6fe8-167">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c6fe8-167">-PolicySetDefinition</span></span>
<span data-ttu-id="c6fe8-168">İlke kümesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-168">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fe8-169">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c6fe8-169">-Pre</span></span>
<span data-ttu-id="c6fe8-170">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-170">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c6fe8-171">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c6fe8-171">-Scope</span></span>
<span data-ttu-id="c6fe8-172">İlkenin atanacağı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-172">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="c6fe8-173">Örneğin, kaynak grubuna ilke atamak için aşağıdakileri belirtin: `/subscriptions/` ABONELIK kimliği `/resourcegroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c6fe8-173">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="c6fe8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fe8-174">CommonParameters</span></span>
<span data-ttu-id="c6fe8-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6fe8-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6fe8-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fe8-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6fe8-177">INPUTS</span></span>

### <span data-ttu-id="c6fe8-178">System. String</span><span class="sxs-lookup"><span data-stu-id="c6fe8-178">System.String</span></span>

### <span data-ttu-id="c6fe8-179">System. String []</span><span class="sxs-lookup"><span data-stu-id="c6fe8-179">System.String[]</span></span>

### <span data-ttu-id="c6fe8-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c6fe8-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c6fe8-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6fe8-181">OUTPUTS</span></span>

### <span data-ttu-id="c6fe8-182">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c6fe8-182">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c6fe8-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6fe8-183">NOTES</span></span>

## <span data-ttu-id="c6fe8-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6fe8-184">RELATED LINKS</span></span>

[<span data-ttu-id="c6fe8-185">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6fe8-185">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c6fe8-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c6fe8-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c6fe8-187">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c6fe8-187">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="c6fe8-188">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c6fe8-188">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


