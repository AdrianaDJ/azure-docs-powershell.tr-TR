---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 8c4352f6345bc6de76208d6821aadd6c249174ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937663"
---
# <span data-ttu-id="9fb91-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9fb91-101">New-AzResourceLock</span></span>

## <span data-ttu-id="9fb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb91-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb91-103">Kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fb91-103">Creates a resource lock.</span></span>

## <span data-ttu-id="9fb91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fb91-104">SYNTAX</span></span>

### <span data-ttu-id="9fb91-105">Bybelirtilmediscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fb91-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb91-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9fb91-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb91-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="9fb91-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb91-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="9fb91-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb91-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9fb91-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb91-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9fb91-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb91-111">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="9fb91-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fb91-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fb91-112">DESCRIPTION</span></span>
<span data-ttu-id="9fb91-113">**New-AzResourceLock** cmdlet 'i kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fb91-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="9fb91-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fb91-114">EXAMPLES</span></span>

### <span data-ttu-id="9fb91-115">Örnek 1: Web sitesinde kaynak kilidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9fb91-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="9fb91-116">Bu komut, Web sitesinde kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fb91-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="9fb91-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fb91-117">PARAMETERS</span></span>

### <span data-ttu-id="9fb91-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="9fb91-118">-ApiVersion</span></span>
<span data-ttu-id="9fb91-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9fb91-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="9fb91-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9fb91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb91-121">-DefaultProfile</span></span>
<span data-ttu-id="9fb91-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9fb91-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fb91-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9fb91-123">-Force</span></span>
<span data-ttu-id="9fb91-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9fb91-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9fb91-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="9fb91-125">-LockId</span></span>
<span data-ttu-id="9fb91-126">Kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="9fb91-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="9fb91-127">-LockLevel</span></span>
<span data-ttu-id="9fb91-128">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="9fb91-129">Geçerli değerler şu anda CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="9fb91-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="9fb91-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="9fb91-130">-LockName</span></span>
<span data-ttu-id="9fb91-131">Kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-131">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb91-132">-Locktes</span><span class="sxs-lookup"><span data-stu-id="9fb91-132">-LockNotes</span></span>
<span data-ttu-id="9fb91-133">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="9fb91-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9fb91-134">-Pre</span></span>
<span data-ttu-id="9fb91-135">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9fb91-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb91-136">-ResourceGroupName</span></span>
<span data-ttu-id="9fb91-137">Kilidin uygulandığı kaynak grubunun adını veya kilidin uygulandığı kaynak grubunu içerir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="9fb91-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9fb91-138">-ResourceName</span></span>
<span data-ttu-id="9fb91-139">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="9fb91-140">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9fb91-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9fb91-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9fb91-141">-ResourceType</span></span>
<span data-ttu-id="9fb91-142">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-142">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="9fb91-143">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="9fb91-143">-Scope</span></span>
<span data-ttu-id="9fb91-144">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="9fb91-145">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: `/subscriptions/` ABONELIK kimliği `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı kaynak grubu belirtmek için aşağıdaki BIÇIMI kullanın: `/subscriptions/` abonelik kimliği `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9fb91-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="9fb91-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9fb91-146">-TenantLevel</span></span>
<span data-ttu-id="9fb91-147">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9fb91-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="9fb91-148">-Confirm</span></span>
<span data-ttu-id="9fb91-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9fb91-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fb91-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb91-150">-WhatIf</span></span>
<span data-ttu-id="9fb91-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fb91-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb91-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9fb91-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fb91-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb91-153">CommonParameters</span></span>
<span data-ttu-id="9fb91-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fb91-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb91-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9fb91-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb91-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fb91-156">INPUTS</span></span>

### <span data-ttu-id="9fb91-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9fb91-157">System.String</span></span>

### <span data-ttu-id="9fb91-158">Microsoft. Azure. Commands. ResourceManager. cmdlet. varlıklar. kilitler. LockLevel</span><span class="sxs-lookup"><span data-stu-id="9fb91-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="9fb91-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fb91-159">OUTPUTS</span></span>

### <span data-ttu-id="9fb91-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9fb91-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9fb91-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fb91-161">NOTES</span></span>

## <span data-ttu-id="9fb91-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fb91-162">RELATED LINKS</span></span>

[<span data-ttu-id="9fb91-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9fb91-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="9fb91-164">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9fb91-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="9fb91-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9fb91-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


