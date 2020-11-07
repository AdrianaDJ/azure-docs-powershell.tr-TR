---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763368"
---
# <span data-ttu-id="64368-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="64368-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="64368-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64368-102">SYNOPSIS</span></span>
<span data-ttu-id="64368-103">Yeni bir etkinlik günlüğü uyarısını oluşturur veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64368-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64368-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64368-104">SYNTAX</span></span>

### <span data-ttu-id="64368-105">Etkinlik günlüğü uyarısı ayarla uyarısı</span><span class="sxs-lookup"><span data-stu-id="64368-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64368-106">Kanaldan RESOURCEID değerini alan etkinlik günlüğü uyarılarını ayarlamak için parametreler</span><span class="sxs-lookup"><span data-stu-id="64368-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64368-107">Kanaldan değer alma etkinlik günlüğü uyarıları ayarlama</span><span class="sxs-lookup"><span data-stu-id="64368-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64368-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="64368-108">DESCRIPTION</span></span>
<span data-ttu-id="64368-109">**Set-AzureRmActivityLogAlert** cmdlet 'i yeni oluşturur veya varolan bir etkinlik günlüğü uyarısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64368-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="64368-110">Etiketler, koşullar ve eylemler için, bu çağrıda virgülle ayrılmış olarak, nesnelerin önceden oluşturulması ve parametrelerin parametre olarak geçirilmesi gerekir (aşağıdaki örneğe bakın).</span><span class="sxs-lookup"><span data-stu-id="64368-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="64368-111">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten oluşturulması/değiştirilmesi öncesinde kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="64368-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="64368-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64368-112">EXAMPLES</span></span>

### <span data-ttu-id="64368-113">Örnek 1: etkinlik günlüğü uyarısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="64368-113">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="64368-114">İlk dört komut yaprak koşulu ve eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64368-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="64368-115">Son komutu koşulu ve eylem grubunu kullanarak etkinlik günlüğü uyarısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64368-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="64368-116">Örnek 2: etkinlik günlüğü uyarısı oluşturma devre dışı</span><span class="sxs-lookup"><span data-stu-id="64368-116">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="64368-117">İlk dört komut yaprak koşulu ve eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64368-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="64368-118">Son komutu koşulu ve eylem grubunu kullanarak etkinlik günlüğü uyarısı oluşturur, ancak uyarıyı devre dışı olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64368-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="64368-119">Örnek 3: kanalda veya InputObject parametresinden bir değer kullanarak etkinlik günlüğü uyarısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="64368-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="64368-120">İlk komut bir NOP ile benzerlik, aynı değerlerle aynı olduğunu, diğer komutların uyarı kuralını geri almasını, açıklamayı değiştirmesini ve devre dışı bırakmayı ve sonra da bu değişiklikleri sürdürmek için InputObject parametresini kullanmaya benzer</span><span class="sxs-lookup"><span data-stu-id="64368-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="64368-121">Örnek 4: kanaldan RESOURCEID değerini kullanarak etkinlik günlüğü uyarısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="64368-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="64368-122">Verilen günlük uyarısı kuralı varsa bu komut bunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="64368-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="64368-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64368-123">PARAMETERS</span></span>

### <span data-ttu-id="64368-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="64368-124">-Location</span></span>
<span data-ttu-id="64368-125">Etkinlik günlüğü uyarısının bulunacağı konum.</span><span class="sxs-lookup"><span data-stu-id="64368-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="64368-126">-Name</span></span>
<span data-ttu-id="64368-127">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="64368-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64368-128">-ResourceGroupName</span></span>
<span data-ttu-id="64368-129">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="64368-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-130">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="64368-130">-Scope</span></span>
<span data-ttu-id="64368-131">Etkinlik günlüğü uyarısı için kapsamlar listesi.</span><span class="sxs-lookup"><span data-stu-id="64368-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-132">-Koşul</span><span class="sxs-lookup"><span data-stu-id="64368-132">-Condition</span></span>
<span data-ttu-id="64368-133">Etkinlik günlüğü uyarısıyla ilgili koşulların listesi.</span><span class="sxs-lookup"><span data-stu-id="64368-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="64368-134">**Not** : koşullar listesinde, alanın "Kategori" değerine eşit olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="64368-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="64368-135">Bu koşul yoksa, arka uç 400 (BadRequest) ile yanıt verir.</span><span class="sxs-lookup"><span data-stu-id="64368-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-136">-Eylem</span><span class="sxs-lookup"><span data-stu-id="64368-136">-Action</span></span>
<span data-ttu-id="64368-137">Etkinlik günlüğü uyarısı için eylem gruplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="64368-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="64368-138">-DisableAlert</span></span>
<span data-ttu-id="64368-139">Kullanıcının etkinlik günlüğü uyarısını devre dışı olarak oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="64368-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="64368-140">Verilmezse, uyarılar etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="64368-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64368-141">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="64368-141">-Description</span></span>
<span data-ttu-id="64368-142">Uyarı kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="64368-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="64368-143">-Tag</span></span>
<span data-ttu-id="64368-144">Etkinlik günlüğü uyarısı kaynağının Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64368-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64368-145">-InputObject</span></span>
<span data-ttu-id="64368-146">Gerekli adı ve kaynak grubu adı özelliklerini ayıklamak için çağrının InputObject etiketleri özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64368-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-147">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="64368-147">-ResourceId</span></span>
<span data-ttu-id="64368-148">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="64368-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64368-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="64368-149">-Confirm</span></span>
<span data-ttu-id="64368-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="64368-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64368-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64368-151">-DefaultProfile</span></span>
<span data-ttu-id="64368-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64368-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64368-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64368-153">-WhatIf</span></span>
<span data-ttu-id="64368-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="64368-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64368-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="64368-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64368-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64368-156">CommonParameters</span></span>
<span data-ttu-id="64368-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64368-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64368-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64368-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64368-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64368-159">INPUTS</span></span>

## <span data-ttu-id="64368-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64368-160">OUTPUTS</span></span>

### <span data-ttu-id="64368-161">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="64368-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="64368-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64368-162">NOTES</span></span>

## <span data-ttu-id="64368-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64368-163">RELATED LINKS</span></span>

[<span data-ttu-id="64368-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="64368-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="64368-165">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="64368-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="64368-166">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="64368-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="64368-167">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="64368-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="64368-168">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="64368-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="64368-169">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="64368-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
