---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 66c127e701432604654cacb556d71588d9786dbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587552"
---
# <span data-ttu-id="76e98-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="76e98-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="76e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e98-102">SYNOPSIS</span></span>
<span data-ttu-id="76e98-103">Yeni bir etkinlik günlüğü uyarısını oluşturur veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="76e98-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76e98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76e98-104">SYNTAX</span></span>

### <span data-ttu-id="76e98-105">Setbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="76e98-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e98-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="76e98-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e98-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="76e98-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76e98-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="76e98-108">DESCRIPTION</span></span>
<span data-ttu-id="76e98-109">**Set-AzureRmActivityLogAlert** cmdlet 'i yeni oluşturur veya varolan bir etkinlik günlüğü uyarısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="76e98-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="76e98-110">Etiketler, koşullar ve eylemler için, bu çağrıda virgülle ayrılmış olarak, nesnelerin önceden oluşturulması ve parametrelerin parametre olarak geçirilmesi gerekir (aşağıdaki örneğe bakın).</span><span class="sxs-lookup"><span data-stu-id="76e98-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="76e98-111">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten oluşturulması/değiştirilmesi öncesinde kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="76e98-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

<span data-ttu-id="76e98-112">**Not** : Bu cmdlet ve ilişkili olanlar kaldırıldı (Kasım 2017) **Add-AzureRmLogAlertRule** yerini alır.</span><span class="sxs-lookup"><span data-stu-id="76e98-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="76e98-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76e98-113">EXAMPLES</span></span>

### <span data-ttu-id="76e98-114">Örnek 1: etkinlik günlüğü uyarısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="76e98-114">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="76e98-115">İlk dört komut yaprak koşulu ve eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76e98-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="76e98-116">Son komutu koşulu ve eylem grubunu kullanarak etkinlik günlüğü uyarısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76e98-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="76e98-117">Örnek 2: etkinlik günlüğü uyarısı oluşturma devre dışı</span><span class="sxs-lookup"><span data-stu-id="76e98-117">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="76e98-118">İlk dört komut yaprak koşulu ve eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76e98-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="76e98-119">Son komutu koşulu ve eylem grubunu kullanarak etkinlik günlüğü uyarısı oluşturur, ancak uyarıyı devre dışı olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76e98-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="76e98-120">Örnek 3: kanalda veya InputObject parametresinden bir değer kullanarak etkinlik günlüğü uyarısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="76e98-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="76e98-121">İlk komut bir NOP ile benzerlik, aynı değerlerle aynı olduğunu, diğer komutların uyarı kuralını geri almasını, açıklamayı değiştirmesini ve devre dışı bırakmayı ve sonra da bu değişiklikleri sürdürmek için InputObject parametresini kullanmaya benzer</span><span class="sxs-lookup"><span data-stu-id="76e98-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="76e98-122">Örnek 4: kanaldan RESOURCEID değerini kullanarak etkinlik günlüğü uyarısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="76e98-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="76e98-123">Verilen günlük uyarısı kuralı varsa bu komut bunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="76e98-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="76e98-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76e98-124">PARAMETERS</span></span>

### <span data-ttu-id="76e98-125">-Eylem</span><span class="sxs-lookup"><span data-stu-id="76e98-125">-Action</span></span>
<span data-ttu-id="76e98-126">Etkinlik günlüğü uyarısı için eylem gruplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="76e98-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-127">-Koşul</span><span class="sxs-lookup"><span data-stu-id="76e98-127">-Condition</span></span>
<span data-ttu-id="76e98-128">Etkinlik günlüğü uyarısıyla ilgili koşulların listesi.</span><span class="sxs-lookup"><span data-stu-id="76e98-128">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="76e98-129">**Not** : koşullar listesinde, alanın "Kategori" değerine eşit olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="76e98-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="76e98-130">Bu koşul yoksa, arka uç 400 (BadRequest) ile yanıt verir.</span><span class="sxs-lookup"><span data-stu-id="76e98-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e98-131">-DefaultProfile</span></span>
<span data-ttu-id="76e98-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="76e98-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76e98-133">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="76e98-133">-Description</span></span>
<span data-ttu-id="76e98-134">Uyarı kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="76e98-134">The description of the alert resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="76e98-135">-DisableAlert</span></span>
<span data-ttu-id="76e98-136">Kullanıcının etkinlik günlüğü uyarısını devre dışı olarak oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="76e98-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="76e98-137">Verilmezse, uyarılar etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="76e98-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76e98-138">-InputObject</span></span>
<span data-ttu-id="76e98-139">Gerekli adı ve kaynak grubu adı özelliklerini ayıklamak için çağrının InputObject etiketleri özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="76e98-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="76e98-140">-Location</span></span>
<span data-ttu-id="76e98-141">Etkinlik günlüğü uyarısının bulunacağı konum.</span><span class="sxs-lookup"><span data-stu-id="76e98-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="76e98-142">-Name</span></span>
<span data-ttu-id="76e98-143">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="76e98-143">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e98-144">-ResourceGroupName</span></span>
<span data-ttu-id="76e98-145">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="76e98-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="76e98-146">-ResourceId</span></span>
<span data-ttu-id="76e98-147">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="76e98-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-148">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="76e98-148">-Scope</span></span>
<span data-ttu-id="76e98-149">Etkinlik günlüğü uyarısı için kapsamlar listesi.</span><span class="sxs-lookup"><span data-stu-id="76e98-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="76e98-150">-Tag</span></span>
<span data-ttu-id="76e98-151">Etkinlik günlüğü uyarısı kaynağının Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="76e98-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="76e98-152">-Confirm</span></span>
<span data-ttu-id="76e98-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76e98-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76e98-154">-WhatIf</span></span>
<span data-ttu-id="76e98-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76e98-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76e98-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76e98-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e98-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e98-157">CommonParameters</span></span>
<span data-ttu-id="76e98-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76e98-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e98-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e98-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e98-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76e98-160">INPUTS</span></span>

### <span data-ttu-id="76e98-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76e98-161">None</span></span>
<span data-ttu-id="76e98-162">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="76e98-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76e98-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76e98-163">OUTPUTS</span></span>

### <span data-ttu-id="76e98-164">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="76e98-164">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="76e98-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76e98-165">NOTES</span></span>

## <span data-ttu-id="76e98-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76e98-166">RELATED LINKS</span></span>

[<span data-ttu-id="76e98-167">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="76e98-167">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="76e98-168">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="76e98-168">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="76e98-169">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="76e98-169">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="76e98-170">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="76e98-170">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="76e98-171">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="76e98-171">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="76e98-172">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="76e98-172">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
