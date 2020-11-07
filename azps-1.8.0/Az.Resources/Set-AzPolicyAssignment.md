---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759316"
---
# <span data-ttu-id="8fe92-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fe92-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="8fe92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe92-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe92-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="8fe92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fe92-104">SYNTAX</span></span>

### <span data-ttu-id="8fe92-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8fe92-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe92-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="8fe92-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe92-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fe92-107">DESCRIPTION</span></span>
<span data-ttu-id="8fe92-108">**Set-AzPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="8fe92-109">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="8fe92-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="8fe92-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fe92-110">EXAMPLES</span></span>

### <span data-ttu-id="8fe92-111">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8fe92-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="8fe92-112">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="8fe92-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8fe92-113">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8fe92-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8fe92-114">İkinci komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="8fe92-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="8fe92-115">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8fe92-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8fe92-116">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="8fe92-117">Örnek 2: ilke atamalarına yönetilen kimlik ekleme</span><span class="sxs-lookup"><span data-stu-id="8fe92-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="8fe92-118">İlk komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak geçerli abonelikteki PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="8fe92-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="8fe92-119">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8fe92-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8fe92-120">Son komutu, ilke atamalarına yönetilen bir kimlik atar.</span><span class="sxs-lookup"><span data-stu-id="8fe92-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="8fe92-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fe92-121">PARAMETERS</span></span>

### <span data-ttu-id="8fe92-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8fe92-122">-ApiVersion</span></span>
<span data-ttu-id="8fe92-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8fe92-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="8fe92-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8fe92-125">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="8fe92-125">-AssignIdentity</span></span>
<span data-ttu-id="8fe92-126">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="8fe92-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="8fe92-127">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8fe92-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="8fe92-128">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="8fe92-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe92-129">-DefaultProfile</span></span>
<span data-ttu-id="8fe92-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8fe92-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fe92-131">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8fe92-131">-Description</span></span>
<span data-ttu-id="8fe92-132">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="8fe92-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="8fe92-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8fe92-133">-DisplayName</span></span>
<span data-ttu-id="8fe92-134">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="8fe92-135">-ID</span><span class="sxs-lookup"><span data-stu-id="8fe92-135">-Id</span></span>
<span data-ttu-id="8fe92-136">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8fe92-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="8fe92-137">-Location</span></span>
<span data-ttu-id="8fe92-138">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="8fe92-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="8fe92-139">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="8fe92-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8fe92-140">-Metadata</span></span>
<span data-ttu-id="8fe92-141">İlke atamasının güncelleştirilmiş meta verileri.</span><span class="sxs-lookup"><span data-stu-id="8fe92-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="8fe92-142">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="8fe92-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="8fe92-143">-Name</span></span>
<span data-ttu-id="8fe92-144">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe92-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="8fe92-145">-NotScope</span></span>
<span data-ttu-id="8fe92-146">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-146">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="8fe92-147">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8fe92-147">-Pre</span></span>
<span data-ttu-id="8fe92-148">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8fe92-149">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="8fe92-149">-Scope</span></span>
<span data-ttu-id="8fe92-150">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-150">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe92-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe92-151">CommonParameters</span></span>
<span data-ttu-id="8fe92-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fe92-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe92-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe92-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe92-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fe92-154">INPUTS</span></span>

### <span data-ttu-id="8fe92-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8fe92-155">System.String</span></span>

### <span data-ttu-id="8fe92-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="8fe92-156">System.String[]</span></span>

## <span data-ttu-id="8fe92-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fe92-157">OUTPUTS</span></span>

### <span data-ttu-id="8fe92-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8fe92-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8fe92-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fe92-159">NOTES</span></span>

## <span data-ttu-id="8fe92-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fe92-160">RELATED LINKS</span></span>

[<span data-ttu-id="8fe92-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fe92-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="8fe92-162">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fe92-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="8fe92-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fe92-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


