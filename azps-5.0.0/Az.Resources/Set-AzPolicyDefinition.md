---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278019"
---
# <span data-ttu-id="e5a3b-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5a3b-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="e5a3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a3b-103">İlke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="e5a3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5a3b-104">SYNTAX</span></span>

### <span data-ttu-id="e5a3b-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5a3b-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a3b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a3b-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a3b-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e5a3b-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a3b-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="e5a3b-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a3b-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="e5a3b-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5a3b-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5a3b-110">DESCRIPTION</span></span>
<span data-ttu-id="e5a3b-111">**Set-AzPolicyDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="e5a3b-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5a3b-112">EXAMPLES</span></span>

### <span data-ttu-id="e5a3b-113">Örnek 1: ilke tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e5a3b-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="e5a3b-114">İlk komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="e5a3b-115">Komut bu nesneyi $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="e5a3b-116">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliği tarafından tanımlanan ilke tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="e5a3b-117">Örnek 2: ilke tanımının modunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e5a3b-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="e5a3b-118">Bu komut, VMPolicyDefinition adındaki ilke tanımını, Mode özelliğini ' All ' olarak ayarlamak için Set-AzPolicyDefinition cmdlet 'ini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="e5a3b-119">Örnek 3: ilke tanımının meta verilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e5a3b-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="e5a3b-120">Bu komut, VMPolicyDefinition adındaki ilke tanımının, kategorisini "sanal makine" olduğunu belirtecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="e5a3b-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5a3b-121">PARAMETERS</span></span>

### <span data-ttu-id="e5a3b-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e5a3b-122">-ApiVersion</span></span>
<span data-ttu-id="e5a3b-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5a3b-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e5a3b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a3b-125">-DefaultProfile</span></span>
<span data-ttu-id="e5a3b-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e5a3b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5a3b-127">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e5a3b-127">-Description</span></span>
<span data-ttu-id="e5a3b-128">İlke tanımı için yeni bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="e5a3b-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5a3b-129">-DisplayName</span></span>
<span data-ttu-id="e5a3b-130">İlke tanımı için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="e5a3b-131">-ID</span><span class="sxs-lookup"><span data-stu-id="e5a3b-131">-Id</span></span>
<span data-ttu-id="e5a3b-132">Bu cmdlet 'in değiştirdiği ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e5a3b-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5a3b-133">-InputObject</span></span>
<span data-ttu-id="e5a3b-134">Başka bir cmdlet 'ten çıktı olan güncelleştirilecek ilke tanımı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a3b-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a3b-135">-ManagementGroupName</span></span>
<span data-ttu-id="e5a3b-136">Güncelleştirilecek ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-136">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a3b-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e5a3b-137">-Metadata</span></span>
<span data-ttu-id="e5a3b-138">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-138">The metadata for policy definition.</span></span> <span data-ttu-id="e5a3b-139">Bu, meta veri veya meta veri içeren bir dosya adının yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="e5a3b-140">-Mod</span><span class="sxs-lookup"><span data-stu-id="e5a3b-140">-Mode</span></span>
<span data-ttu-id="e5a3b-141">Yeni ilke tanımının modu.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="e5a3b-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5a3b-142">-Name</span></span>
<span data-ttu-id="e5a3b-143">Bu cmdlet 'in değiştirdiği ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a3b-144">-Parametre</span><span class="sxs-lookup"><span data-stu-id="e5a3b-144">-Parameter</span></span>
<span data-ttu-id="e5a3b-145">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="e5a3b-146">Bu, parametre bildirimini içeren bir dosya adı veya URI veya dize olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="e5a3b-147">-İlke</span><span class="sxs-lookup"><span data-stu-id="e5a3b-147">-Policy</span></span>
<span data-ttu-id="e5a3b-148">İlke tanımı için yeni ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="e5a3b-149">Bir. json dosyasının veya JavaScript nesne gösterimi (JSON) biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="e5a3b-150">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e5a3b-150">-Pre</span></span>
<span data-ttu-id="e5a3b-151">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5a3b-152">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e5a3b-152">-SubscriptionId</span></span>
<span data-ttu-id="e5a3b-153">Güncelleştirilecek ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-153">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a3b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a3b-154">CommonParameters</span></span>
<span data-ttu-id="e5a3b-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a3b-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5a3b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a3b-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5a3b-157">INPUTS</span></span>

### <span data-ttu-id="e5a3b-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e5a3b-158">System.String</span></span>

### <span data-ttu-id="e5a3b-159">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5a3b-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e5a3b-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5a3b-160">OUTPUTS</span></span>

### <span data-ttu-id="e5a3b-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e5a3b-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5a3b-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5a3b-162">NOTES</span></span>

## <span data-ttu-id="e5a3b-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5a3b-163">RELATED LINKS</span></span>

[<span data-ttu-id="e5a3b-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5a3b-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="e5a3b-165">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="e5a3b-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="e5a3b-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5a3b-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


