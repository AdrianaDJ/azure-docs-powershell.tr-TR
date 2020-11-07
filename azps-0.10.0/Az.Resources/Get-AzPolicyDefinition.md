---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 66901872a6a7c3e871ce95287b45966aee974b52
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936440"
---
# <span data-ttu-id="d87dc-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d87dc-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="d87dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d87dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d87dc-103">İlke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-103">Gets policy definitions.</span></span>

## <span data-ttu-id="d87dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d87dc-104">SYNTAX</span></span>

### <span data-ttu-id="d87dc-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d87dc-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d87dc-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d87dc-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d87dc-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d87dc-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d87dc-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="d87dc-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d87dc-109">Buılfilterparameterset</span><span class="sxs-lookup"><span data-stu-id="d87dc-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d87dc-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="d87dc-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d87dc-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="d87dc-111">DESCRIPTION</span></span>
<span data-ttu-id="d87dc-112">**Get-AzPolicyDefinition** cmdlet 'i, ilke tanımlarının bir koleksiyonunu veya ad veya kimlikle tanımlanan belirli bir ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="d87dc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d87dc-113">EXAMPLES</span></span>

### <span data-ttu-id="d87dc-114">Örnek 1: tüm ilke tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="d87dc-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="d87dc-115">Bu komut, tüm ilke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="d87dc-116">Örnek 2: geçerli abonelikten ilke tanımını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="d87dc-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="d87dc-117">Bu komut, VMPolicyDefinition adlı ilke tanımını geçerli varsayılan aboneliğinden alır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="d87dc-118">Örnek 3: yönetim grubundan adla ilke tanımı alma</span><span class="sxs-lookup"><span data-stu-id="d87dc-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="d87dc-119">Bu komut, Dept42 adındaki yönetim grubundan VMPolicyDefinition adındaki ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="d87dc-120">Örnek 4: aboneliğin tüm yerleşik ilke tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="d87dc-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="d87dc-121">Bu komut, KIMLIK 3bf44b72-c631-427A-b8c8-53e2595398ca ile aboneliğin tüm yerleşik ilke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="d87dc-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d87dc-122">PARAMETERS</span></span>

### <span data-ttu-id="d87dc-123">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="d87dc-123">-ApiVersion</span></span>
<span data-ttu-id="d87dc-124">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d87dc-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d87dc-125">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d87dc-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="d87dc-126">-Builtin</span></span>
<span data-ttu-id="d87dc-127">Yalnızca yerleşik ilke tanımlarının sonuçları listesini sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="d87dc-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="d87dc-128">-Özel</span><span class="sxs-lookup"><span data-stu-id="d87dc-128">-Custom</span></span>
<span data-ttu-id="d87dc-129">Yalnızca özel ilke tanımlarına sonuç listesini kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="d87dc-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="d87dc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87dc-130">-DefaultProfile</span></span>
<span data-ttu-id="d87dc-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d87dc-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d87dc-132">-ID</span><span class="sxs-lookup"><span data-stu-id="d87dc-132">-Id</span></span>
<span data-ttu-id="d87dc-133">Bu cmdlet 'in aldığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d87dc-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d87dc-134">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d87dc-134">-InformationAction</span></span>
<span data-ttu-id="d87dc-135">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d87dc-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d87dc-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d87dc-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d87dc-137">'A</span><span class="sxs-lookup"><span data-stu-id="d87dc-137">Continue</span></span>
- <span data-ttu-id="d87dc-138">Manıza</span><span class="sxs-lookup"><span data-stu-id="d87dc-138">Ignore</span></span>
- <span data-ttu-id="d87dc-139">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d87dc-139">Inquire</span></span>
- <span data-ttu-id="d87dc-140">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d87dc-140">SilentlyContinue</span></span>
- <span data-ttu-id="d87dc-141">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d87dc-141">Stop</span></span>
- <span data-ttu-id="d87dc-142">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d87dc-142">Suspend</span></span>

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

### <span data-ttu-id="d87dc-143">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d87dc-143">-InformationVariable</span></span>
<span data-ttu-id="d87dc-144">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d87dc-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d87dc-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d87dc-145">-ManagementGroupName</span></span>
<span data-ttu-id="d87dc-146">Alınacak ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d87dc-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="d87dc-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="d87dc-147">-Name</span></span>
<span data-ttu-id="d87dc-148">Bu cmdlet 'in aldığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d87dc-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d87dc-149">-Pre-</span><span class="sxs-lookup"><span data-stu-id="d87dc-149">-Pre</span></span>
<span data-ttu-id="d87dc-150">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d87dc-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d87dc-151">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d87dc-151">-SubscriptionId</span></span>
<span data-ttu-id="d87dc-152">Alınacak ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d87dc-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="d87dc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87dc-153">CommonParameters</span></span>
<span data-ttu-id="d87dc-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d87dc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87dc-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d87dc-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87dc-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d87dc-156">INPUTS</span></span>

## <span data-ttu-id="d87dc-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d87dc-157">OUTPUTS</span></span>

## <span data-ttu-id="d87dc-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d87dc-158">NOTES</span></span>

## <span data-ttu-id="d87dc-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d87dc-159">RELATED LINKS</span></span>

[<span data-ttu-id="d87dc-160">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="d87dc-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="d87dc-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d87dc-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="d87dc-162">Set-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="d87dc-162">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


