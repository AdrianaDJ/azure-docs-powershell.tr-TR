---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322780"
---
# <span data-ttu-id="e74ab-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e74ab-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="e74ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e74ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e74ab-103">Kaynak kilidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="e74ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e74ab-104">SYNTAX</span></span>

### <span data-ttu-id="e74ab-105">Bybelirtilmediscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e74ab-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e74ab-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e74ab-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74ab-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e74ab-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74ab-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e74ab-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e74ab-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e74ab-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e74ab-110">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="e74ab-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e74ab-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="e74ab-111">DESCRIPTION</span></span>
<span data-ttu-id="e74ab-112">**Set-AzResourceLock** cmdlet 'i kaynak kilidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="e74ab-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e74ab-113">EXAMPLES</span></span>

### <span data-ttu-id="e74ab-114">Örnek 1: kilidin notlarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e74ab-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e74ab-115">Bu komut, ContosoSiteLock adındaki kilit için notu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="e74ab-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e74ab-116">PARAMETERS</span></span>

### <span data-ttu-id="e74ab-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e74ab-117">-ApiVersion</span></span>
<span data-ttu-id="e74ab-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e74ab-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="e74ab-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e74ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e74ab-120">-DefaultProfile</span></span>
<span data-ttu-id="e74ab-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e74ab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e74ab-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e74ab-122">-Force</span></span>
<span data-ttu-id="e74ab-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e74ab-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e74ab-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="e74ab-124">-LockId</span></span>
<span data-ttu-id="e74ab-125">Bu cmdlet 'in değiştirdiği kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e74ab-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="e74ab-126">-LockLevel</span></span>
<span data-ttu-id="e74ab-127">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="e74ab-128">Şu anda tek geçerli değer CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="e74ab-128">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e74ab-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="e74ab-129">-LockName</span></span>
<span data-ttu-id="e74ab-130">Bu cmdlet 'in değiştirdiği kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e74ab-131">-Locktes</span><span class="sxs-lookup"><span data-stu-id="e74ab-131">-LockNotes</span></span>
<span data-ttu-id="e74ab-132">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-132">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e74ab-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e74ab-133">-Pre</span></span>
<span data-ttu-id="e74ab-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e74ab-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e74ab-135">-ResourceGroupName</span></span>
<span data-ttu-id="e74ab-136">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="e74ab-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e74ab-137">-ResourceName</span></span>
<span data-ttu-id="e74ab-138">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="e74ab-139">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: sunucu `/` veritabanı</span><span class="sxs-lookup"><span data-stu-id="e74ab-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e74ab-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e74ab-140">-ResourceType</span></span>
<span data-ttu-id="e74ab-141">Kilidin uygulandığı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-141">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e74ab-142">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="e74ab-142">-Scope</span></span>
<span data-ttu-id="e74ab-143">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="e74ab-144">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: `/subscriptions/` ABONELIK kimliği `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı kaynak grubu belirtmek için aşağıdaki BIÇIMI kullanın: `/subscriptions/` abonelik kimliği `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e74ab-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="e74ab-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="e74ab-145">-Confirm</span></span>
<span data-ttu-id="e74ab-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e74ab-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e74ab-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e74ab-147">-WhatIf</span></span>
<span data-ttu-id="e74ab-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e74ab-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e74ab-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e74ab-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e74ab-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e74ab-150">CommonParameters</span></span>
<span data-ttu-id="e74ab-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e74ab-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e74ab-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e74ab-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e74ab-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e74ab-153">INPUTS</span></span>

### <span data-ttu-id="e74ab-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e74ab-154">System.String</span></span>

### <span data-ttu-id="e74ab-155">Microsoft. Azure. Commands. ResourceManager. cmdlet. varlıklar. kilitler. LockLevel</span><span class="sxs-lookup"><span data-stu-id="e74ab-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="e74ab-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e74ab-156">OUTPUTS</span></span>

### <span data-ttu-id="e74ab-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e74ab-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e74ab-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e74ab-158">NOTES</span></span>

## <span data-ttu-id="e74ab-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e74ab-159">RELATED LINKS</span></span>

[<span data-ttu-id="e74ab-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e74ab-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="e74ab-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e74ab-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="e74ab-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e74ab-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


