---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322813"
---
# <span data-ttu-id="ca03e-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ca03e-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="ca03e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca03e-102">SYNOPSIS</span></span>
<span data-ttu-id="ca03e-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="ca03e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca03e-104">SYNTAX</span></span>

### <span data-ttu-id="ca03e-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca03e-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca03e-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca03e-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca03e-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca03e-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca03e-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="ca03e-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca03e-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca03e-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca03e-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca03e-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca03e-111">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="ca03e-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca03e-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca03e-112">DESCRIPTION</span></span>
<span data-ttu-id="ca03e-113">**Set-AzPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="ca03e-114">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="ca03e-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="ca03e-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca03e-115">EXAMPLES</span></span>

### <span data-ttu-id="ca03e-116">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ca03e-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="ca03e-117">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="ca03e-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ca03e-118">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ca03e-119">İkinci komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="ca03e-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="ca03e-120">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ca03e-121">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="ca03e-122">Örnek 2: ilke atamalarına yönetilen kimlik ekleme</span><span class="sxs-lookup"><span data-stu-id="ca03e-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="ca03e-123">İlk komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak geçerli abonelikteki PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="ca03e-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="ca03e-124">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ca03e-125">Son komutu, ilke atamalarına yönetilen bir kimlik atar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="ca03e-126">Örnek 3: yeni ilke parametresi nesnesiyle ilke atama parametrelerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ca03e-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="ca03e-127">İlk ve ikinci komutlar adları "Fransa" veya "İngiltere" ile başlayan tüm Azure bölgelerini içeren bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca03e-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="ca03e-128">İkinci komut bu nesneyi $AllowedLocations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="ca03e-129">Üçüncü komut, ' PolicyAssignment ' adlı ilke atamasını alır komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ca03e-130">Son komutu, PolicyAssignment adlı ilke atamasında parametre değerlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="ca03e-131">Örnek 4: ilke atama parametrelerini ilke parametre dosyasıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ca03e-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="ca03e-132">Yerel çalışma dizininde aşağıdaki içerikle _AllowedLocations.js_ adlı bir dosya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca03e-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="ca03e-133">Komut, yerel çalışma dizininden AllowedLocations.jsilke parametre dosyasını kullanarak ' PolicyAssignment ' adlı ilke atamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="ca03e-134">Örnek 5: enforcementMode 'ı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ca03e-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="ca03e-135">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="ca03e-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ca03e-136">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ca03e-137">İkinci komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="ca03e-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="ca03e-138">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ca03e-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ca03e-139">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki Ilke atamasında enforcementMode özelliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="ca03e-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca03e-140">PARAMETERS</span></span>

### <span data-ttu-id="ca03e-141">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ca03e-141">-ApiVersion</span></span>
<span data-ttu-id="ca03e-142">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ca03e-143">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="ca03e-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ca03e-144">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="ca03e-144">-AssignIdentity</span></span>
<span data-ttu-id="ca03e-145">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="ca03e-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="ca03e-146">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ca03e-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="ca03e-147">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="ca03e-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca03e-148">-DefaultProfile</span></span>
<span data-ttu-id="ca03e-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ca03e-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca03e-150">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ca03e-150">-Description</span></span>
<span data-ttu-id="ca03e-151">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="ca03e-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="ca03e-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ca03e-152">-DisplayName</span></span>
<span data-ttu-id="ca03e-153">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="ca03e-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="ca03e-154">-EnforcementMode</span></span>
<span data-ttu-id="ca03e-155">İlke ataması için zorlama modu.</span><span class="sxs-lookup"><span data-stu-id="ca03e-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="ca03e-156">Geçerli değerler varsayılan, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="ca03e-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="ca03e-157">-ID</span><span class="sxs-lookup"><span data-stu-id="ca03e-157">-Id</span></span>
<span data-ttu-id="ca03e-158">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca03e-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca03e-159">-InputObject</span></span>
<span data-ttu-id="ca03e-160">Başka bir cmdlet 'ten alınan, güncelleştirilecek ilke atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ca03e-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca03e-161">-Konum</span><span class="sxs-lookup"><span data-stu-id="ca03e-161">-Location</span></span>
<span data-ttu-id="ca03e-162">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="ca03e-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="ca03e-163">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="ca03e-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ca03e-164">-Metadata</span></span>
<span data-ttu-id="ca03e-165">İlke atamasının güncelleştirilmiş meta verileri.</span><span class="sxs-lookup"><span data-stu-id="ca03e-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="ca03e-166">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="ca03e-167">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca03e-167">-Name</span></span>
<span data-ttu-id="ca03e-168">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca03e-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="ca03e-169">-NotScope</span></span>
<span data-ttu-id="ca03e-170">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="ca03e-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="ca03e-171">-PolicyParameter</span></span>
<span data-ttu-id="ca03e-172">İlke atamasının yeni ilke parametreleri dosya yolu veya dizesi.</span><span class="sxs-lookup"><span data-stu-id="ca03e-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca03e-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca03e-173">-PolicyParameterObject</span></span>
<span data-ttu-id="ca03e-174">İlke atamasının yeni ilke parametreleri nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ca03e-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca03e-175">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ca03e-175">-Pre</span></span>
<span data-ttu-id="ca03e-176">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ca03e-177">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ca03e-177">-Scope</span></span>
<span data-ttu-id="ca03e-178">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca03e-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca03e-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca03e-179">CommonParameters</span></span>
<span data-ttu-id="ca03e-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca03e-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca03e-181">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca03e-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca03e-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca03e-182">INPUTS</span></span>

### <span data-ttu-id="ca03e-183">System. String</span><span class="sxs-lookup"><span data-stu-id="ca03e-183">System.String</span></span>

### <span data-ttu-id="ca03e-184">System. String []</span><span class="sxs-lookup"><span data-stu-id="ca03e-184">System.String[]</span></span>

## <span data-ttu-id="ca03e-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca03e-185">OUTPUTS</span></span>

### <span data-ttu-id="ca03e-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ca03e-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ca03e-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca03e-187">NOTES</span></span>

## <span data-ttu-id="ca03e-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca03e-188">RELATED LINKS</span></span>

[<span data-ttu-id="ca03e-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ca03e-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="ca03e-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ca03e-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="ca03e-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ca03e-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


