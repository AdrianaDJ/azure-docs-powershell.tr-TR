---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098099"
---
# <span data-ttu-id="19fe3-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19fe3-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="19fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="19fe3-103">İlke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-103">Gets policy definitions.</span></span>

## <span data-ttu-id="19fe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19fe3-104">SYNTAX</span></span>

### <span data-ttu-id="19fe3-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19fe3-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19fe3-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19fe3-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19fe3-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="19fe3-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19fe3-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="19fe3-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19fe3-109">Buılfilterparameterset</span><span class="sxs-lookup"><span data-stu-id="19fe3-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19fe3-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="19fe3-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19fe3-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="19fe3-111">DESCRIPTION</span></span>
<span data-ttu-id="19fe3-112">**Get-AzPolicyDefinition** cmdlet 'i, ilke tanımlarının bir koleksiyonunu veya ad veya kimlikle tanımlanan belirli bir ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="19fe3-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19fe3-113">EXAMPLES</span></span>

### <span data-ttu-id="19fe3-114">Örnek 1: tüm ilke tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="19fe3-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="19fe3-115">Bu komut, tüm ilke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="19fe3-116">Örnek 2: geçerli abonelikten ilke tanımını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="19fe3-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="19fe3-117">Bu komut, VMPolicyDefinition adlı ilke tanımını geçerli varsayılan aboneliğinden alır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="19fe3-118">Örnek 3: yönetim grubundan adla ilke tanımı alma</span><span class="sxs-lookup"><span data-stu-id="19fe3-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="19fe3-119">Bu komut, Dept42 adındaki yönetim grubundan VMPolicyDefinition adındaki ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="19fe3-120">Örnek 4: aboneliğin tüm yerleşik ilke tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="19fe3-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="19fe3-121">Bu komut, KIMLIK 3bf44b72-c631-427A-b8c8-53e2595398ca ile aboneliğin tüm yerleşik ilke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="19fe3-122">Örnek 5: belirli bir kategorideki ilke tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="19fe3-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="19fe3-123">Bu komut, "sanal makine" kategorisindeki tüm ilke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="19fe3-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19fe3-124">PARAMETERS</span></span>

### <span data-ttu-id="19fe3-125">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="19fe3-125">-ApiVersion</span></span>
<span data-ttu-id="19fe3-126">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19fe3-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="19fe3-127">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="19fe3-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="19fe3-128">-Builtin</span></span>
<span data-ttu-id="19fe3-129">Yalnızca yerleşik ilke tanımlarının sonuçları listesini sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="19fe3-129">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19fe3-130">-Özel</span><span class="sxs-lookup"><span data-stu-id="19fe3-130">-Custom</span></span>
<span data-ttu-id="19fe3-131">Yalnızca özel ilke tanımlarına sonuç listesini kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="19fe3-131">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19fe3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19fe3-132">-DefaultProfile</span></span>
<span data-ttu-id="19fe3-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="19fe3-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19fe3-134">-ID</span><span class="sxs-lookup"><span data-stu-id="19fe3-134">-Id</span></span>
<span data-ttu-id="19fe3-135">Bu cmdlet 'in aldığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="19fe3-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19fe3-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="19fe3-136">-ManagementGroupName</span></span>
<span data-ttu-id="19fe3-137">Alınacak ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="19fe3-137">The name of the management group of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19fe3-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="19fe3-138">-Name</span></span>
<span data-ttu-id="19fe3-139">Bu cmdlet 'in aldığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19fe3-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19fe3-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="19fe3-140">-Pre</span></span>
<span data-ttu-id="19fe3-141">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="19fe3-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="19fe3-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="19fe3-142">-SubscriptionId</span></span>
<span data-ttu-id="19fe3-143">Alınacak ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="19fe3-143">The subscription ID of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19fe3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19fe3-144">CommonParameters</span></span>
<span data-ttu-id="19fe3-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19fe3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19fe3-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="19fe3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19fe3-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19fe3-147">INPUTS</span></span>

### <span data-ttu-id="19fe3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="19fe3-148">System.String</span></span>

### <span data-ttu-id="19fe3-149">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="19fe3-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="19fe3-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19fe3-150">OUTPUTS</span></span>

### <span data-ttu-id="19fe3-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="19fe3-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19fe3-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19fe3-152">NOTES</span></span>

## <span data-ttu-id="19fe3-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19fe3-153">RELATED LINKS</span></span>

[<span data-ttu-id="19fe3-154">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="19fe3-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="19fe3-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19fe3-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="19fe3-156">Set-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="19fe3-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


