---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d558e7104027e4c3fcef3b6e8d8427d5fd3802fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764298"
---
# <span data-ttu-id="f5637-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f5637-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="f5637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5637-102">SYNOPSIS</span></span>
<span data-ttu-id="f5637-103">İlke kümesi tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="f5637-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5637-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5637-104">SYNTAX</span></span>

### <span data-ttu-id="f5637-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5637-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5637-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5637-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5637-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f5637-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5637-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="f5637-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5637-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5637-109">DESCRIPTION</span></span>
<span data-ttu-id="f5637-110">**Set-AzureRmPolicySetDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f5637-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f5637-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5637-111">EXAMPLES</span></span>

### <span data-ttu-id="f5637-112">Örnek 1: ilke kümesi tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f5637-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f5637-113">İlk komut, Get-AzureRmPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="f5637-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="f5637-114">Komut bu nesneyi $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f5637-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="f5637-115">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliği tarafından tanımlanan ilke kümesi tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="f5637-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="f5637-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5637-116">PARAMETERS</span></span>

### <span data-ttu-id="f5637-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f5637-117">-ApiVersion</span></span>
<span data-ttu-id="f5637-118">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5637-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5637-119">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f5637-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f5637-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5637-120">-DefaultProfile</span></span>
<span data-ttu-id="f5637-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f5637-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5637-122">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f5637-122">-Description</span></span>
<span data-ttu-id="f5637-123">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="f5637-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="f5637-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f5637-124">-DisplayName</span></span>
<span data-ttu-id="f5637-125">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="f5637-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="f5637-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f5637-126">-Id</span></span>
<span data-ttu-id="f5637-127">Abonelik dahil tam nitelikli ilke tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="f5637-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="f5637-128">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="f5637-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="f5637-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f5637-129">-ManagementGroupName</span></span>
<span data-ttu-id="f5637-130">Güncelleştirilecek ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f5637-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="f5637-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f5637-131">-Metadata</span></span>
<span data-ttu-id="f5637-132">Güncelleştirilmiş ilke kümesi tanımının meta verileri.</span><span class="sxs-lookup"><span data-stu-id="f5637-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="f5637-133">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="f5637-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="f5637-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5637-134">-Name</span></span>
<span data-ttu-id="f5637-135">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="f5637-135">The policy set definition name.</span></span>

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

### <span data-ttu-id="f5637-136">-Parametre</span><span class="sxs-lookup"><span data-stu-id="f5637-136">-Parameter</span></span>
<span data-ttu-id="f5637-137">Güncelleştirilmiş ilke kümesi tanımının parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="f5637-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="f5637-138">Bu, parametre bildirimini içeren bir dosya adı veya URI veya dize olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="f5637-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="f5637-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f5637-139">-PolicyDefinition</span></span>
<span data-ttu-id="f5637-140">İlke kümesi tanımı.</span><span class="sxs-lookup"><span data-stu-id="f5637-140">The policy set definition.</span></span> <span data-ttu-id="f5637-141">Bu, ilke tanımlarını içeren bir dosya adına veya ilke kümesi tanımına dize olarak bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="f5637-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="f5637-142">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f5637-142">-Pre</span></span>
<span data-ttu-id="f5637-143">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5637-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f5637-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f5637-144">-SubscriptionId</span></span>
<span data-ttu-id="f5637-145">Güncelleştirilecek ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f5637-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="f5637-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5637-146">-Confirm</span></span>
<span data-ttu-id="f5637-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5637-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5637-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5637-148">-WhatIf</span></span>
<span data-ttu-id="f5637-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5637-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5637-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5637-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5637-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5637-151">CommonParameters</span></span>
<span data-ttu-id="f5637-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5637-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5637-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5637-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5637-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5637-154">INPUTS</span></span>

### <span data-ttu-id="f5637-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f5637-155">System.String</span></span>

### <span data-ttu-id="f5637-156">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f5637-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f5637-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5637-157">OUTPUTS</span></span>

### <span data-ttu-id="f5637-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f5637-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5637-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5637-159">NOTES</span></span>

## <span data-ttu-id="f5637-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5637-160">RELATED LINKS</span></span>
