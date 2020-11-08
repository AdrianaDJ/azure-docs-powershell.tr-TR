---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266445"
---
# <span data-ttu-id="ba2ff-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba2ff-101">New-AzResourceLock</span></span>

## <span data-ttu-id="ba2ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2ff-103">Kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-103">Creates a resource lock.</span></span>

## <span data-ttu-id="ba2ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba2ff-104">SYNTAX</span></span>

### <span data-ttu-id="ba2ff-105">Bybelirtilmediscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba2ff-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba2ff-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba2ff-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba2ff-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="ba2ff-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba2ff-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="ba2ff-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba2ff-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ba2ff-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba2ff-110">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="ba2ff-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba2ff-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba2ff-111">DESCRIPTION</span></span>
<span data-ttu-id="ba2ff-112">**New-AzResourceLock** cmdlet 'i kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="ba2ff-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba2ff-113">EXAMPLES</span></span>

### <span data-ttu-id="ba2ff-114">Örnek 1: Web sitesinde kaynak kilidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ba2ff-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="ba2ff-115">Bu komut, Web sitesinde kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="ba2ff-116">Örnek 2: veritabanında kaynak kilidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ba2ff-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="ba2ff-117">Bu komut, bir Azure veritabanında kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="ba2ff-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba2ff-118">PARAMETERS</span></span>

### <span data-ttu-id="ba2ff-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ba2ff-119">-ApiVersion</span></span>
<span data-ttu-id="ba2ff-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ba2ff-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ba2ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2ff-122">-DefaultProfile</span></span>
<span data-ttu-id="ba2ff-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba2ff-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba2ff-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ba2ff-124">-Force</span></span>
<span data-ttu-id="ba2ff-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba2ff-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="ba2ff-126">-LockId</span></span>
<span data-ttu-id="ba2ff-127">Kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="ba2ff-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="ba2ff-128">-LockLevel</span></span>
<span data-ttu-id="ba2ff-129">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="ba2ff-130">Geçerli değerler şu anda CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="ba2ff-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="ba2ff-131">-LockName</span></span>
<span data-ttu-id="ba2ff-132">Kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="ba2ff-133">-Locktes</span><span class="sxs-lookup"><span data-stu-id="ba2ff-133">-LockNotes</span></span>
<span data-ttu-id="ba2ff-134">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="ba2ff-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ba2ff-135">-Pre</span></span>
<span data-ttu-id="ba2ff-136">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ba2ff-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba2ff-137">-ResourceGroupName</span></span>
<span data-ttu-id="ba2ff-138">Kilidin uygulandığı kaynak grubunun adını veya kilidin uygulandığı kaynak grubunu içerir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="ba2ff-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ba2ff-139">-ResourceName</span></span>
<span data-ttu-id="ba2ff-140">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="ba2ff-141">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ba2ff-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ba2ff-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ba2ff-142">-ResourceType</span></span>
<span data-ttu-id="ba2ff-143">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="ba2ff-144">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ba2ff-144">-Scope</span></span>
<span data-ttu-id="ba2ff-145">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="ba2ff-146">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: `/subscriptions/` ABONELIK kimliği `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı kaynak grubu belirtmek için aşağıdaki BIÇIMI kullanın: `/subscriptions/` abonelik kimliği `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ba2ff-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="ba2ff-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba2ff-147">-Confirm</span></span>
<span data-ttu-id="ba2ff-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba2ff-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba2ff-149">-WhatIf</span></span>
<span data-ttu-id="ba2ff-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba2ff-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba2ff-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2ff-152">CommonParameters</span></span>
<span data-ttu-id="ba2ff-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2ff-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2ff-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba2ff-155">INPUTS</span></span>

### <span data-ttu-id="ba2ff-156">System. String</span><span class="sxs-lookup"><span data-stu-id="ba2ff-156">System.String</span></span>

### <span data-ttu-id="ba2ff-157">Microsoft. Azure. Commands. ResourceManager. cmdlet. varlıklar. kilitler. LockLevel</span><span class="sxs-lookup"><span data-stu-id="ba2ff-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="ba2ff-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba2ff-158">OUTPUTS</span></span>

### <span data-ttu-id="ba2ff-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ba2ff-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ba2ff-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba2ff-160">NOTES</span></span>

## <span data-ttu-id="ba2ff-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba2ff-161">RELATED LINKS</span></span>

[<span data-ttu-id="ba2ff-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba2ff-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="ba2ff-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba2ff-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="ba2ff-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba2ff-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


