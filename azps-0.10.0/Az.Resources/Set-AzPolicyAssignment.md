---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 102d297f53fe51779f8831e4890c7d55bb59d2eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936323"
---
# <span data-ttu-id="6caed-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6caed-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="6caed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6caed-102">SYNOPSIS</span></span>
<span data-ttu-id="6caed-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6caed-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="6caed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6caed-104">SYNTAX</span></span>

### <span data-ttu-id="6caed-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6caed-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6caed-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="6caed-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6caed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6caed-107">DESCRIPTION</span></span>
<span data-ttu-id="6caed-108">**Set-AzPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6caed-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="6caed-109">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="6caed-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="6caed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6caed-110">EXAMPLES</span></span>

### <span data-ttu-id="6caed-111">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6caed-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="6caed-112">İlk komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="6caed-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="6caed-113">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6caed-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="6caed-114">İkinci komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="6caed-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6caed-115">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6caed-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="6caed-116">Son komutu, $ResourceGroup 'un **RESOURCEID** özelliğiyle tanımlanan kaynak grubundaki ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6caed-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="6caed-117">Örnek 2: ilke atamalarına yönetilen kimlik ekleme</span><span class="sxs-lookup"><span data-stu-id="6caed-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="6caed-118">İlk komut, Get-AzPolicyAssignment cmdlet 'ini kullanarak geçerli abonelikteki PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="6caed-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6caed-119">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6caed-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="6caed-120">Son komutu, ilke atamalarına yönetilen bir kimlik atar.</span><span class="sxs-lookup"><span data-stu-id="6caed-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="6caed-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6caed-121">PARAMETERS</span></span>

### <span data-ttu-id="6caed-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="6caed-122">-ApiVersion</span></span>
<span data-ttu-id="6caed-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6caed-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6caed-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="6caed-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6caed-125">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="6caed-125">-AssignIdentity</span></span>
<span data-ttu-id="6caed-126">Bu ilke ataması için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="6caed-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="6caed-127">' DeployIfNotExists ' ilkeleri için dağıtımlar yürütülürken kimlik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6caed-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="6caed-128">Bir kimlik atanırken konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6caed-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="6caed-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6caed-129">-DefaultProfile</span></span>
<span data-ttu-id="6caed-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6caed-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6caed-131">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6caed-131">-Description</span></span>
<span data-ttu-id="6caed-132">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="6caed-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="6caed-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6caed-133">-DisplayName</span></span>
<span data-ttu-id="6caed-134">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="6caed-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="6caed-135">-ID</span><span class="sxs-lookup"><span data-stu-id="6caed-135">-Id</span></span>
<span data-ttu-id="6caed-136">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6caed-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6caed-137">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6caed-137">-InformationAction</span></span>
<span data-ttu-id="6caed-138">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6caed-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="6caed-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6caed-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6caed-140">'A</span><span class="sxs-lookup"><span data-stu-id="6caed-140">Continue</span></span>
- <span data-ttu-id="6caed-141">Manıza</span><span class="sxs-lookup"><span data-stu-id="6caed-141">Ignore</span></span>
- <span data-ttu-id="6caed-142">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="6caed-142">Inquire</span></span>
- <span data-ttu-id="6caed-143">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="6caed-143">SilentlyContinue</span></span>
- <span data-ttu-id="6caed-144">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="6caed-144">Stop</span></span>
- <span data-ttu-id="6caed-145">Biliriz</span><span class="sxs-lookup"><span data-stu-id="6caed-145">Suspend</span></span>

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

### <span data-ttu-id="6caed-146">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="6caed-146">-InformationVariable</span></span>
<span data-ttu-id="6caed-147">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="6caed-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6caed-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="6caed-148">-Location</span></span>
<span data-ttu-id="6caed-149">İlke atamasının kaynak kimliğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="6caed-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="6caed-150">-Atamakimliği anahtarı kullanıldığında bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6caed-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="6caed-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6caed-151">-Metadata</span></span>
<span data-ttu-id="6caed-152">İlke atamasının güncelleştirilmiş meta verileri.</span><span class="sxs-lookup"><span data-stu-id="6caed-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="6caed-153">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="6caed-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="6caed-154">-Ad</span><span class="sxs-lookup"><span data-stu-id="6caed-154">-Name</span></span>
<span data-ttu-id="6caed-155">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6caed-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6caed-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="6caed-156">-NotScope</span></span>
<span data-ttu-id="6caed-157">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="6caed-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="6caed-158">-Pre-</span><span class="sxs-lookup"><span data-stu-id="6caed-158">-Pre</span></span>
<span data-ttu-id="6caed-159">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6caed-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6caed-160">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="6caed-160">-Scope</span></span>
<span data-ttu-id="6caed-161">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6caed-161">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="6caed-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="6caed-162">-Sku</span></span>
<span data-ttu-id="6caed-163">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="6caed-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="6caed-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6caed-164">CommonParameters</span></span>
<span data-ttu-id="6caed-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6caed-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6caed-166">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6caed-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6caed-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6caed-167">INPUTS</span></span>

## <span data-ttu-id="6caed-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6caed-168">OUTPUTS</span></span>

## <span data-ttu-id="6caed-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6caed-169">NOTES</span></span>

## <span data-ttu-id="6caed-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6caed-170">RELATED LINKS</span></span>

[<span data-ttu-id="6caed-171">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6caed-171">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="6caed-172">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6caed-172">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="6caed-173">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6caed-173">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


