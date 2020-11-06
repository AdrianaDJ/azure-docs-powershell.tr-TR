---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594575"
---
# <span data-ttu-id="86ed2-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="86ed2-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="86ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="86ed2-103">Kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86ed2-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ed2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86ed2-104">SYNTAX</span></span>

### <span data-ttu-id="86ed2-105">Belirtilen kapsamda bir kilit.</span><span class="sxs-lookup"><span data-stu-id="86ed2-105">A lock at the specified scope.</span></span> <span data-ttu-id="86ed2-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="86ed2-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86ed2-107">Kaynak grubu kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="86ed2-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86ed2-108">Kaynak Grup kaynak kapsamından bir kilit.</span><span class="sxs-lookup"><span data-stu-id="86ed2-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ed2-109">Abonelik kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="86ed2-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86ed2-110">Abonelik kaynağı kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="86ed2-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ed2-111">Kiracı kaynak kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="86ed2-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ed2-112">Kimliğe göre bir kilit.</span><span class="sxs-lookup"><span data-stu-id="86ed2-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86ed2-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="86ed2-113">DESCRIPTION</span></span>
<span data-ttu-id="86ed2-114">**New-AzureRmResourceLock** cmdlet 'i kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86ed2-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="86ed2-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86ed2-115">EXAMPLES</span></span>

### <span data-ttu-id="86ed2-116">Örnek 1: Web sitesinde kaynak kilidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="86ed2-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="86ed2-117">Bu komut, Web sitesinde kaynak kilidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86ed2-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="86ed2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86ed2-118">PARAMETERS</span></span>

### <span data-ttu-id="86ed2-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="86ed2-119">-ApiVersion</span></span>
<span data-ttu-id="86ed2-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="86ed2-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="86ed2-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="86ed2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="86ed2-122">-Force</span></span>
<span data-ttu-id="86ed2-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="86ed2-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="86ed2-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="86ed2-124">-InformationAction</span></span>
<span data-ttu-id="86ed2-125">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86ed2-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="86ed2-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86ed2-127">'A</span><span class="sxs-lookup"><span data-stu-id="86ed2-127">Continue</span></span>
- <span data-ttu-id="86ed2-128">Manıza</span><span class="sxs-lookup"><span data-stu-id="86ed2-128">Ignore</span></span>
- <span data-ttu-id="86ed2-129">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="86ed2-129">Inquire</span></span>
- <span data-ttu-id="86ed2-130">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="86ed2-130">SilentlyContinue</span></span>
- <span data-ttu-id="86ed2-131">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="86ed2-131">Stop</span></span>
- <span data-ttu-id="86ed2-132">Biliriz</span><span class="sxs-lookup"><span data-stu-id="86ed2-132">Suspend</span></span>

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

### <span data-ttu-id="86ed2-133">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="86ed2-133">-InformationVariable</span></span>
<span data-ttu-id="86ed2-134">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="86ed2-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="86ed2-135">-LockId</span></span>
<span data-ttu-id="86ed2-136">Kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-136">Specifies the ID of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ed2-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="86ed2-137">-LockLevel</span></span>
<span data-ttu-id="86ed2-138">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="86ed2-139">Şu anda tek geçerli değer CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="86ed2-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="86ed2-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="86ed2-140">-LockName</span></span>
<span data-ttu-id="86ed2-141">Kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-141">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ed2-142">-Locktes</span><span class="sxs-lookup"><span data-stu-id="86ed2-142">-LockNotes</span></span>
<span data-ttu-id="86ed2-143">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="86ed2-144">-Pre-</span><span class="sxs-lookup"><span data-stu-id="86ed2-144">-Pre</span></span>
<span data-ttu-id="86ed2-145">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="86ed2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ed2-146">-ResourceGroupName</span></span>
<span data-ttu-id="86ed2-147">Kilidin uygulandığı kaynak grubunun adını veya kilidin uygulandığı kaynak grubunu içerir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ed2-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="86ed2-148">-ResourceName</span></span>
<span data-ttu-id="86ed2-149">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="86ed2-150">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="86ed2-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ed2-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="86ed2-151">-ResourceType</span></span>
<span data-ttu-id="86ed2-152">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-152">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ed2-153">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="86ed2-153">-Scope</span></span>
<span data-ttu-id="86ed2-154">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="86ed2-155">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="86ed2-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="86ed2-156">`/subscriptions/`abonelik KIMLIĞI `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="86ed2-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="86ed2-157">Kaynak grubu belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="86ed2-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="86ed2-158">`/subscriptions/`abonelik KIMLIĞI `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="86ed2-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ed2-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="86ed2-159">-TenantLevel</span></span>
<span data-ttu-id="86ed2-160">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ed2-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="86ed2-161">-Confirm</span></span>
<span data-ttu-id="86ed2-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86ed2-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ed2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ed2-163">-WhatIf</span></span>
<span data-ttu-id="86ed2-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86ed2-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ed2-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86ed2-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ed2-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ed2-166">-DefaultProfile</span></span>
<span data-ttu-id="86ed2-167">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="86ed2-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86ed2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ed2-168">CommonParameters</span></span>
<span data-ttu-id="86ed2-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86ed2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ed2-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ed2-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ed2-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86ed2-171">INPUTS</span></span>

## <span data-ttu-id="86ed2-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86ed2-172">OUTPUTS</span></span>

### <span data-ttu-id="86ed2-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="86ed2-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="86ed2-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86ed2-174">NOTES</span></span>

## <span data-ttu-id="86ed2-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86ed2-175">RELATED LINKS</span></span>

[<span data-ttu-id="86ed2-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="86ed2-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="86ed2-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="86ed2-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="86ed2-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="86ed2-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


