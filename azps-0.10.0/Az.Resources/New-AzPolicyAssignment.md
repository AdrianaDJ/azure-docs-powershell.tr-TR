---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b8a7bd3d0c9f73b551cf6eefcb2564918fde1fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936395"
---
# <span data-ttu-id="a45b1-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a45b1-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="a45b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a45b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a45b1-103">İlke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a45b1-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="a45b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a45b1-104">SYNTAX</span></span>

### <span data-ttu-id="a45b1-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a45b1-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a45b1-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a45b1-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a45b1-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a45b1-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a45b1-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a45b1-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a45b1-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a45b1-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a45b1-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a45b1-110">DESCRIPTION</span></span>
<span data-ttu-id="a45b1-111">**New-AzPolicyAssignment** cmdlet 'i bir ilke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a45b1-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="a45b1-112">Bir ilke ve kapsam belirtin.</span><span class="sxs-lookup"><span data-stu-id="a45b1-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="a45b1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a45b1-113">EXAMPLES</span></span>

### <span data-ttu-id="a45b1-114">Örnek 1: Kaynak Grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a45b1-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="a45b1-115">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a45b1-116">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a45b1-117">Son komut, $ResourceGroup **RESOURCEID** özelliğiyle tanımlanan kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="a45b1-118">Örnek 2: ilke parametresi nesnesiyle kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a45b1-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="a45b1-119">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="a45b1-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a45b1-120">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a45b1-121">İkinci komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="a45b1-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a45b1-122">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="a45b1-123">Üçüncü ve dördüncü komutlar, ad içinde "Doğu" ile tüm Azure bölgelerini içeren bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a45b1-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="a45b1-124">Komutlar bu nesneyi $AllowedLocations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="a45b1-125">Son komutu, $AllowedLocations ilke parametre nesnesini kullanarak kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="a45b1-126">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="a45b1-127">Örnek 3: ilke parametresi dosyası olan kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a45b1-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="a45b1-128">Yerel çalışma dizininde aşağıdaki içerikle _AllowedLocations.js_ adlı bir dosya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a45b1-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="a45b1-129">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a45b1-130">İkinci komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a45b1-131">Son komut, ilkeyi, yerel çalışma dizininden AllowedLocations.jsilke parametre dosyasını kullanarak $ResourceGroup **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki $Policy atar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="a45b1-132">Örnek 4: yönetilen kimlikte Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="a45b1-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="a45b1-133">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adında bir kaynak grubu alır ve $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a45b1-134">İkinci komut VirtualMachineGet-AzPolicyDefinition Policy adındaki ilke tanımını alır ve $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="a45b1-135">Son komut $Policy ilkeyi kaynak grubuna atar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="a45b1-136">Yönetilen kimlik otomatik olarak oluşturulur ve ilke atamalarına atanır.</span><span class="sxs-lookup"><span data-stu-id="a45b1-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="a45b1-137">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a45b1-137">PARAMETERS</span></span>

### <span data-ttu-id="a45b1-138">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a45b1-138">-ApiVersion</span></span>
<span data-ttu-id="a45b1-139">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a45b1-140">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="a45b1-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a45b1-141">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="a45b1-141">-AssignIdentity</span></span>
<span data-ttu-id="a45b1-142">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="a45b1-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="a45b1-143">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a45b1-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="a45b1-144">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="a45b1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45b1-145">-DefaultProfile</span></span>
<span data-ttu-id="a45b1-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a45b1-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a45b1-147">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a45b1-147">-Description</span></span>
<span data-ttu-id="a45b1-148">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="a45b1-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="a45b1-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a45b1-149">-DisplayName</span></span>
<span data-ttu-id="a45b1-150">İlke ataması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="a45b1-151">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a45b1-151">-InformationAction</span></span>
<span data-ttu-id="a45b1-152">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a45b1-153">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a45b1-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a45b1-154">'A</span><span class="sxs-lookup"><span data-stu-id="a45b1-154">Continue</span></span>
- <span data-ttu-id="a45b1-155">Manıza</span><span class="sxs-lookup"><span data-stu-id="a45b1-155">Ignore</span></span>
- <span data-ttu-id="a45b1-156">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="a45b1-156">Inquire</span></span>
- <span data-ttu-id="a45b1-157">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="a45b1-157">SilentlyContinue</span></span>
- <span data-ttu-id="a45b1-158">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="a45b1-158">Stop</span></span>
- <span data-ttu-id="a45b1-159">Biliriz</span><span class="sxs-lookup"><span data-stu-id="a45b1-159">Suspend</span></span>

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

### <span data-ttu-id="a45b1-160">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="a45b1-160">-InformationVariable</span></span>
<span data-ttu-id="a45b1-161">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a45b1-162">-Konum</span><span class="sxs-lookup"><span data-stu-id="a45b1-162">-Location</span></span>
<span data-ttu-id="a45b1-163">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="a45b1-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="a45b1-164">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="a45b1-165">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a45b1-165">-Metadata</span></span>
<span data-ttu-id="a45b1-166">Yeni ilke atamasının meta verileri.</span><span class="sxs-lookup"><span data-stu-id="a45b1-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="a45b1-167">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="a45b1-168">-Ad</span><span class="sxs-lookup"><span data-stu-id="a45b1-168">-Name</span></span>
<span data-ttu-id="a45b1-169">İlke ataması için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="a45b1-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="a45b1-170">-NotScope</span></span>
<span data-ttu-id="a45b1-171">İlke ataması için olmayan kapsamlar.</span><span class="sxs-lookup"><span data-stu-id="a45b1-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="a45b1-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a45b1-172">-PolicyDefinition</span></span>
<span data-ttu-id="a45b1-173">İlke kuralını içeren **Pspolicydefinition** nesnesi olarak bir ilke belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="a45b1-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="a45b1-174">-PolicyParameter</span></span>
<span data-ttu-id="a45b1-175">İlke parametresi dosya yolu veya ilke parametresi dizesi.</span><span class="sxs-lookup"><span data-stu-id="a45b1-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="a45b1-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="a45b1-176">-PolicyParameterObject</span></span>
<span data-ttu-id="a45b1-177">İlke parametresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a45b1-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="a45b1-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a45b1-178">-PolicySetDefinition</span></span>
<span data-ttu-id="a45b1-179">İlke kümesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a45b1-179">The policy set definition object.</span></span>

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

### <span data-ttu-id="a45b1-180">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a45b1-180">-Pre</span></span>
<span data-ttu-id="a45b1-181">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a45b1-182">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a45b1-182">-Scope</span></span>
<span data-ttu-id="a45b1-183">İlkenin atanacağı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45b1-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="a45b1-184">Örneğin, kaynak grubuna ilke atamak için aşağıdakileri belirtin: `/subscriptions/` ABONELIK kimliği `/resourcegroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a45b1-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="a45b1-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="a45b1-185">-Sku</span></span>
<span data-ttu-id="a45b1-186">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="a45b1-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="a45b1-187">Varsayılan değer: `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="a45b1-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="a45b1-188">Standart SKU 'yu kullanmak için değerleri kullanın: `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="a45b1-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

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

### <span data-ttu-id="a45b1-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45b1-189">CommonParameters</span></span>
<span data-ttu-id="a45b1-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a45b1-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45b1-191">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a45b1-191">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45b1-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a45b1-192">INPUTS</span></span>

## <span data-ttu-id="a45b1-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a45b1-193">OUTPUTS</span></span>

## <span data-ttu-id="a45b1-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a45b1-194">NOTES</span></span>

## <span data-ttu-id="a45b1-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a45b1-195">RELATED LINKS</span></span>

[<span data-ttu-id="a45b1-196">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a45b1-196">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a45b1-197">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a45b1-197">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="a45b1-198">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a45b1-198">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="a45b1-199">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a45b1-199">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)

