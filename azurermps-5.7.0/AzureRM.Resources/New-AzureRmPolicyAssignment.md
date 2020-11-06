---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592406"
---
# <span data-ttu-id="ed149-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ed149-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="ed149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed149-102">SYNOPSIS</span></span>
<span data-ttu-id="ed149-103">İlke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed149-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed149-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed149-104">SYNTAX</span></span>

### <span data-ttu-id="ed149-105">CreateWithoutParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed149-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ed149-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="ed149-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ed149-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="ed149-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ed149-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="ed149-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ed149-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="ed149-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ed149-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed149-110">DESCRIPTION</span></span>
<span data-ttu-id="ed149-111">**New-AzureRmPolicyAssignment** cmdlet 'i bir ilke ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed149-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="ed149-112">Bir ilke ve kapsam belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed149-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="ed149-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed149-113">EXAMPLES</span></span>

### <span data-ttu-id="ed149-114">Örnek 1: Kaynak Grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="ed149-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="ed149-115">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="ed149-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ed149-116">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed149-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ed149-117">İkinci komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak VirtualMachinePolicy adındaki ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="ed149-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ed149-118">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed149-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="ed149-119">Son komutu, ilkeyi bir kaynak grubu düzeyinde $Policy atar.</span><span class="sxs-lookup"><span data-stu-id="ed149-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="ed149-120">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ed149-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="ed149-121">Örnek 2: ilke parametresi nesnesiyle kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="ed149-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="ed149-122">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="ed149-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ed149-123">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed149-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ed149-124">İkinci komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="ed149-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ed149-125">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed149-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="ed149-126">Üçüncü ve dördüncü komutlar, ad içinde "Doğu" ile tüm Azure bölgelerini içeren bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed149-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="ed149-127">Komutlar bu nesneyi $AllowedLocations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed149-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="ed149-128">Son komutu, $AllowedLocations ilke parametre nesnesini kullanarak kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="ed149-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="ed149-129">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ed149-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="ed149-130">Örnek 3: ilke parametresi dosyası olan kaynak grup düzeyindeki Ilke ataması</span><span class="sxs-lookup"><span data-stu-id="ed149-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="ed149-131">Yerel çalışma dizininde aşağıdaki içerikle _AllowedLocations.js_ adlı bir dosya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ed149-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="ed149-132">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="ed149-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ed149-133">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed149-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ed149-134">İkinci komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak izin verilen konumlar için yerleşik ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="ed149-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ed149-135">Komut bu nesneyi $Policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed149-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="ed149-136">Son komutu, yerel çalışma dizininde AllowedLocations.jsilke parametre dosyasını kullanarak bir kaynak grubunun düzeyindeki $Policy ilke atar.</span><span class="sxs-lookup"><span data-stu-id="ed149-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="ed149-137">$ResourceGroup **RESOURCEID** özelliği kaynak grubunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ed149-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="ed149-138">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed149-138">PARAMETERS</span></span>

### <span data-ttu-id="ed149-139">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ed149-139">-ApiVersion</span></span>
<span data-ttu-id="ed149-140">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed149-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ed149-141">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="ed149-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed149-142">-DefaultProfile</span></span>
<span data-ttu-id="ed149-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ed149-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-144">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ed149-144">-Description</span></span>
<span data-ttu-id="ed149-145">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="ed149-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed149-146">-DisplayName</span></span>
<span data-ttu-id="ed149-147">İlke ataması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed149-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-148">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ed149-148">-InformationAction</span></span>
<span data-ttu-id="ed149-149">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed149-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ed149-150">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ed149-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed149-151">'A</span><span class="sxs-lookup"><span data-stu-id="ed149-151">Continue</span></span>
- <span data-ttu-id="ed149-152">Manıza</span><span class="sxs-lookup"><span data-stu-id="ed149-152">Ignore</span></span>
- <span data-ttu-id="ed149-153">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ed149-153">Inquire</span></span>
- <span data-ttu-id="ed149-154">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ed149-154">SilentlyContinue</span></span>
- <span data-ttu-id="ed149-155">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ed149-155">Stop</span></span>
- <span data-ttu-id="ed149-156">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ed149-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-157">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ed149-157">-InformationVariable</span></span>
<span data-ttu-id="ed149-158">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed149-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed149-159">-Name</span></span>
<span data-ttu-id="ed149-160">İlke ataması için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed149-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="ed149-161">-NotScope</span></span>
<span data-ttu-id="ed149-162">İlke ataması için olmayan kapsamlar.</span><span class="sxs-lookup"><span data-stu-id="ed149-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ed149-163">-PolicyDefinition</span></span>
<span data-ttu-id="ed149-164">İlke kuralını içeren bir **Psobject** nesnesi olarak bir ilke belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed149-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="ed149-165">-PolicyParameter</span></span>
<span data-ttu-id="ed149-166">İlke parametresi dosya yolu veya ilke parametresi dizesi.</span><span class="sxs-lookup"><span data-stu-id="ed149-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="ed149-167">-PolicyParameterObject</span></span>
<span data-ttu-id="ed149-168">İlke parametresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ed149-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ed149-169">-PolicySetDefinition</span></span>
<span data-ttu-id="ed149-170">İlke kümesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ed149-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-171">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ed149-171">-Pre</span></span>
<span data-ttu-id="ed149-172">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed149-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-173">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ed149-173">-Scope</span></span>
<span data-ttu-id="ed149-174">İlkenin atanacağı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed149-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="ed149-175">Örneğin, kaynak grubuna ilke atamak için aşağıdakileri belirtin:</span><span class="sxs-lookup"><span data-stu-id="ed149-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="ed149-176">`/subscriptions/`abonelik KIMLIĞI `/resourcegroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ed149-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="ed149-177">-Sku</span></span>
<span data-ttu-id="ed149-178">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="ed149-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="ed149-179">Ücretsiz SKU için Varsayılanlar: ad = a0, katman = fre</span><span class="sxs-lookup"><span data-stu-id="ed149-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed149-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed149-180">CommonParameters</span></span>
<span data-ttu-id="ed149-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed149-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed149-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed149-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed149-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed149-183">INPUTS</span></span>

### <span data-ttu-id="ed149-184">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ed149-184">None</span></span>
<span data-ttu-id="ed149-185">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ed149-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed149-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed149-186">OUTPUTS</span></span>

### <span data-ttu-id="ed149-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ed149-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ed149-188">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed149-188">NOTES</span></span>

## <span data-ttu-id="ed149-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed149-189">RELATED LINKS</span></span>

[<span data-ttu-id="ed149-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ed149-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="ed149-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ed149-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ed149-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ed149-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ed149-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ed149-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


