---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: bd374f19a282ccafc3201a2965c33d4e8a3007ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097238"
---
# <span data-ttu-id="3d1aa-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d1aa-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="3d1aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1aa-103">İlke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-103">Removes a policy definition.</span></span>

## <span data-ttu-id="3d1aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d1aa-104">SYNTAX</span></span>

### <span data-ttu-id="3d1aa-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d1aa-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d1aa-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d1aa-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d1aa-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3d1aa-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d1aa-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="3d1aa-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d1aa-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d1aa-109">DESCRIPTION</span></span>
<span data-ttu-id="3d1aa-110">**Remove-AzPolicyDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="3d1aa-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d1aa-111">EXAMPLES</span></span>

### <span data-ttu-id="3d1aa-112">Örnek 1: ilke tanımını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="3d1aa-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="3d1aa-113">Bu komut belirtilen ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="3d1aa-114">Örnek 2: kaynak KIMLIĞIYLE ilke tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3d1aa-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="3d1aa-115">İlk komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3d1aa-116">Komut, $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="3d1aa-117">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliğinin tanımladığı ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="3d1aa-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d1aa-118">PARAMETERS</span></span>

### <span data-ttu-id="3d1aa-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="3d1aa-119">-ApiVersion</span></span>
<span data-ttu-id="3d1aa-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d1aa-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3d1aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1aa-122">-DefaultProfile</span></span>
<span data-ttu-id="3d1aa-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3d1aa-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d1aa-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3d1aa-124">-Force</span></span>
<span data-ttu-id="3d1aa-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d1aa-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3d1aa-126">-Id</span></span>
<span data-ttu-id="3d1aa-127">Bu cmdlet 'in kaldırdığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3d1aa-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3d1aa-128">-ManagementGroupName</span></span>
<span data-ttu-id="3d1aa-129">Silinecek ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="3d1aa-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d1aa-130">-Name</span></span>
<span data-ttu-id="3d1aa-131">Bu cmdlet 'in kaldırdığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3d1aa-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="3d1aa-132">-Pre</span></span>
<span data-ttu-id="3d1aa-133">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3d1aa-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3d1aa-134">-SubscriptionId</span></span>
<span data-ttu-id="3d1aa-135">Silinecek ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="3d1aa-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d1aa-136">-Confirm</span></span>
<span data-ttu-id="3d1aa-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d1aa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d1aa-138">-WhatIf</span></span>
<span data-ttu-id="3d1aa-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d1aa-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d1aa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1aa-141">CommonParameters</span></span>
<span data-ttu-id="3d1aa-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1aa-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d1aa-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1aa-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d1aa-144">INPUTS</span></span>

### <span data-ttu-id="3d1aa-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3d1aa-145">System.String</span></span>

### <span data-ttu-id="3d1aa-146">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="3d1aa-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3d1aa-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d1aa-147">OUTPUTS</span></span>

### <span data-ttu-id="3d1aa-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d1aa-148">System.Boolean</span></span>

## <span data-ttu-id="3d1aa-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d1aa-149">NOTES</span></span>

## <span data-ttu-id="3d1aa-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d1aa-150">RELATED LINKS</span></span>

[<span data-ttu-id="3d1aa-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d1aa-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="3d1aa-152">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="3d1aa-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="3d1aa-153">Set-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="3d1aa-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


