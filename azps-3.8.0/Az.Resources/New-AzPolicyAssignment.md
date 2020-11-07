---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 2ae25ea7679655c4bc10f8eea714cba851bc8c9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938048"
---
# <span data-ttu-id="a1bb1-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1bb1-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="a1bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bb1-103">İlke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="a1bb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1bb1-104">SYNTAX</span></span>

### <span data-ttu-id="a1bb1-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1bb1-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1bb1-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1bb1-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1bb1-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1bb1-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1bb1-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1bb1-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1bb1-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1bb1-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1bb1-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1bb1-110">DESCRIPTION</span></span>
<span data-ttu-id="a1bb1-111">**New-AzPolicyAssignment** cmdlet 'i bir ilke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="a1bb1-112">Bir ilke ve kapsam belirtin.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="a1bb1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1bb1-113">EXAMPLES</span></span>

### <span data-ttu-id="a1bb1-114">Örnek 1: abonelik düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a1bb1-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="a1bb1-115">İlk komut, Get-AzSubscription cmdlet 'ini kullanarak Subscription01 adlı bir aboneliği alır ve $Subscription değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="a1bb1-116">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a1bb1-117">Son komutu, aboneliği abonelik kapsamı dizesi tarafından tanımlanan aboneliğin düzeyine $Policy atar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="a1bb1-118">Örnek 2: Kaynak Grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a1bb1-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="a1bb1-119">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a1bb1-120">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a1bb1-121">Son komut, $ResourceGroup **RESOURCEID** özelliğiyle tanımlanan kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="a1bb1-122">Örnek 3: ilke parametresi nesnesi olan kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a1bb1-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="a1bb1-123">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a1bb1-124">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a1bb1-125">İkinci komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a1bb1-126">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="a1bb1-127">Üçüncü ve dördüncü komutlar, ad içinde "Doğu" ile tüm Azure bölgelerini içeren bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="a1bb1-128">Komutlar bu nesneyi $AllowedLocations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="a1bb1-129">Son komutu, $AllowedLocations ilke parametre nesnesini kullanarak kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="a1bb1-130">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="a1bb1-131">Örnek 4: ilke parametresi dosyası olan kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a1bb1-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="a1bb1-132">Yerel çalışma dizininde aşağıdaki içerikle _AllowedLocations.js_ adlı bir dosya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="a1bb1-133">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a1bb1-134">İkinci komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a1bb1-135">Son komut, ilkeyi, yerel çalışma dizininden AllowedLocations.jsilke parametre dosyasını kullanarak $ResourceGroup **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki $Policy atar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="a1bb1-136">Örnek 5: yönetilen kimlikle Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a1bb1-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="a1bb1-137">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a1bb1-138">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a1bb1-139">Son komut $Policy ilkeyi kaynak grubuna atar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="a1bb1-140">Yönetilen kimlik otomatik olarak oluşturulur ve ilke atamalarına atanır.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="a1bb1-141">Örnek 6: zorlama modu özelliğiyle Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a1bb1-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="a1bb1-142">İlk komut, Get-AzSubscription cmdlet 'ini kullanarak Subscription01 adlı bir aboneliği alır ve $Subscription değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="a1bb1-143">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a1bb1-144">Son komutu, aboneliği abonelik kapsamı dizesi tarafından tanımlanan aboneliğin düzeyine $Policy atar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="a1bb1-145">Ödev, bir EnforcementMode değeri olan _Donotenforce_ gibi ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="a1bb1-146">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1bb1-146">PARAMETERS</span></span>

### <span data-ttu-id="a1bb1-147">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a1bb1-147">-ApiVersion</span></span>
<span data-ttu-id="a1bb1-148">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a1bb1-149">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a1bb1-150">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="a1bb1-150">-AssignIdentity</span></span>
<span data-ttu-id="a1bb1-151">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="a1bb1-152">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="a1bb1-153">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="a1bb1-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bb1-154">-DefaultProfile</span></span>
<span data-ttu-id="a1bb1-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a1bb1-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1bb1-156">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a1bb1-156">-Description</span></span>
<span data-ttu-id="a1bb1-157">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="a1bb1-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="a1bb1-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a1bb1-158">-DisplayName</span></span>
<span data-ttu-id="a1bb1-159">İlke ataması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="a1bb1-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="a1bb1-160">-EnforcementMode</span></span>
<span data-ttu-id="a1bb1-161">İlke ataması için zorlama modu.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="a1bb1-162">Geçerli değerler varsayılan, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-162">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bb1-163">-Konum</span><span class="sxs-lookup"><span data-stu-id="a1bb1-163">-Location</span></span>
<span data-ttu-id="a1bb1-164">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="a1bb1-165">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="a1bb1-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a1bb1-166">-Metadata</span></span>
<span data-ttu-id="a1bb1-167">Yeni ilke atamasının meta verileri.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="a1bb1-168">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="a1bb1-169">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1bb1-169">-Name</span></span>
<span data-ttu-id="a1bb1-170">İlke ataması için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="a1bb1-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="a1bb1-171">-NotScope</span></span>
<span data-ttu-id="a1bb1-172">İlke ataması için olmayan kapsamlar.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="a1bb1-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a1bb1-173">-PolicyDefinition</span></span>
<span data-ttu-id="a1bb1-174">İlke kuralını içeren **Pspolicydefinition** nesnesi olarak bir ilke belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="a1bb1-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="a1bb1-175">-PolicyParameter</span></span>
<span data-ttu-id="a1bb1-176">İlke parametresi dosya yolu veya ilke parametresi dizesi.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="a1bb1-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1bb1-177">-PolicyParameterObject</span></span>
<span data-ttu-id="a1bb1-178">İlke parametresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="a1bb1-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a1bb1-179">-PolicySetDefinition</span></span>
<span data-ttu-id="a1bb1-180">İlke kümesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="a1bb1-181">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a1bb1-181">-Pre</span></span>
<span data-ttu-id="a1bb1-182">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1bb1-183">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a1bb1-183">-Scope</span></span>
<span data-ttu-id="a1bb1-184">İlkenin atanacağı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="a1bb1-185">Örneğin, kaynak grubuna ilke atamak için aşağıdakileri belirtin: `/subscriptions/` ABONELIK kimliği `/resourcegroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a1bb1-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="a1bb1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bb1-186">CommonParameters</span></span>
<span data-ttu-id="a1bb1-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bb1-188">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1bb1-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bb1-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1bb1-189">INPUTS</span></span>

### <span data-ttu-id="a1bb1-190">System. String</span><span class="sxs-lookup"><span data-stu-id="a1bb1-190">System.String</span></span>

### <span data-ttu-id="a1bb1-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="a1bb1-191">System.String[]</span></span>

### <span data-ttu-id="a1bb1-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a1bb1-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a1bb1-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1bb1-193">OUTPUTS</span></span>

### <span data-ttu-id="a1bb1-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a1bb1-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a1bb1-195">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1bb1-195">NOTES</span></span>

## <span data-ttu-id="a1bb1-196">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1bb1-196">RELATED LINKS</span></span>

[<span data-ttu-id="a1bb1-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a1bb1-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a1bb1-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1bb1-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="a1bb1-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1bb1-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="a1bb1-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1bb1-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


