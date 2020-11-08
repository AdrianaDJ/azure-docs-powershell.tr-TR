---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266426"
---
# <span data-ttu-id="e2c54-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e2c54-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="e2c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2c54-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c54-103">İlke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2c54-103">Removes a policy definition.</span></span>

## <span data-ttu-id="e2c54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2c54-104">SYNTAX</span></span>

### <span data-ttu-id="e2c54-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2c54-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c54-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2c54-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c54-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e2c54-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c54-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="e2c54-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c54-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="e2c54-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2c54-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2c54-110">DESCRIPTION</span></span>
<span data-ttu-id="e2c54-111">**Remove-AzPolicyDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2c54-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="e2c54-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2c54-112">EXAMPLES</span></span>

### <span data-ttu-id="e2c54-113">Örnek 1: ilke tanımını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="e2c54-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="e2c54-114">Bu komut belirtilen ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2c54-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="e2c54-115">Örnek 2: kaynak KIMLIĞIYLE ilke tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e2c54-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="e2c54-116">İlk komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="e2c54-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="e2c54-117">Komut, $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e2c54-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="e2c54-118">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliğinin tanımladığı ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2c54-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="e2c54-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2c54-119">PARAMETERS</span></span>

### <span data-ttu-id="e2c54-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e2c54-120">-ApiVersion</span></span>
<span data-ttu-id="e2c54-121">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c54-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e2c54-122">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="e2c54-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e2c54-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c54-123">-DefaultProfile</span></span>
<span data-ttu-id="e2c54-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e2c54-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2c54-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e2c54-125">-Force</span></span>
<span data-ttu-id="e2c54-126">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e2c54-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2c54-127">-ID</span><span class="sxs-lookup"><span data-stu-id="e2c54-127">-Id</span></span>
<span data-ttu-id="e2c54-128">Bu cmdlet 'in kaldırdığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c54-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2c54-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2c54-129">-InputObject</span></span>
<span data-ttu-id="e2c54-130">Başka bir cmdlet 'ten çıktı olan, kaldırılacak ilke tanımı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e2c54-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="e2c54-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e2c54-131">-ManagementGroupName</span></span>
<span data-ttu-id="e2c54-132">Silinecek ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e2c54-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="e2c54-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2c54-133">-Name</span></span>
<span data-ttu-id="e2c54-134">Bu cmdlet 'in kaldırdığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c54-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c54-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e2c54-135">-Pre</span></span>
<span data-ttu-id="e2c54-136">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2c54-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e2c54-137">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e2c54-137">-SubscriptionId</span></span>
<span data-ttu-id="e2c54-138">Silinecek ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e2c54-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="e2c54-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2c54-139">-Confirm</span></span>
<span data-ttu-id="e2c54-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2c54-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c54-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2c54-141">-WhatIf</span></span>
<span data-ttu-id="e2c54-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2c54-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2c54-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2c54-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c54-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c54-144">CommonParameters</span></span>
<span data-ttu-id="e2c54-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2c54-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c54-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2c54-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c54-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2c54-147">INPUTS</span></span>

### <span data-ttu-id="e2c54-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e2c54-148">System.String</span></span>

### <span data-ttu-id="e2c54-149">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2c54-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e2c54-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2c54-150">OUTPUTS</span></span>

### <span data-ttu-id="e2c54-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2c54-151">System.Boolean</span></span>

## <span data-ttu-id="e2c54-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2c54-152">NOTES</span></span>

## <span data-ttu-id="e2c54-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2c54-153">RELATED LINKS</span></span>

[<span data-ttu-id="e2c54-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e2c54-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="e2c54-155">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="e2c54-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="e2c54-156">Set-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="e2c54-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


