---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: 0b3498ba3107e2312b596143820036286b925b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762360"
---
# <span data-ttu-id="a89d9-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a89d9-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="a89d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a89d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a89d9-103">Kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a89d9-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a89d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a89d9-104">SYNTAX</span></span>

### <span data-ttu-id="a89d9-105">Bybelirtilmediscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a89d9-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a89d9-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a89d9-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a89d9-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="a89d9-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89d9-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="a89d9-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a89d9-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a89d9-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89d9-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a89d9-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89d9-111">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="a89d9-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a89d9-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="a89d9-112">DESCRIPTION</span></span>
<span data-ttu-id="a89d9-113">**New-AzureRmResourceLock** cmdlet 'i kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a89d9-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="a89d9-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a89d9-114">EXAMPLES</span></span>

### <span data-ttu-id="a89d9-115">Örnek 1: Web sitesinde kaynak kilidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a89d9-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="a89d9-116">Bu komut, Web sitesinde kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a89d9-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="a89d9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a89d9-117">PARAMETERS</span></span>

### <span data-ttu-id="a89d9-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a89d9-118">-ApiVersion</span></span>
<span data-ttu-id="a89d9-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a89d9-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="a89d9-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89d9-121">-DefaultProfile</span></span>
<span data-ttu-id="a89d9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a89d9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a89d9-123">-Force</span></span>
<span data-ttu-id="a89d9-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a89d9-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a89d9-125">-InformationAction</span></span>
<span data-ttu-id="a89d9-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a89d9-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a89d9-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a89d9-128">'A</span><span class="sxs-lookup"><span data-stu-id="a89d9-128">Continue</span></span>
- <span data-ttu-id="a89d9-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="a89d9-129">Ignore</span></span>
- <span data-ttu-id="a89d9-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="a89d9-130">Inquire</span></span>
- <span data-ttu-id="a89d9-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="a89d9-131">SilentlyContinue</span></span>
- <span data-ttu-id="a89d9-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="a89d9-132">Stop</span></span>
- <span data-ttu-id="a89d9-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="a89d9-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="a89d9-134">-InformationVariable</span></span>
<span data-ttu-id="a89d9-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="a89d9-136">-LockId</span></span>
<span data-ttu-id="a89d9-137">Kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-137">Specifies the ID of the lock.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a89d9-138">-LockLevel</span></span>
<span data-ttu-id="a89d9-139">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="a89d9-140">Geçerli değerler şu anda CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="a89d9-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="a89d9-141">-LockName</span></span>
<span data-ttu-id="a89d9-142">Kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-142">Specifies the name of the lock.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-143">-Locktes</span><span class="sxs-lookup"><span data-stu-id="a89d9-143">-LockNotes</span></span>
<span data-ttu-id="a89d9-144">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-145">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a89d9-145">-Pre</span></span>
<span data-ttu-id="a89d9-146">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89d9-147">-ResourceGroupName</span></span>
<span data-ttu-id="a89d9-148">Kilidin uygulandığı kaynak grubunun adını veya kilidin uygulandığı kaynak grubunu içerir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a89d9-149">-ResourceName</span></span>
<span data-ttu-id="a89d9-150">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="a89d9-151">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="a89d9-151">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a89d9-152">-ResourceType</span></span>
<span data-ttu-id="a89d9-153">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-153">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-154">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a89d9-154">-Scope</span></span>
<span data-ttu-id="a89d9-155">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="a89d9-156">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="a89d9-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="a89d9-157">`/subscriptions/`abonelik KIMLIĞI `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="a89d9-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="a89d9-158">Kaynak grubu belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="a89d9-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="a89d9-159">`/subscriptions/`abonelik KIMLIĞI `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a89d9-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a89d9-160">-TenantLevel</span></span>
<span data-ttu-id="a89d9-161">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="a89d9-162">-Confirm</span></span>
<span data-ttu-id="a89d9-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a89d9-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a89d9-164">-WhatIf</span></span>
<span data-ttu-id="a89d9-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a89d9-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a89d9-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a89d9-166">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89d9-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89d9-167">CommonParameters</span></span>
<span data-ttu-id="a89d9-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a89d9-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89d9-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89d9-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89d9-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a89d9-170">INPUTS</span></span>

### <span data-ttu-id="a89d9-171">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a89d9-171">None</span></span>
<span data-ttu-id="a89d9-172">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a89d9-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a89d9-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a89d9-173">OUTPUTS</span></span>

### <span data-ttu-id="a89d9-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a89d9-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a89d9-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a89d9-175">NOTES</span></span>

## <span data-ttu-id="a89d9-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a89d9-176">RELATED LINKS</span></span>

[<span data-ttu-id="a89d9-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a89d9-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="a89d9-178">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a89d9-178">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="a89d9-179">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a89d9-179">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


