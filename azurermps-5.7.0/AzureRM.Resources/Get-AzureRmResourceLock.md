---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: e3d0dfe975a6a76267864b329c3e3130f447cb58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573310"
---
# <span data-ttu-id="fadba-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="fadba-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="fadba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fadba-102">SYNOPSIS</span></span>
<span data-ttu-id="fadba-103">Kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="fadba-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fadba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fadba-104">SYNTAX</span></span>

### <span data-ttu-id="fadba-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fadba-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fadba-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="fadba-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fadba-107">Bybelirtildiedscope</span><span class="sxs-lookup"><span data-stu-id="fadba-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fadba-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="fadba-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fadba-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="fadba-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fadba-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fadba-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fadba-111">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="fadba-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fadba-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="fadba-112">DESCRIPTION</span></span>
<span data-ttu-id="fadba-113">**Get-AzureRmResourceLock** cmdlet 'i Azure kaynak kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fadba-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="fadba-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fadba-114">EXAMPLES</span></span>

### <span data-ttu-id="fadba-115">Örnek 1: kilit alma</span><span class="sxs-lookup"><span data-stu-id="fadba-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fadba-116">Bu komut, ContosoSiteLock adındaki kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="fadba-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="fadba-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fadba-117">PARAMETERS</span></span>

### <span data-ttu-id="fadba-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="fadba-118">-ApiVersion</span></span>
<span data-ttu-id="fadba-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fadba-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="fadba-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fadba-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="fadba-121">-AtScope</span></span>
<span data-ttu-id="fadba-122">Bu cmdlet 'in belirtilen kapsamda veya yukarısındaki tüm kilitleri döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="fadba-123">Bu parametreyi belirtmezseniz, cmdlet, kapsamın üstünde veya altında tüm kilitleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fadba-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="fadba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadba-124">-DefaultProfile</span></span>
<span data-ttu-id="fadba-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fadba-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fadba-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fadba-126">-InformationAction</span></span>
<span data-ttu-id="fadba-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fadba-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fadba-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fadba-129">'A</span><span class="sxs-lookup"><span data-stu-id="fadba-129">Continue</span></span>
- <span data-ttu-id="fadba-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="fadba-130">Ignore</span></span>
- <span data-ttu-id="fadba-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fadba-131">Inquire</span></span>
- <span data-ttu-id="fadba-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fadba-132">SilentlyContinue</span></span>
- <span data-ttu-id="fadba-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fadba-133">Stop</span></span>
- <span data-ttu-id="fadba-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fadba-134">Suspend</span></span>

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

### <span data-ttu-id="fadba-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fadba-135">-InformationVariable</span></span>
<span data-ttu-id="fadba-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fadba-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="fadba-137">-LockId</span></span>
<span data-ttu-id="fadba-138">Bu cmdlet 'in aldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fadba-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="fadba-139">-LockName</span></span>
<span data-ttu-id="fadba-140">Bu cmdlet 'in aldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-140">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadba-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fadba-141">-Pre</span></span>
<span data-ttu-id="fadba-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fadba-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fadba-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fadba-143">-ResourceGroupName</span></span>
<span data-ttu-id="fadba-144">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="fadba-145">Bu cmdlet bu kaynak grubunun kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fadba-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="fadba-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fadba-146">-ResourceName</span></span>
<span data-ttu-id="fadba-147">Bu kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="fadba-148">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fadba-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="fadba-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fadba-149">-ResourceType</span></span>
<span data-ttu-id="fadba-150">Bu kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="fadba-151">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fadba-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="fadba-152">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="fadba-152">-Scope</span></span>
<span data-ttu-id="fadba-153">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fadba-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="fadba-154">Cmdlet bu kapsamın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fadba-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="fadba-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fadba-155">-TenantLevel</span></span>
<span data-ttu-id="fadba-156">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="fadba-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="fadba-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadba-157">CommonParameters</span></span>
<span data-ttu-id="fadba-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fadba-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadba-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fadba-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadba-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fadba-160">INPUTS</span></span>

### <span data-ttu-id="fadba-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fadba-161">None</span></span>
<span data-ttu-id="fadba-162">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fadba-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fadba-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fadba-163">OUTPUTS</span></span>

### <span data-ttu-id="fadba-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fadba-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fadba-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fadba-165">NOTES</span></span>

## <span data-ttu-id="fadba-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fadba-166">RELATED LINKS</span></span>

[<span data-ttu-id="fadba-167">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="fadba-167">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="fadba-168">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="fadba-168">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="fadba-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="fadba-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


