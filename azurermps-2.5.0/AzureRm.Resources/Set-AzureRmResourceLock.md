---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: ccb491742d9a66a7e6eb300d7e75be0dcfac687e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938761"
---
# <span data-ttu-id="efacd-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="efacd-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="efacd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efacd-102">SYNOPSIS</span></span>
<span data-ttu-id="efacd-103">Kaynak kilidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="efacd-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efacd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efacd-104">SYNTAX</span></span>

### <span data-ttu-id="efacd-105">Bybelirtilmediscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efacd-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efacd-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="efacd-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efacd-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="efacd-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efacd-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="efacd-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efacd-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="efacd-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efacd-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="efacd-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efacd-111">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="efacd-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efacd-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="efacd-112">DESCRIPTION</span></span>
<span data-ttu-id="efacd-113">**Set-AzureRmResourceLock** cmdlet 'i kaynak kilidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="efacd-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="efacd-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efacd-114">EXAMPLES</span></span>

### <span data-ttu-id="efacd-115">Örnek 1: kilidin notlarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="efacd-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="efacd-116">Bu komut, ContosoSiteLock adındaki kilit için notu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efacd-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="efacd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efacd-117">PARAMETERS</span></span>

### <span data-ttu-id="efacd-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="efacd-118">-ApiVersion</span></span>
<span data-ttu-id="efacd-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="efacd-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="efacd-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="efacd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efacd-121">-DefaultProfile</span></span>
<span data-ttu-id="efacd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="efacd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efacd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="efacd-123">-Force</span></span>
<span data-ttu-id="efacd-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="efacd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="efacd-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="efacd-125">-InformationAction</span></span>
<span data-ttu-id="efacd-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="efacd-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="efacd-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efacd-128">'A</span><span class="sxs-lookup"><span data-stu-id="efacd-128">Continue</span></span>
- <span data-ttu-id="efacd-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="efacd-129">Ignore</span></span>
- <span data-ttu-id="efacd-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="efacd-130">Inquire</span></span>
- <span data-ttu-id="efacd-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="efacd-131">SilentlyContinue</span></span>
- <span data-ttu-id="efacd-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="efacd-132">Stop</span></span>
- <span data-ttu-id="efacd-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="efacd-133">Suspend</span></span>

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

### <span data-ttu-id="efacd-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="efacd-134">-InformationVariable</span></span>
<span data-ttu-id="efacd-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="efacd-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="efacd-136">-LockId</span></span>
<span data-ttu-id="efacd-137">Bu cmdlet 'in değiştirdiği kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="efacd-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="efacd-138">-LockLevel</span></span>
<span data-ttu-id="efacd-139">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="efacd-140">Şu anda tek geçerli değer CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="efacd-140">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="efacd-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="efacd-141">-LockName</span></span>
<span data-ttu-id="efacd-142">Bu cmdlet 'in değiştirdiği kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="efacd-143">-Locktes</span><span class="sxs-lookup"><span data-stu-id="efacd-143">-LockNotes</span></span>
<span data-ttu-id="efacd-144">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="efacd-145">-Pre-</span><span class="sxs-lookup"><span data-stu-id="efacd-145">-Pre</span></span>
<span data-ttu-id="efacd-146">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="efacd-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="efacd-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efacd-147">-ResourceGroupName</span></span>
<span data-ttu-id="efacd-148">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="efacd-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="efacd-149">-ResourceName</span></span>
<span data-ttu-id="efacd-150">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="efacd-151">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: sunucu `/` veritabanı</span><span class="sxs-lookup"><span data-stu-id="efacd-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="efacd-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="efacd-152">-ResourceType</span></span>
<span data-ttu-id="efacd-153">Kilidin uygulandığı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="efacd-154">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="efacd-154">-Scope</span></span>
<span data-ttu-id="efacd-155">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacd-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="efacd-156">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: `/subscriptions/` ABONELIK kimliği `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı kaynak grubu belirtmek için aşağıdaki BIÇIMI kullanın: `/subscriptions/` abonelik kimliği `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="efacd-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="efacd-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="efacd-157">-TenantLevel</span></span>
<span data-ttu-id="efacd-158">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="efacd-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="efacd-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="efacd-159">-Confirm</span></span>
<span data-ttu-id="efacd-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="efacd-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efacd-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efacd-161">-WhatIf</span></span>
<span data-ttu-id="efacd-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="efacd-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efacd-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="efacd-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efacd-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efacd-164">CommonParameters</span></span>
<span data-ttu-id="efacd-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efacd-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efacd-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efacd-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efacd-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efacd-167">INPUTS</span></span>

## <span data-ttu-id="efacd-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efacd-168">OUTPUTS</span></span>

## <span data-ttu-id="efacd-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efacd-169">NOTES</span></span>

## <span data-ttu-id="efacd-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efacd-170">RELATED LINKS</span></span>

[<span data-ttu-id="efacd-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="efacd-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="efacd-172">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="efacd-172">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="efacd-173">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="efacd-173">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


