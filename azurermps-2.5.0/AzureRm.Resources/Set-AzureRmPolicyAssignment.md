---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: dc54d84886bc9c13fa6a4ecef4e41ef80fa6d4e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939243"
---
# <span data-ttu-id="777fe-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777fe-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="777fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="777fe-102">SYNOPSIS</span></span>
<span data-ttu-id="777fe-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="777fe-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="777fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="777fe-104">SYNTAX</span></span>

### <span data-ttu-id="777fe-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="777fe-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="777fe-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="777fe-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="777fe-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="777fe-107">DESCRIPTION</span></span>
<span data-ttu-id="777fe-108">**Set-AzureRmPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="777fe-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="777fe-109">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="777fe-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="777fe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="777fe-110">EXAMPLES</span></span>

### <span data-ttu-id="777fe-111">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="777fe-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="777fe-112">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="777fe-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="777fe-113">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="777fe-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="777fe-114">İkinci komut, Get-AzureRmPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="777fe-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="777fe-115">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="777fe-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="777fe-116">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="777fe-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="777fe-117">Örnek 2: ilke atamalarına yönetilen kimlik ekleme</span><span class="sxs-lookup"><span data-stu-id="777fe-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="777fe-118">İlk komut, Get-AzureRmPolicyAssignment cmdlet 'ini kullanarak geçerli abonelikteki PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="777fe-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="777fe-119">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="777fe-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="777fe-120">Son komutu, ilke atamalarına yönetilen bir kimlik atar.</span><span class="sxs-lookup"><span data-stu-id="777fe-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="777fe-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="777fe-121">PARAMETERS</span></span>

### <span data-ttu-id="777fe-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="777fe-122">-ApiVersion</span></span>
<span data-ttu-id="777fe-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="777fe-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="777fe-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="777fe-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="777fe-125">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="777fe-125">-AssignIdentity</span></span>
<span data-ttu-id="777fe-126">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="777fe-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="777fe-127">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="777fe-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="777fe-128">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="777fe-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="777fe-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="777fe-129">-DefaultProfile</span></span>
<span data-ttu-id="777fe-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="777fe-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="777fe-131">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="777fe-131">-Description</span></span>
<span data-ttu-id="777fe-132">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="777fe-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="777fe-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="777fe-133">-DisplayName</span></span>
<span data-ttu-id="777fe-134">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="777fe-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="777fe-135">-ID</span><span class="sxs-lookup"><span data-stu-id="777fe-135">-Id</span></span>
<span data-ttu-id="777fe-136">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="777fe-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="777fe-137">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="777fe-137">-InformationAction</span></span>
<span data-ttu-id="777fe-138">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="777fe-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="777fe-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="777fe-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="777fe-140">'A</span><span class="sxs-lookup"><span data-stu-id="777fe-140">Continue</span></span>
- <span data-ttu-id="777fe-141">Manıza</span><span class="sxs-lookup"><span data-stu-id="777fe-141">Ignore</span></span>
- <span data-ttu-id="777fe-142">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="777fe-142">Inquire</span></span>
- <span data-ttu-id="777fe-143">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="777fe-143">SilentlyContinue</span></span>
- <span data-ttu-id="777fe-144">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="777fe-144">Stop</span></span>
- <span data-ttu-id="777fe-145">Biliriz</span><span class="sxs-lookup"><span data-stu-id="777fe-145">Suspend</span></span>

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

### <span data-ttu-id="777fe-146">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="777fe-146">-InformationVariable</span></span>
<span data-ttu-id="777fe-147">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="777fe-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="777fe-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="777fe-148">-Location</span></span>
<span data-ttu-id="777fe-149">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="777fe-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="777fe-150">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="777fe-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="777fe-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="777fe-151">-Metadata</span></span>
<span data-ttu-id="777fe-152">İlke atamasının güncelleştirilmiş meta verileri.</span><span class="sxs-lookup"><span data-stu-id="777fe-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="777fe-153">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="777fe-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="777fe-154">-Ad</span><span class="sxs-lookup"><span data-stu-id="777fe-154">-Name</span></span>
<span data-ttu-id="777fe-155">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="777fe-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="777fe-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="777fe-156">-NotScope</span></span>
<span data-ttu-id="777fe-157">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="777fe-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="777fe-158">-Pre-</span><span class="sxs-lookup"><span data-stu-id="777fe-158">-Pre</span></span>
<span data-ttu-id="777fe-159">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="777fe-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="777fe-160">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="777fe-160">-Scope</span></span>
<span data-ttu-id="777fe-161">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="777fe-161">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="777fe-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="777fe-162">-Sku</span></span>
<span data-ttu-id="777fe-163">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="777fe-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="777fe-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777fe-164">CommonParameters</span></span>
<span data-ttu-id="777fe-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="777fe-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777fe-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="777fe-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777fe-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="777fe-167">INPUTS</span></span>

## <span data-ttu-id="777fe-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="777fe-168">OUTPUTS</span></span>

## <span data-ttu-id="777fe-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="777fe-169">NOTES</span></span>

## <span data-ttu-id="777fe-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="777fe-170">RELATED LINKS</span></span>

[<span data-ttu-id="777fe-171">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777fe-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="777fe-172">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777fe-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="777fe-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777fe-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


