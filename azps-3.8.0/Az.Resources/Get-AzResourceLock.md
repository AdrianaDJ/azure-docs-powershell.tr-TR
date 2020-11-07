---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937811"
---
# <span data-ttu-id="0e518-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0e518-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="0e518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e518-102">SYNOPSIS</span></span>
<span data-ttu-id="0e518-103">Kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-103">Gets a resource lock.</span></span>

## <span data-ttu-id="0e518-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e518-104">SYNTAX</span></span>

### <span data-ttu-id="0e518-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e518-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e518-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0e518-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e518-107">Bybelirtildiedscope</span><span class="sxs-lookup"><span data-stu-id="0e518-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e518-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0e518-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e518-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0e518-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e518-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0e518-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e518-111">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="0e518-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e518-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e518-112">DESCRIPTION</span></span>
<span data-ttu-id="0e518-113">**Get-AzResourceLock** cmdlet 'i Azure kaynak kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="0e518-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e518-114">EXAMPLES</span></span>

### <span data-ttu-id="0e518-115">Örnek 1: kilit alma</span><span class="sxs-lookup"><span data-stu-id="0e518-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0e518-116">Bu komut, ContosoSiteLock adındaki kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="0e518-117">Örnek 2: Kaynak Grup düzeyindeki veya üzeri kilitleri alma</span><span class="sxs-lookup"><span data-stu-id="0e518-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="0e518-118">Bu komut, kaynak grubundaki veya abonelikteki kaynak kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="0e518-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e518-119">PARAMETERS</span></span>

### <span data-ttu-id="0e518-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0e518-120">-ApiVersion</span></span>
<span data-ttu-id="0e518-121">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0e518-122">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0e518-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0e518-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="0e518-123">-AtScope</span></span>
<span data-ttu-id="0e518-124">Bu cmdlet 'in belirtilen kapsamda veya yukarısındaki tüm kilitleri döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="0e518-125">Bu parametreyi belirtmezseniz, cmdlet, kapsamın üstünde veya altında tüm kilitleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0e518-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="0e518-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e518-126">-DefaultProfile</span></span>
<span data-ttu-id="0e518-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0e518-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e518-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="0e518-128">-LockId</span></span>
<span data-ttu-id="0e518-129">Bu cmdlet 'in aldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0e518-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="0e518-130">-LockName</span></span>
<span data-ttu-id="0e518-131">Bu cmdlet 'in aldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-131">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e518-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0e518-132">-Pre</span></span>
<span data-ttu-id="0e518-133">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e518-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0e518-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e518-134">-ResourceGroupName</span></span>
<span data-ttu-id="0e518-135">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="0e518-136">Bu cmdlet bu kaynak grubunun kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="0e518-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0e518-137">-ResourceName</span></span>
<span data-ttu-id="0e518-138">Bu kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="0e518-139">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-139">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0e518-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0e518-140">-ResourceType</span></span>
<span data-ttu-id="0e518-141">Bu kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="0e518-142">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-142">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0e518-143">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0e518-143">-Scope</span></span>
<span data-ttu-id="0e518-144">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e518-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="0e518-145">Cmdlet bu kapsamın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0e518-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="0e518-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0e518-146">-TenantLevel</span></span>
<span data-ttu-id="0e518-147">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e518-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0e518-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e518-148">CommonParameters</span></span>
<span data-ttu-id="0e518-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e518-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e518-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0e518-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e518-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e518-151">INPUTS</span></span>

### <span data-ttu-id="0e518-152">System. String</span><span class="sxs-lookup"><span data-stu-id="0e518-152">System.String</span></span>

## <span data-ttu-id="0e518-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e518-153">OUTPUTS</span></span>

### <span data-ttu-id="0e518-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0e518-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0e518-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e518-155">NOTES</span></span>

## <span data-ttu-id="0e518-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e518-156">RELATED LINKS</span></span>

[<span data-ttu-id="0e518-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0e518-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="0e518-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0e518-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="0e518-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0e518-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


