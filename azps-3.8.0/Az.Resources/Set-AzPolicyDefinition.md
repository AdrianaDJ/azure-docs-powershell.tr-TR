---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 9f6f23babc1dfaf947a7eb8cea88011ff184cce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097215"
---
# <span data-ttu-id="c5573-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c5573-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="c5573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5573-102">SYNOPSIS</span></span>
<span data-ttu-id="c5573-103">İlke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c5573-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="c5573-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5573-104">SYNTAX</span></span>

### <span data-ttu-id="c5573-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5573-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5573-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5573-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5573-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c5573-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5573-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="c5573-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5573-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5573-109">DESCRIPTION</span></span>
<span data-ttu-id="c5573-110">**Set-AzPolicyDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c5573-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="c5573-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5573-111">EXAMPLES</span></span>

### <span data-ttu-id="c5573-112">Örnek 1: ilke tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c5573-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="c5573-113">İlk komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="c5573-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c5573-114">Komut bu nesneyi $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c5573-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="c5573-115">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliği tarafından tanımlanan ilke tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="c5573-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="c5573-116">Örnek 2: ilke tanımının modunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c5573-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="c5573-117">Bu komut, VMPolicyDefinition adındaki ilke tanımını, Mode özelliğini ' All ' olarak ayarlamak için Set-AzPolicyDefinition cmdlet 'ini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c5573-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="c5573-118">Örnek 3: ilke tanımının meta verilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c5573-118">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="c5573-119">Bu komut, VMPolicyDefinition adındaki ilke tanımının, kategorisini "sanal makine" olduğunu belirtecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c5573-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="c5573-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5573-120">PARAMETERS</span></span>

### <span data-ttu-id="c5573-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c5573-121">-ApiVersion</span></span>
<span data-ttu-id="c5573-122">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5573-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c5573-123">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c5573-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c5573-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5573-124">-DefaultProfile</span></span>
<span data-ttu-id="c5573-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5573-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5573-126">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c5573-126">-Description</span></span>
<span data-ttu-id="c5573-127">İlke tanımı için yeni bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5573-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="c5573-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5573-128">-DisplayName</span></span>
<span data-ttu-id="c5573-129">İlke tanımı için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5573-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="c5573-130">-ID</span><span class="sxs-lookup"><span data-stu-id="c5573-130">-Id</span></span>
<span data-ttu-id="c5573-131">Bu cmdlet 'in değiştirdiği ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5573-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c5573-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c5573-132">-ManagementGroupName</span></span>
<span data-ttu-id="c5573-133">Güncelleştirilecek ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c5573-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="c5573-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c5573-134">-Metadata</span></span>
<span data-ttu-id="c5573-135">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="c5573-135">The metadata for policy definition.</span></span> <span data-ttu-id="c5573-136">Bu, meta veri veya meta veri içeren bir dosya adının yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="c5573-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="c5573-137">-Mod</span><span class="sxs-lookup"><span data-stu-id="c5573-137">-Mode</span></span>
<span data-ttu-id="c5573-138">Yeni ilke tanımının modu.</span><span class="sxs-lookup"><span data-stu-id="c5573-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="c5573-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5573-139">-Name</span></span>
<span data-ttu-id="c5573-140">Bu cmdlet 'in değiştirdiği ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5573-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c5573-141">-Parametre</span><span class="sxs-lookup"><span data-stu-id="c5573-141">-Parameter</span></span>
<span data-ttu-id="c5573-142">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="c5573-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="c5573-143">Bu, parametre bildirimini içeren bir dosya adı veya URI veya dize olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="c5573-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="c5573-144">-İlke</span><span class="sxs-lookup"><span data-stu-id="c5573-144">-Policy</span></span>
<span data-ttu-id="c5573-145">İlke tanımı için yeni ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5573-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="c5573-146">Bir. json dosyasının veya JavaScript nesne gösterimi (JSON) biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c5573-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="c5573-147">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c5573-147">-Pre</span></span>
<span data-ttu-id="c5573-148">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5573-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c5573-149">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c5573-149">-SubscriptionId</span></span>
<span data-ttu-id="c5573-150">Güncelleştirilecek ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c5573-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="c5573-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5573-151">CommonParameters</span></span>
<span data-ttu-id="c5573-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5573-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5573-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c5573-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5573-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5573-154">INPUTS</span></span>

### <span data-ttu-id="c5573-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c5573-155">System.String</span></span>

### <span data-ttu-id="c5573-156">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="c5573-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c5573-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5573-157">OUTPUTS</span></span>

### <span data-ttu-id="c5573-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c5573-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c5573-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5573-159">NOTES</span></span>

## <span data-ttu-id="c5573-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5573-160">RELATED LINKS</span></span>

[<span data-ttu-id="c5573-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c5573-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c5573-162">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="c5573-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="c5573-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c5573-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


