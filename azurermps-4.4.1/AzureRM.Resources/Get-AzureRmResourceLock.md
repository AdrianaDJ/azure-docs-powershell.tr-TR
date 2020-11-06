---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592575"
---
# <span data-ttu-id="3a422-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3a422-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="3a422-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a422-102">SYNOPSIS</span></span>
<span data-ttu-id="3a422-103">Kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="3a422-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a422-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a422-104">SYNTAX</span></span>

### <span data-ttu-id="3a422-105">Kaynak grubu kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="3a422-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a422-106">Kaynak Grup kaynak kapsamından bir kilit.</span><span class="sxs-lookup"><span data-stu-id="3a422-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a422-107">Belirtilen kapsamda bir kilit.</span><span class="sxs-lookup"><span data-stu-id="3a422-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a422-108">Abonelik kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="3a422-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a422-109">Abonelik kaynağı kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="3a422-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a422-110">Kiracı kaynak kapsamındaki bir kilit.</span><span class="sxs-lookup"><span data-stu-id="3a422-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a422-111">Kimliğe göre bir kilit.</span><span class="sxs-lookup"><span data-stu-id="3a422-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3a422-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a422-112">DESCRIPTION</span></span>
<span data-ttu-id="3a422-113">**Get-AzureRmResourceLock** cmdlet 'i Azure kaynak kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a422-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="3a422-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a422-114">EXAMPLES</span></span>

### <span data-ttu-id="3a422-115">Örnek 1: kilit alma</span><span class="sxs-lookup"><span data-stu-id="3a422-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3a422-116">Bu komut, ContosoSiteLock adındaki kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="3a422-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="3a422-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a422-117">PARAMETERS</span></span>

### <span data-ttu-id="3a422-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="3a422-118">-ApiVersion</span></span>
<span data-ttu-id="3a422-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3a422-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="3a422-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3a422-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="3a422-121">-AtScope</span></span>
<span data-ttu-id="3a422-122">Bu cmdlet 'in belirtilen kapsamda veya yukarısındaki tüm kilitleri döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="3a422-123">Bu parametreyi belirtmezseniz, cmdlet, kapsamın üstünde veya altında tüm kilitleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a422-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="3a422-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3a422-124">-InformationAction</span></span>
<span data-ttu-id="3a422-125">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3a422-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3a422-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a422-127">'A</span><span class="sxs-lookup"><span data-stu-id="3a422-127">Continue</span></span>
- <span data-ttu-id="3a422-128">Manıza</span><span class="sxs-lookup"><span data-stu-id="3a422-128">Ignore</span></span>
- <span data-ttu-id="3a422-129">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="3a422-129">Inquire</span></span>
- <span data-ttu-id="3a422-130">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="3a422-130">SilentlyContinue</span></span>
- <span data-ttu-id="3a422-131">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="3a422-131">Stop</span></span>
- <span data-ttu-id="3a422-132">Biliriz</span><span class="sxs-lookup"><span data-stu-id="3a422-132">Suspend</span></span>

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

### <span data-ttu-id="3a422-133">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="3a422-133">-InformationVariable</span></span>
<span data-ttu-id="3a422-134">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3a422-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="3a422-135">-LockId</span></span>
<span data-ttu-id="3a422-136">Bu cmdlet 'in aldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3a422-137">-LockName</span><span class="sxs-lookup"><span data-stu-id="3a422-137">-LockName</span></span>
<span data-ttu-id="3a422-138">Bu cmdlet 'in aldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a422-139">-Pre-</span><span class="sxs-lookup"><span data-stu-id="3a422-139">-Pre</span></span>
<span data-ttu-id="3a422-140">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a422-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3a422-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a422-141">-ResourceGroupName</span></span>
<span data-ttu-id="3a422-142">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="3a422-143">Bu cmdlet bu kaynak grubunun kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a422-143">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="3a422-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3a422-144">-ResourceName</span></span>
<span data-ttu-id="3a422-145">Bu kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="3a422-146">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a422-146">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="3a422-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3a422-147">-ResourceType</span></span>
<span data-ttu-id="3a422-148">Bu kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="3a422-149">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a422-149">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="3a422-150">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="3a422-150">-Scope</span></span>
<span data-ttu-id="3a422-151">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a422-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="3a422-152">Cmdlet bu kapsamın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a422-152">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="3a422-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3a422-153">-TenantLevel</span></span>
<span data-ttu-id="3a422-154">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a422-154">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="3a422-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a422-155">-DefaultProfile</span></span>
<span data-ttu-id="3a422-156">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a422-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a422-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a422-157">CommonParameters</span></span>
<span data-ttu-id="3a422-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a422-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a422-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a422-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a422-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a422-160">INPUTS</span></span>

## <span data-ttu-id="3a422-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a422-161">OUTPUTS</span></span>

### <span data-ttu-id="3a422-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3a422-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3a422-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a422-163">NOTES</span></span>

## <span data-ttu-id="3a422-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a422-164">RELATED LINKS</span></span>

[<span data-ttu-id="3a422-165">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3a422-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="3a422-166">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3a422-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="3a422-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3a422-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


