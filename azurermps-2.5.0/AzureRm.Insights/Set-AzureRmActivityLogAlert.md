---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 993e1b9cde421bad1039f94f4557ee58f781c20b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938860"
---
# <span data-ttu-id="9586a-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9586a-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="9586a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9586a-102">SYNOPSIS</span></span>
<span data-ttu-id="9586a-103">Yeni bir etkinlik günlüğü uyarısını oluşturur veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9586a-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9586a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9586a-104">SYNTAX</span></span>

### <span data-ttu-id="9586a-105">Setbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="9586a-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9586a-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9586a-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9586a-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9586a-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9586a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9586a-108">DESCRIPTION</span></span>
<span data-ttu-id="9586a-109">**Set-AzureRmActivityLogAlert** cmdlet 'i yeni oluşturur veya varolan bir etkinlik günlüğü uyarısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9586a-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="9586a-110">Etiketler, koşullar ve eylemler için, bu çağrıda virgülle ayrılmış olarak, nesnelerin önceden oluşturulması ve parametrelerin parametre olarak geçirilmesi gerekir (aşağıdaki örneğe bakın).</span><span class="sxs-lookup"><span data-stu-id="9586a-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="9586a-111">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten oluşturulması/değiştirilmesi öncesinde kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="9586a-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="9586a-112">**Not** : Bu cmdlet ve ilişkili olanlar kaldırıldı (Kasım 2017) **Add-AzureRmLogAlertRule** yerini alır.</span><span class="sxs-lookup"><span data-stu-id="9586a-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="9586a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9586a-113">EXAMPLES</span></span>

### <span data-ttu-id="9586a-114">Örnek 1: etkinlik günlüğü uyarısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9586a-114">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="9586a-115">İlk dört komut yaprak koşulu ve eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9586a-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="9586a-116">Son komutu koşulu ve eylem grubunu kullanarak etkinlik günlüğü uyarısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9586a-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="9586a-117">Örnek 2: etkinlik günlüğü uyarısı oluşturma devre dışı</span><span class="sxs-lookup"><span data-stu-id="9586a-117">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="9586a-118">İlk dört komut yaprak koşulu ve eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9586a-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="9586a-119">Son komutu koşulu ve eylem grubunu kullanarak etkinlik günlüğü uyarısı oluşturur, ancak uyarıyı devre dışı olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9586a-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="9586a-120">Örnek 3: kanalda veya InputObject parametresinden bir değer kullanarak etkinlik günlüğü uyarısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="9586a-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="9586a-121">İlk komut bir NOP ile benzerlik, aynı değerlerle aynı olduğunu, diğer komutların uyarı kuralını geri almasını, açıklamayı değiştirmesini ve devre dışı bırakmayı ve sonra da bu değişiklikleri sürdürmek için InputObject parametresini kullanmaya benzer</span><span class="sxs-lookup"><span data-stu-id="9586a-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="9586a-122">Örnek 4: kanaldan RESOURCEID değerini kullanarak etkinlik günlüğü uyarısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="9586a-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="9586a-123">Verilen günlük uyarısı kuralı varsa bu komut bunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9586a-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="9586a-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9586a-124">PARAMETERS</span></span>

### <span data-ttu-id="9586a-125">-Eylem</span><span class="sxs-lookup"><span data-stu-id="9586a-125">-Action</span></span>
<span data-ttu-id="9586a-126">Etkinlik günlüğü uyarısı için eylem gruplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="9586a-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="9586a-127">-Koşul</span><span class="sxs-lookup"><span data-stu-id="9586a-127">-Condition</span></span>
<span data-ttu-id="9586a-128">Etkinlik günlüğü uyarısıyla ilgili koşulların listesi.</span><span class="sxs-lookup"><span data-stu-id="9586a-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="9586a-129">**Not** : koşullar listesinde, alanın "Kategori" değerine eşit olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9586a-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="9586a-130">Bu koşul yoksa, arka uç 400 (BadRequest) ile yanıt verir.</span><span class="sxs-lookup"><span data-stu-id="9586a-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="9586a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9586a-131">-DefaultProfile</span></span>
<span data-ttu-id="9586a-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9586a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9586a-133">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9586a-133">-Description</span></span>
<span data-ttu-id="9586a-134">Uyarı kaynağının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9586a-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586a-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="9586a-135">-DisableAlert</span></span>
<span data-ttu-id="9586a-136">Kullanıcının etkinlik günlüğü uyarısını devre dışı olarak oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9586a-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="9586a-137">Verilmezse, uyarılar etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9586a-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9586a-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9586a-138">-InputObject</span></span>
<span data-ttu-id="9586a-139">Gerekli adı ve kaynak grubu adı özelliklerini ayıklamak için çağrının InputObject etiketleri özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9586a-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9586a-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="9586a-140">-Location</span></span>
<span data-ttu-id="9586a-141">Etkinlik günlüğü uyarısının bulunacağı konum.</span><span class="sxs-lookup"><span data-stu-id="9586a-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586a-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="9586a-142">-Name</span></span>
<span data-ttu-id="9586a-143">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="9586a-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9586a-144">-ResourceGroupName</span></span>
<span data-ttu-id="9586a-145">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9586a-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586a-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9586a-146">-ResourceId</span></span>
<span data-ttu-id="9586a-147">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="9586a-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586a-148">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="9586a-148">-Scope</span></span>
<span data-ttu-id="9586a-149">Etkinlik günlüğü uyarısı için kapsamlar listesi.</span><span class="sxs-lookup"><span data-stu-id="9586a-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="9586a-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9586a-150">-Tag</span></span>
<span data-ttu-id="9586a-151">Etkinlik günlüğü uyarısı kaynağının Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9586a-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="9586a-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="9586a-152">-Confirm</span></span>
<span data-ttu-id="9586a-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9586a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9586a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9586a-154">-WhatIf</span></span>
<span data-ttu-id="9586a-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9586a-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9586a-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9586a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9586a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9586a-157">CommonParameters</span></span>
<span data-ttu-id="9586a-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9586a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9586a-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9586a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9586a-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9586a-160">INPUTS</span></span>

### <span data-ttu-id="9586a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9586a-161">System.String</span></span>

### <span data-ttu-id="9586a-162">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9586a-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9586a-163">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. model. Activitygünlükalertleafcondition, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9586a-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9586a-164">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertActionGroup, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9586a-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9586a-165">System. Koleksiyonlar. Generic. Dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9586a-165">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9586a-166">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="9586a-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="9586a-167">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9586a-167">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9586a-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9586a-168">OUTPUTS</span></span>

### <span data-ttu-id="9586a-169">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="9586a-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="9586a-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9586a-170">NOTES</span></span>

## <span data-ttu-id="9586a-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9586a-171">RELATED LINKS</span></span>

[<span data-ttu-id="9586a-172">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9586a-172">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9586a-173">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9586a-173">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9586a-174">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9586a-174">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9586a-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9586a-175">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9586a-176">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9586a-176">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="9586a-177">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9586a-177">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
