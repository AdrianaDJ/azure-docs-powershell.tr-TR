---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763623"
---
# <span data-ttu-id="87b9a-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87b9a-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="87b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="87b9a-103">Kaynak kilidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87b9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87b9a-104">SYNTAX</span></span>

### <span data-ttu-id="87b9a-105">Belirtilen kapsamda bir kilit.</span><span class="sxs-lookup"><span data-stu-id="87b9a-105">A lock at the specified scope.</span></span> <span data-ttu-id="87b9a-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="87b9a-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87b9a-107">Kaynak grubu kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="87b9a-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87b9a-108">Kaynak Grup kaynak kapsamından bir kilit.</span><span class="sxs-lookup"><span data-stu-id="87b9a-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b9a-109">Abonelik kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="87b9a-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87b9a-110">Abonelik kaynağı kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="87b9a-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b9a-111">Kiracı kaynak kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="87b9a-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b9a-112">Kimliğe göre bir kilit.</span><span class="sxs-lookup"><span data-stu-id="87b9a-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87b9a-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="87b9a-113">DESCRIPTION</span></span>
<span data-ttu-id="87b9a-114">**Set-AzureRmResourceLock** cmdlet 'i kaynak kilidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="87b9a-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87b9a-115">EXAMPLES</span></span>

### <span data-ttu-id="87b9a-116">Örnek 1: kilidin notlarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="87b9a-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="87b9a-117">Bu komut, ContosoSiteLock adındaki kilit için notu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="87b9a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87b9a-118">PARAMETERS</span></span>

### <span data-ttu-id="87b9a-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="87b9a-119">-ApiVersion</span></span>
<span data-ttu-id="87b9a-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="87b9a-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="87b9a-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="87b9a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="87b9a-122">-Force</span></span>
<span data-ttu-id="87b9a-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="87b9a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87b9a-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="87b9a-124">-InformationAction</span></span>
<span data-ttu-id="87b9a-125">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87b9a-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="87b9a-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87b9a-127">'A</span><span class="sxs-lookup"><span data-stu-id="87b9a-127">Continue</span></span>
- <span data-ttu-id="87b9a-128">Manıza</span><span class="sxs-lookup"><span data-stu-id="87b9a-128">Ignore</span></span>
- <span data-ttu-id="87b9a-129">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="87b9a-129">Inquire</span></span>
- <span data-ttu-id="87b9a-130">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="87b9a-130">SilentlyContinue</span></span>
- <span data-ttu-id="87b9a-131">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="87b9a-131">Stop</span></span>
- <span data-ttu-id="87b9a-132">Biliriz</span><span class="sxs-lookup"><span data-stu-id="87b9a-132">Suspend</span></span>

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

### <span data-ttu-id="87b9a-133">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="87b9a-133">-InformationVariable</span></span>
<span data-ttu-id="87b9a-134">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="87b9a-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="87b9a-135">-LockId</span></span>
<span data-ttu-id="87b9a-136">Bu cmdlet 'in değiştirdiği kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87b9a-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="87b9a-137">-LockLevel</span></span>
<span data-ttu-id="87b9a-138">Kilidin düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="87b9a-139">Şu anda tek geçerli değer CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="87b9a-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="87b9a-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="87b9a-140">-LockName</span></span>
<span data-ttu-id="87b9a-141">Bu cmdlet 'in değiştirdiği kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87b9a-142">-Locktes</span><span class="sxs-lookup"><span data-stu-id="87b9a-142">-LockNotes</span></span>
<span data-ttu-id="87b9a-143">Kilidin notlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="87b9a-144">-Pre-</span><span class="sxs-lookup"><span data-stu-id="87b9a-144">-Pre</span></span>
<span data-ttu-id="87b9a-145">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="87b9a-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b9a-146">-ResourceGroupName</span></span>
<span data-ttu-id="87b9a-147">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-147">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="87b9a-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="87b9a-148">-ResourceName</span></span>
<span data-ttu-id="87b9a-149">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="87b9a-150">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="87b9a-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="87b9a-151">Sunucu `/` veritabanı</span><span class="sxs-lookup"><span data-stu-id="87b9a-151">Server`/`Database</span></span>

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

### <span data-ttu-id="87b9a-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="87b9a-152">-ResourceType</span></span>
<span data-ttu-id="87b9a-153">Kilidin uygulandığı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="87b9a-154">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="87b9a-154">-Scope</span></span>
<span data-ttu-id="87b9a-155">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="87b9a-156">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="87b9a-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="87b9a-157">`/subscriptions/`abonelik KIMLIĞI `/resourceGroups/` kaynak grubu adı `/providers/Microsoft.Sql/servers/` sunucu adı `/databases/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="87b9a-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="87b9a-158">Kaynak grubu belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="87b9a-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="87b9a-159">`/subscriptions/`abonelik KIMLIĞI `/resourceGroups/` kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="87b9a-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="87b9a-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="87b9a-160">-TenantLevel</span></span>
<span data-ttu-id="87b9a-161">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-161">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="87b9a-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="87b9a-162">-Confirm</span></span>
<span data-ttu-id="87b9a-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87b9a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b9a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b9a-164">-WhatIf</span></span>
<span data-ttu-id="87b9a-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87b9a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b9a-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87b9a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b9a-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b9a-167">-DefaultProfile</span></span>
<span data-ttu-id="87b9a-168">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87b9a-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b9a-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b9a-169">CommonParameters</span></span>
<span data-ttu-id="87b9a-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87b9a-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b9a-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b9a-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b9a-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87b9a-172">INPUTS</span></span>

## <span data-ttu-id="87b9a-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87b9a-173">OUTPUTS</span></span>

### <span data-ttu-id="87b9a-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="87b9a-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="87b9a-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87b9a-175">NOTES</span></span>

## <span data-ttu-id="87b9a-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87b9a-176">RELATED LINKS</span></span>

[<span data-ttu-id="87b9a-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87b9a-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="87b9a-178">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87b9a-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="87b9a-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87b9a-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


