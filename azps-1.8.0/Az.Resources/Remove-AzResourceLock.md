---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759331"
---
# <span data-ttu-id="26e0a-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26e0a-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="26e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="26e0a-103">Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26e0a-103">Removes a resource lock.</span></span>

## <span data-ttu-id="26e0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26e0a-104">SYNTAX</span></span>

### <span data-ttu-id="26e0a-105">Bylockıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26e0a-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e0a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26e0a-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e0a-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="26e0a-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e0a-108">Bybelirtildiedscope</span><span class="sxs-lookup"><span data-stu-id="26e0a-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e0a-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="26e0a-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e0a-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="26e0a-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26e0a-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="26e0a-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26e0a-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="26e0a-112">DESCRIPTION</span></span>
<span data-ttu-id="26e0a-113">**Remove-AzResourceLock** cmdlet 'ı bir Azure Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26e0a-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="26e0a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26e0a-114">EXAMPLES</span></span>

### <span data-ttu-id="26e0a-115">Örnek 1: kilidi kaldırma</span><span class="sxs-lookup"><span data-stu-id="26e0a-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="26e0a-116">Bu komut, ContosoSiteLock adındaki kilidi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26e0a-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="26e0a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26e0a-117">PARAMETERS</span></span>

### <span data-ttu-id="26e0a-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="26e0a-118">-ApiVersion</span></span>
<span data-ttu-id="26e0a-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="26e0a-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="26e0a-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="26e0a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e0a-121">-DefaultProfile</span></span>
<span data-ttu-id="26e0a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="26e0a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26e0a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="26e0a-123">-Force</span></span>
<span data-ttu-id="26e0a-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="26e0a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26e0a-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="26e0a-125">-LockId</span></span>
<span data-ttu-id="26e0a-126">Bu cmdlet 'in kaldırıldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e0a-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="26e0a-127">-LockName</span></span>
<span data-ttu-id="26e0a-128">Bu cmdlet 'in kaldırıldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-128">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e0a-129">-Pre-</span><span class="sxs-lookup"><span data-stu-id="26e0a-129">-Pre</span></span>
<span data-ttu-id="26e0a-130">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26e0a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e0a-131">-ResourceGroupName</span></span>
<span data-ttu-id="26e0a-132">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-132">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e0a-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="26e0a-133">-ResourceName</span></span>
<span data-ttu-id="26e0a-134">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="26e0a-135">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: sunucu `/` veritabanı</span><span class="sxs-lookup"><span data-stu-id="26e0a-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e0a-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="26e0a-136">-ResourceType</span></span>
<span data-ttu-id="26e0a-137">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-137">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e0a-138">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="26e0a-138">-Scope</span></span>
<span data-ttu-id="26e0a-139">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-139">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e0a-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="26e0a-140">-TenantLevel</span></span>
<span data-ttu-id="26e0a-141">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-141">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e0a-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="26e0a-142">-Confirm</span></span>
<span data-ttu-id="26e0a-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26e0a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e0a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e0a-144">-WhatIf</span></span>
<span data-ttu-id="26e0a-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26e0a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e0a-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26e0a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e0a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e0a-147">CommonParameters</span></span>
<span data-ttu-id="26e0a-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26e0a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e0a-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e0a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e0a-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26e0a-150">INPUTS</span></span>

### <span data-ttu-id="26e0a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="26e0a-151">System.String</span></span>

## <span data-ttu-id="26e0a-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26e0a-152">OUTPUTS</span></span>

### <span data-ttu-id="26e0a-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="26e0a-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="26e0a-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26e0a-154">NOTES</span></span>

## <span data-ttu-id="26e0a-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26e0a-155">RELATED LINKS</span></span>

[<span data-ttu-id="26e0a-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26e0a-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="26e0a-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26e0a-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="26e0a-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26e0a-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


