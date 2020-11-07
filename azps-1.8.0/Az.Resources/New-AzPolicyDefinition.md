---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 07882064fae3cfc4a24899b6106480551f3681a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759387"
---
# <span data-ttu-id="0797f-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0797f-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="0797f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0797f-102">SYNOPSIS</span></span>
<span data-ttu-id="0797f-103">İlke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0797f-103">Creates a policy definition.</span></span>

## <span data-ttu-id="0797f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0797f-104">SYNTAX</span></span>

### <span data-ttu-id="0797f-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0797f-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0797f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0797f-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0797f-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0797f-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0797f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0797f-108">DESCRIPTION</span></span>
<span data-ttu-id="0797f-109">**Yeni-Azilketanımı** cmdlet 'ı JavaScript nesne GÖSTERIMI (JSON) biçiminde ilke kuralı içeren bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0797f-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="0797f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0797f-110">EXAMPLES</span></span>

### <span data-ttu-id="0797f-111">Örnek 1: ilke dosyası kullanarak ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0797f-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="0797f-112">Bu komut, C:\LocationPolicy.json alanında belirtilen ilke kuralını içeren LocationDefinition adlı bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0797f-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="0797f-113">LocationPolicy.jsdosyanın içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="0797f-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="0797f-114">Örnek 2: satır içi parametreler kullanarak parametreli bir ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0797f-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="0797f-115">Bu komut, C:\LocationPolicy.json alanında belirtilen ilke kuralını içeren LocationDefinition adlı bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0797f-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="0797f-116">İlke kuralının parametre tanımı satır içi olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="0797f-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="0797f-117">Örnek 3: yönetim grubunda satır içi bir ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0797f-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="0797f-118">Bu komut, VMPolicyDefinition adında bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0797f-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="0797f-119">Komut ilkeyi geçerli JSON biçiminde bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0797f-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="0797f-120">Örnek 4: meta verilerle bir ilke tanımı satıriçi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0797f-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="0797f-121">Bu komut, VMPolicyDefinition adlı bir ilke tanımını, kategorisini "sanal makine" olarak belirtecek şekilde oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0797f-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="0797f-122">Komut ilkeyi geçerli JSON biçiminde bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0797f-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="0797f-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0797f-123">PARAMETERS</span></span>

### <span data-ttu-id="0797f-124">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0797f-124">-ApiVersion</span></span>
<span data-ttu-id="0797f-125">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0797f-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0797f-126">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0797f-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0797f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0797f-127">-DefaultProfile</span></span>
<span data-ttu-id="0797f-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0797f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0797f-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="0797f-129">-Description</span></span>
<span data-ttu-id="0797f-130">İlke tanımının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0797f-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="0797f-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0797f-131">-DisplayName</span></span>
<span data-ttu-id="0797f-132">İlke tanımı için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0797f-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="0797f-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0797f-133">-ManagementGroupName</span></span>
<span data-ttu-id="0797f-134">Yeni ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0797f-134">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="0797f-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0797f-135">-Metadata</span></span>
<span data-ttu-id="0797f-136">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="0797f-136">The metadata for policy definition.</span></span> <span data-ttu-id="0797f-137">Bu, meta veri içeren bir dosya adının yolu veya dize olarak meta veri olabilir</span><span class="sxs-lookup"><span data-stu-id="0797f-137">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="0797f-138">-Mod</span><span class="sxs-lookup"><span data-stu-id="0797f-138">-Mode</span></span>
<span data-ttu-id="0797f-139">İlke tanımının modu</span><span class="sxs-lookup"><span data-stu-id="0797f-139">The mode of the policy definition</span></span>

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

### <span data-ttu-id="0797f-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="0797f-140">-Name</span></span>
<span data-ttu-id="0797f-141">İlke tanımı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0797f-141">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="0797f-142">-Parametre</span><span class="sxs-lookup"><span data-stu-id="0797f-142">-Parameter</span></span>
<span data-ttu-id="0797f-143">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="0797f-143">The parameters declaration for policy definition.</span></span> <span data-ttu-id="0797f-144">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="0797f-144">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="0797f-145">-İlke</span><span class="sxs-lookup"><span data-stu-id="0797f-145">-Policy</span></span>
<span data-ttu-id="0797f-146">İlke tanımı için bir ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0797f-146">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="0797f-147">. Json dosyasının veya JSON biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0797f-147">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="0797f-148">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0797f-148">-Pre</span></span>
<span data-ttu-id="0797f-149">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0797f-149">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0797f-150">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0797f-150">-SubscriptionId</span></span>
<span data-ttu-id="0797f-151">Yeni ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0797f-151">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="0797f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0797f-152">CommonParameters</span></span>
<span data-ttu-id="0797f-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0797f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0797f-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0797f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0797f-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0797f-155">INPUTS</span></span>

### <span data-ttu-id="0797f-156">System. String</span><span class="sxs-lookup"><span data-stu-id="0797f-156">System.String</span></span>

### <span data-ttu-id="0797f-157">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="0797f-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0797f-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0797f-158">OUTPUTS</span></span>

### <span data-ttu-id="0797f-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0797f-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0797f-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0797f-160">NOTES</span></span>

## <span data-ttu-id="0797f-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0797f-161">RELATED LINKS</span></span>

[<span data-ttu-id="0797f-162">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0797f-162">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="0797f-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0797f-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="0797f-164">Set-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="0797f-164">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


