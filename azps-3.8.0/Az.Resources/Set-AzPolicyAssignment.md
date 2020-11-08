---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: ab0617b4012ca623bf67471a9a5bcc3ccf54d905
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097214"
---
# <span data-ttu-id="1f565-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f565-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="1f565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f565-102">SYNOPSIS</span></span>
<span data-ttu-id="1f565-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1f565-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="1f565-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f565-104">SYNTAX</span></span>

### <span data-ttu-id="1f565-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f565-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f565-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f565-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f565-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f565-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f565-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="1f565-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f565-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f565-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f565-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f565-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f565-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f565-111">DESCRIPTION</span></span>
<span data-ttu-id="1f565-112">**Set-AzPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1f565-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="1f565-113">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="1f565-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="1f565-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f565-114">EXAMPLES</span></span>

### <span data-ttu-id="1f565-115">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1f565-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="1f565-116">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="1f565-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1f565-117">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f565-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1f565-118">İkinci komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="1f565-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="1f565-119">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f565-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1f565-120">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f565-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="1f565-121">Örnek 2: ilke atamalarına yönetilen kimlik ekleme</span><span class="sxs-lookup"><span data-stu-id="1f565-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="1f565-122">İlk komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak geçerli abonelikteki PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="1f565-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="1f565-123">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f565-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1f565-124">Son komutu, ilke atamalarına yönetilen bir kimlik atar.</span><span class="sxs-lookup"><span data-stu-id="1f565-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="1f565-125">Örnek 3: yeni ilke parametresi nesnesiyle ilke atama parametrelerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1f565-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="1f565-126">İlk ve ikinci komutlar adları "Fransa" veya "İngiltere" ile başlayan tüm Azure bölgelerini içeren bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f565-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="1f565-127">İkinci komut bu nesneyi $AllowedLocations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f565-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="1f565-128">Üçüncü komut, ' PolicyAssignment ' adlı ilke atamasını alır komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f565-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1f565-129">Son komutu, PolicyAssignment adlı ilke atamasında parametre değerlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f565-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="1f565-130">Örnek 4: ilke atama parametrelerini ilke parametre dosyasıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1f565-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="1f565-131">Yerel çalışma dizininde aşağıdaki içerikle _AllowedLocations.js_ adlı bir dosya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1f565-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="1f565-132">Komut, yerel çalışma dizininden AllowedLocations.jsilke parametre dosyasını kullanarak ' PolicyAssignment ' adlı ilke atamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f565-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="1f565-133">Örnek 5: enforcementMode 'ı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1f565-133">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="1f565-134">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="1f565-134">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1f565-135">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f565-135">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1f565-136">İkinci komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="1f565-136">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="1f565-137">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f565-137">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1f565-138">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki Ilke atamasında enforcementMode özelliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f565-138">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="1f565-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f565-139">PARAMETERS</span></span>

### <span data-ttu-id="1f565-140">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="1f565-140">-ApiVersion</span></span>
<span data-ttu-id="1f565-141">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f565-141">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1f565-142">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="1f565-142">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1f565-143">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="1f565-143">-AssignIdentity</span></span>
<span data-ttu-id="1f565-144">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="1f565-144">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="1f565-145">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1f565-145">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="1f565-146">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1f565-146">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="1f565-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f565-147">-DefaultProfile</span></span>
<span data-ttu-id="1f565-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1f565-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f565-149">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1f565-149">-Description</span></span>
<span data-ttu-id="1f565-150">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="1f565-150">The description for policy assignment</span></span>

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

### <span data-ttu-id="1f565-151">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f565-151">-DisplayName</span></span>
<span data-ttu-id="1f565-152">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f565-152">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="1f565-153">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="1f565-153">-EnforcementMode</span></span>
<span data-ttu-id="1f565-154">İlke ataması için zorlama modu.</span><span class="sxs-lookup"><span data-stu-id="1f565-154">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="1f565-155">Geçerli değerler varsayılan, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="1f565-155">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="1f565-156">-ID</span><span class="sxs-lookup"><span data-stu-id="1f565-156">-Id</span></span>
<span data-ttu-id="1f565-157">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f565-157">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1f565-158">-Konum</span><span class="sxs-lookup"><span data-stu-id="1f565-158">-Location</span></span>
<span data-ttu-id="1f565-159">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="1f565-159">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="1f565-160">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1f565-160">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="1f565-161">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1f565-161">-Metadata</span></span>
<span data-ttu-id="1f565-162">İlke atamasının güncelleştirilmiş meta verileri.</span><span class="sxs-lookup"><span data-stu-id="1f565-162">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="1f565-163">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="1f565-163">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="1f565-164">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f565-164">-Name</span></span>
<span data-ttu-id="1f565-165">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f565-165">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1f565-166">-NotScope</span><span class="sxs-lookup"><span data-stu-id="1f565-166">-NotScope</span></span>
<span data-ttu-id="1f565-167">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="1f565-167">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="1f565-168">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="1f565-168">-PolicyParameter</span></span>
<span data-ttu-id="1f565-169">İlke atamasının yeni ilke parametreleri dosya yolu veya dizesi.</span><span class="sxs-lookup"><span data-stu-id="1f565-169">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="1f565-170">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1f565-170">-PolicyParameterObject</span></span>
<span data-ttu-id="1f565-171">İlke atamasının yeni ilke parametreleri nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1f565-171">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="1f565-172">-Pre-</span><span class="sxs-lookup"><span data-stu-id="1f565-172">-Pre</span></span>
<span data-ttu-id="1f565-173">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f565-173">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1f565-174">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="1f565-174">-Scope</span></span>
<span data-ttu-id="1f565-175">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f565-175">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="1f565-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f565-176">CommonParameters</span></span>
<span data-ttu-id="1f565-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f565-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f565-178">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1f565-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f565-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f565-179">INPUTS</span></span>

### <span data-ttu-id="1f565-180">System. String</span><span class="sxs-lookup"><span data-stu-id="1f565-180">System.String</span></span>

### <span data-ttu-id="1f565-181">System. String []</span><span class="sxs-lookup"><span data-stu-id="1f565-181">System.String[]</span></span>

## <span data-ttu-id="1f565-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f565-182">OUTPUTS</span></span>

### <span data-ttu-id="1f565-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1f565-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1f565-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f565-184">NOTES</span></span>

## <span data-ttu-id="1f565-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f565-185">RELATED LINKS</span></span>

[<span data-ttu-id="1f565-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f565-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1f565-187">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f565-187">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="1f565-188">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1f565-188">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

