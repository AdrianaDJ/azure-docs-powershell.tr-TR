---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 5d83266e341643adc45a2fc7af8eff1f9a5e0b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933306"
---
# <span data-ttu-id="2db92-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2db92-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="2db92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db92-102">SYNOPSIS</span></span>
<span data-ttu-id="2db92-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2db92-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="2db92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2db92-104">SYNTAX</span></span>

### <span data-ttu-id="2db92-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2db92-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db92-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db92-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db92-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db92-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db92-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="2db92-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db92-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db92-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db92-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db92-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db92-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="2db92-111">DESCRIPTION</span></span>
<span data-ttu-id="2db92-112">**Set-AzPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2db92-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="2db92-113">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="2db92-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="2db92-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2db92-114">EXAMPLES</span></span>

### <span data-ttu-id="2db92-115">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2db92-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="2db92-116">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="2db92-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2db92-117">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2db92-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2db92-118">İkinci komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="2db92-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2db92-119">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2db92-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2db92-120">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2db92-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="2db92-121">Örnek 2: ilke atamalarına yönetilen kimlik ekleme</span><span class="sxs-lookup"><span data-stu-id="2db92-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="2db92-122">İlk komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak geçerli abonelikteki PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="2db92-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2db92-123">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2db92-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2db92-124">Son komutu, ilke atamalarına yönetilen bir kimlik atar.</span><span class="sxs-lookup"><span data-stu-id="2db92-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="2db92-125">Örnek 3: yeni ilke parametresi nesnesiyle ilke atama parametrelerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2db92-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="2db92-126">İlk ve ikinci komutlar adları "Fransa" veya "İngiltere" ile başlayan tüm Azure bölgelerini içeren bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2db92-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="2db92-127">İkinci komut bu nesneyi $AllowedLocations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2db92-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="2db92-128">Üçüncü komut, ' PolicyAssignment ' adlı ilke atamasını alır komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2db92-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2db92-129">Son komutu, PolicyAssignment adlı ilke atamasında parametre değerlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2db92-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="2db92-130">Örnek 4: ilke atama parametrelerini ilke parametre dosyasıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2db92-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="2db92-131">Yerel çalışma dizininde aşağıdaki içerikle _AllowedLocations.js_ adlı bir dosya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2db92-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="2db92-132">Komut, yerel çalışma dizininden AllowedLocations.jsilke parametre dosyasını kullanarak ' PolicyAssignment ' adlı ilke atamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2db92-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

## <span data-ttu-id="2db92-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2db92-133">PARAMETERS</span></span>

### <span data-ttu-id="2db92-134">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="2db92-134">-ApiVersion</span></span>
<span data-ttu-id="2db92-135">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db92-135">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2db92-136">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="2db92-136">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2db92-137">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="2db92-137">-AssignIdentity</span></span>
<span data-ttu-id="2db92-138">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="2db92-138">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="2db92-139">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2db92-139">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="2db92-140">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2db92-140">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="2db92-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db92-141">-DefaultProfile</span></span>
<span data-ttu-id="2db92-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2db92-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2db92-143">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="2db92-143">-Description</span></span>
<span data-ttu-id="2db92-144">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="2db92-144">The description for policy assignment</span></span>

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

### <span data-ttu-id="2db92-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2db92-145">-DisplayName</span></span>
<span data-ttu-id="2db92-146">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db92-146">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="2db92-147">-ID</span><span class="sxs-lookup"><span data-stu-id="2db92-147">-Id</span></span>
<span data-ttu-id="2db92-148">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db92-148">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2db92-149">-Konum</span><span class="sxs-lookup"><span data-stu-id="2db92-149">-Location</span></span>
<span data-ttu-id="2db92-150">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="2db92-150">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="2db92-151">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2db92-151">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="2db92-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2db92-152">-Metadata</span></span>
<span data-ttu-id="2db92-153">İlke atamasının güncelleştirilmiş meta verileri.</span><span class="sxs-lookup"><span data-stu-id="2db92-153">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="2db92-154">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="2db92-154">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="2db92-155">-Ad</span><span class="sxs-lookup"><span data-stu-id="2db92-155">-Name</span></span>
<span data-ttu-id="2db92-156">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db92-156">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2db92-157">-NotScope</span><span class="sxs-lookup"><span data-stu-id="2db92-157">-NotScope</span></span>
<span data-ttu-id="2db92-158">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="2db92-158">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="2db92-159">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="2db92-159">-PolicyParameter</span></span>
<span data-ttu-id="2db92-160">İlke atamasının yeni ilke parametreleri dosya yolu veya dizesi.</span><span class="sxs-lookup"><span data-stu-id="2db92-160">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="2db92-161">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="2db92-161">-PolicyParameterObject</span></span>
<span data-ttu-id="2db92-162">İlke atamasının yeni ilke parametreleri nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2db92-162">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="2db92-163">-Pre-</span><span class="sxs-lookup"><span data-stu-id="2db92-163">-Pre</span></span>
<span data-ttu-id="2db92-164">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2db92-164">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2db92-165">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="2db92-165">-Scope</span></span>
<span data-ttu-id="2db92-166">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db92-166">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="2db92-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db92-167">CommonParameters</span></span>
<span data-ttu-id="2db92-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2db92-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db92-169">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2db92-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db92-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2db92-170">INPUTS</span></span>

### <span data-ttu-id="2db92-171">System. String</span><span class="sxs-lookup"><span data-stu-id="2db92-171">System.String</span></span>

### <span data-ttu-id="2db92-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="2db92-172">System.String[]</span></span>

## <span data-ttu-id="2db92-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2db92-173">OUTPUTS</span></span>

### <span data-ttu-id="2db92-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2db92-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2db92-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2db92-175">NOTES</span></span>

## <span data-ttu-id="2db92-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2db92-176">RELATED LINKS</span></span>

[<span data-ttu-id="2db92-177">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2db92-177">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="2db92-178">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2db92-178">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="2db92-179">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2db92-179">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


