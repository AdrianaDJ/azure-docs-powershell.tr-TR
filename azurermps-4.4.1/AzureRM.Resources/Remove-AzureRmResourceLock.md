---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592555"
---
# <span data-ttu-id="f1857-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1857-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="f1857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1857-102">SYNOPSIS</span></span>
<span data-ttu-id="f1857-103">Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1857-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1857-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1857-104">SYNTAX</span></span>

### <span data-ttu-id="f1857-105">Bir kilit, kimliğe göre. (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1857-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1857-106">Kaynak grubu kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="f1857-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1857-107">Kaynak Grup kaynak kapsamından bir kilit.</span><span class="sxs-lookup"><span data-stu-id="f1857-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1857-108">Belirtilen kapsamda bir kilit.</span><span class="sxs-lookup"><span data-stu-id="f1857-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1857-109">Abonelik kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="f1857-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1857-110">Abonelik kaynağı kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="f1857-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1857-111">Kiracı kaynak kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="f1857-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1857-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1857-112">DESCRIPTION</span></span>
<span data-ttu-id="f1857-113">**Remove-AzureRmResourceLock** cmdlet 'ı bir Azure Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1857-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="f1857-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1857-114">EXAMPLES</span></span>

### <span data-ttu-id="f1857-115">Örnek 1: kilidi kaldırma</span><span class="sxs-lookup"><span data-stu-id="f1857-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="f1857-116">Bu komut, ContosoSiteLock adındaki kilidi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1857-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="f1857-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1857-117">PARAMETERS</span></span>

### <span data-ttu-id="f1857-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f1857-118">-ApiVersion</span></span>
<span data-ttu-id="f1857-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f1857-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="f1857-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f1857-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f1857-121">-Force</span></span>
<span data-ttu-id="f1857-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f1857-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1857-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f1857-123">-InformationAction</span></span>
<span data-ttu-id="f1857-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f1857-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f1857-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1857-126">'A</span><span class="sxs-lookup"><span data-stu-id="f1857-126">Continue</span></span>
- <span data-ttu-id="f1857-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="f1857-127">Ignore</span></span>
- <span data-ttu-id="f1857-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f1857-128">Inquire</span></span>
- <span data-ttu-id="f1857-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f1857-129">SilentlyContinue</span></span>
- <span data-ttu-id="f1857-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f1857-130">Stop</span></span>
- <span data-ttu-id="f1857-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f1857-131">Suspend</span></span>

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

### <span data-ttu-id="f1857-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f1857-132">-InformationVariable</span></span>
<span data-ttu-id="f1857-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f1857-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="f1857-134">-LockId</span></span>
<span data-ttu-id="f1857-135">Bu cmdlet 'in kaldırıldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f1857-136">-LockName</span><span class="sxs-lookup"><span data-stu-id="f1857-136">-LockName</span></span>
<span data-ttu-id="f1857-137">Bu cmdlet 'in kaldırıldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1857-138">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f1857-138">-Pre</span></span>
<span data-ttu-id="f1857-139">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1857-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f1857-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1857-140">-ResourceGroupName</span></span>
<span data-ttu-id="f1857-141">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-141">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="f1857-142">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f1857-142">-ResourceName</span></span>
<span data-ttu-id="f1857-143">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="f1857-144">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="f1857-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="f1857-145">Sunucu `/` veritabanı</span><span class="sxs-lookup"><span data-stu-id="f1857-145">Server`/`Database</span></span>

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

### <span data-ttu-id="f1857-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f1857-146">-ResourceType</span></span>
<span data-ttu-id="f1857-147">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-147">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="f1857-148">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="f1857-148">-Scope</span></span>
<span data-ttu-id="f1857-149">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1857-149">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="f1857-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f1857-150">-TenantLevel</span></span>
<span data-ttu-id="f1857-151">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1857-151">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f1857-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1857-152">-Confirm</span></span>
<span data-ttu-id="f1857-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1857-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1857-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1857-154">-WhatIf</span></span>
<span data-ttu-id="f1857-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1857-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1857-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1857-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1857-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1857-157">-DefaultProfile</span></span>
<span data-ttu-id="f1857-158">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1857-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1857-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1857-159">CommonParameters</span></span>
<span data-ttu-id="f1857-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1857-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1857-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1857-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1857-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1857-162">INPUTS</span></span>

## <span data-ttu-id="f1857-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1857-163">OUTPUTS</span></span>

### <span data-ttu-id="f1857-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f1857-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f1857-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1857-165">NOTES</span></span>

## <span data-ttu-id="f1857-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1857-166">RELATED LINKS</span></span>

[<span data-ttu-id="f1857-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1857-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="f1857-168">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1857-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="f1857-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1857-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


