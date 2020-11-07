---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 8d4f4180cc827c879dde0252044d30d5242d2300
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936384"
---
# <span data-ttu-id="0011a-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0011a-101">New-AzResourceLock</span></span>

## <span data-ttu-id="0011a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0011a-102">SYNOPSIS</span></span>
<span data-ttu-id="0011a-103">Kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0011a-103">Creates a resource lock.</span></span>

## <span data-ttu-id="0011a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0011a-104">SYNTAX</span></span>

### <span data-ttu-id="0011a-105">Bybelirtilmediscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0011a-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0011a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0011a-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0011a-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0011a-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0011a-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0011a-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0011a-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0011a-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0011a-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0011a-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0011a-111">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="0011a-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0011a-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="0011a-112">DESCRIPTION</span></span>
<span data-ttu-id="0011a-113">**New-AzResourceLock** cmdlet 'i kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0011a-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="0011a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0011a-114">EXAMPLES</span></span>

### <span data-ttu-id="0011a-115">Örnek 1: Web sitesinde kaynak kilidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0011a-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="0011a-116">Bu komut, Web sitesinde kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0011a-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="0011a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0011a-117">PARAMETERS</span></span>

### <span data-ttu-id="0011a-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0011a-118">-ApiVersion</span></span>
<span data-ttu-id="0011a-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0011a-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0011a-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0011a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0011a-121">-DefaultProfile</span></span>
<span data-ttu-id="0011a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0011a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0011a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0011a-123">-Force</span></span>
<span data-ttu-id="0011a-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0011a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0011a-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0011a-125">-InformationAction</span></span>
<span data-ttu-id="0011a-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0011a-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0011a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0011a-128">'A</span><span class="sxs-lookup"><span data-stu-id="0011a-128">Continue</span></span>
- <span data-ttu-id="0011a-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="0011a-129">Ignore</span></span>
- <span data-ttu-id="0011a-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="0011a-130">Inquire</span></span>
- <span data-ttu-id="0011a-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="0011a-131">SilentlyContinue</span></span>
- <span data-ttu-id="0011a-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="0011a-132">Stop</span></span>
- <span data-ttu-id="0011a-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="0011a-133">Suspend</span></span>

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

### <span data-ttu-id="0011a-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="0011a-134">-InformationVariable</span></span>
<span data-ttu-id="0011a-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0011a-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="0011a-136">-LockId</span></span>
<span data-ttu-id="0011a-137">Kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="0011a-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="0011a-138">-LockLevel</span></span>
<span data-ttu-id="0011a-139">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="0011a-140">Geçerli değerler şu anda CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="0011a-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0011a-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="0011a-141">-LockName</span></span>
<span data-ttu-id="0011a-142">Kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="0011a-143">-Locktes</span><span class="sxs-lookup"><span data-stu-id="0011a-143">-LockNotes</span></span>
<span data-ttu-id="0011a-144">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="0011a-145">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0011a-145">-Pre</span></span>
<span data-ttu-id="0011a-146">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0011a-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0011a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0011a-147">-ResourceGroupName</span></span>
<span data-ttu-id="0011a-148">Kilidin uygulandığı kaynak grubunun adını veya kilidin uygulandığı kaynak grubunu içerir.</span><span class="sxs-lookup"><span data-stu-id="0011a-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="0011a-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0011a-149">-ResourceName</span></span>
<span data-ttu-id="0011a-150">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="0011a-151">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0011a-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0011a-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0011a-152">-ResourceType</span></span>
<span data-ttu-id="0011a-153">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="0011a-154">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0011a-154">-Scope</span></span>
<span data-ttu-id="0011a-155">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0011a-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="0011a-156">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: `/subscriptions/` ABONELIK kimliği `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı kaynak grubu belirtmek için aşağıdaki BIÇIMI kullanın: `/subscriptions/` abonelik kimliği `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0011a-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="0011a-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0011a-157">-TenantLevel</span></span>
<span data-ttu-id="0011a-158">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0011a-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0011a-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="0011a-159">-Confirm</span></span>
<span data-ttu-id="0011a-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0011a-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0011a-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0011a-161">-WhatIf</span></span>
<span data-ttu-id="0011a-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0011a-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0011a-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0011a-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0011a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0011a-164">CommonParameters</span></span>
<span data-ttu-id="0011a-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0011a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0011a-166">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0011a-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0011a-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0011a-167">INPUTS</span></span>

## <span data-ttu-id="0011a-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0011a-168">OUTPUTS</span></span>

## <span data-ttu-id="0011a-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0011a-169">NOTES</span></span>

## <span data-ttu-id="0011a-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0011a-170">RELATED LINKS</span></span>

[<span data-ttu-id="0011a-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0011a-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="0011a-172">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0011a-172">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="0011a-173">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0011a-173">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


