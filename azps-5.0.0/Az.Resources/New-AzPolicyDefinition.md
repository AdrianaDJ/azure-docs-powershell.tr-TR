---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 51c5608c8212b519e6ca979e470c2ab1a5d96e6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322125"
---
# <span data-ttu-id="989dc-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="989dc-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="989dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="989dc-102">SYNOPSIS</span></span>
<span data-ttu-id="989dc-103">İlke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="989dc-103">Creates a policy definition.</span></span>

## <span data-ttu-id="989dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="989dc-104">SYNTAX</span></span>

### <span data-ttu-id="989dc-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="989dc-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="989dc-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="989dc-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="989dc-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="989dc-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="989dc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="989dc-108">DESCRIPTION</span></span>
<span data-ttu-id="989dc-109">**Yeni-Azilketanımı** cmdlet 'ı JavaScript nesne GÖSTERIMI (JSON) biçiminde ilke kuralı içeren bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="989dc-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="989dc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="989dc-110">EXAMPLES</span></span>

### <span data-ttu-id="989dc-111">Örnek 1: ilke dosyası kullanarak ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="989dc-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="989dc-112">Bu komut, C:\LocationPolicy.json alanında belirtilen ilke kuralını içeren LocationDefinition adlı bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="989dc-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="989dc-113">LocationPolicy.jsdosyanın içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="989dc-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="989dc-114">Örnek 2: satır içi parametreler kullanarak parametreli bir ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="989dc-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="989dc-115">Bu komut, C:\LocationPolicy.json alanında belirtilen ilke kuralını içeren LocationDefinition adlı bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="989dc-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="989dc-116">İlke kuralının parametre tanımı satır içi olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="989dc-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="989dc-117">Örnek 3: yönetim grubunda satır içi bir ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="989dc-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="989dc-118">Bu komut, VMPolicyDefinition adında bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="989dc-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="989dc-119">Komut ilkeyi geçerli JSON biçiminde bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="989dc-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="989dc-120">Örnek 4: meta verilerle bir ilke tanımı satıriçi oluşturma</span><span class="sxs-lookup"><span data-stu-id="989dc-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="989dc-121">Bu komut, VMPolicyDefinition adlı bir ilke tanımını, kategorisini "sanal makine" olarak belirtecek şekilde oluşturur.</span><span class="sxs-lookup"><span data-stu-id="989dc-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="989dc-122">Komut ilkeyi geçerli JSON biçiminde bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="989dc-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="989dc-123">Örnek 5: mod ile satır içi bir ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="989dc-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="989dc-124">Bu komut, bu ilkenin, yalnızca etiketleri ve konumu destekleyen kaynak türleri için değerlendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="989dc-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="989dc-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="989dc-125">PARAMETERS</span></span>

### <span data-ttu-id="989dc-126">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="989dc-126">-ApiVersion</span></span>
<span data-ttu-id="989dc-127">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="989dc-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="989dc-128">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="989dc-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="989dc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989dc-129">-DefaultProfile</span></span>
<span data-ttu-id="989dc-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="989dc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="989dc-131">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="989dc-131">-Description</span></span>
<span data-ttu-id="989dc-132">İlke tanımının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="989dc-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="989dc-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="989dc-133">-DisplayName</span></span>
<span data-ttu-id="989dc-134">İlke tanımı için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="989dc-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="989dc-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="989dc-135">-ManagementGroupName</span></span>
<span data-ttu-id="989dc-136">Yeni ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="989dc-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="989dc-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="989dc-137">-Metadata</span></span>
<span data-ttu-id="989dc-138">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="989dc-138">The metadata for policy definition.</span></span> <span data-ttu-id="989dc-139">Bu, meta veri içeren bir dosya adının yolu veya dize olarak meta veri olabilir</span><span class="sxs-lookup"><span data-stu-id="989dc-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="989dc-140">-Mod</span><span class="sxs-lookup"><span data-stu-id="989dc-140">-Mode</span></span>
<span data-ttu-id="989dc-141">İlke tanımının modu</span><span class="sxs-lookup"><span data-stu-id="989dc-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989dc-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="989dc-142">-Name</span></span>
<span data-ttu-id="989dc-143">İlke tanımı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="989dc-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="989dc-144">-Parametre</span><span class="sxs-lookup"><span data-stu-id="989dc-144">-Parameter</span></span>
<span data-ttu-id="989dc-145">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="989dc-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="989dc-146">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="989dc-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="989dc-147">-İlke</span><span class="sxs-lookup"><span data-stu-id="989dc-147">-Policy</span></span>
<span data-ttu-id="989dc-148">İlke tanımı için bir ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="989dc-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="989dc-149">. Json dosyasının veya JSON biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="989dc-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="989dc-150">-Pre-</span><span class="sxs-lookup"><span data-stu-id="989dc-150">-Pre</span></span>
<span data-ttu-id="989dc-151">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="989dc-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="989dc-152">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="989dc-152">-SubscriptionId</span></span>
<span data-ttu-id="989dc-153">Yeni ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="989dc-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="989dc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989dc-154">CommonParameters</span></span>
<span data-ttu-id="989dc-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="989dc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989dc-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="989dc-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989dc-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="989dc-157">INPUTS</span></span>

### <span data-ttu-id="989dc-158">System. String</span><span class="sxs-lookup"><span data-stu-id="989dc-158">System.String</span></span>

### <span data-ttu-id="989dc-159">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="989dc-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="989dc-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="989dc-160">OUTPUTS</span></span>

### <span data-ttu-id="989dc-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="989dc-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="989dc-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="989dc-162">NOTES</span></span>

## <span data-ttu-id="989dc-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="989dc-163">RELATED LINKS</span></span>

[<span data-ttu-id="989dc-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="989dc-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="989dc-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="989dc-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="989dc-166">Set-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="989dc-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


