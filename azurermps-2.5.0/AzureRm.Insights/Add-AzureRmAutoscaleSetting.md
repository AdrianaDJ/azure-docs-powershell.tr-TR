---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 8025c68c7fcaf2e7757cc81718636785bd62a19b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940152"
---
# <span data-ttu-id="b3894-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3894-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="b3894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3894-102">SYNOPSIS</span></span>
<span data-ttu-id="b3894-103">Otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3894-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3894-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3894-104">SYNTAX</span></span>

### <span data-ttu-id="b3894-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3894-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3894-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3894-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3894-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3894-107">DESCRIPTION</span></span>
<span data-ttu-id="b3894-108">**Add-AzureRmAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3894-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="b3894-109">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="b3894-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b3894-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3894-110">EXAMPLES</span></span>

### <span data-ttu-id="b3894-111">Örnek 1: otomatik ölçeklendirme ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b3894-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="b3894-112">İlk iki komut New-AzureRmAutoscaleRule kullanarak iki otomatik ölçeklendirme kuralı, $Rule 1 ve $Rule 2 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3894-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="b3894-113">Üçüncü ve dördüncü komutlarda, $Rule 1 ve $Rule 2 kullanarak otomatik ölçeklendirme profilleri, $Profile 1 ve $Profile 2 kullanarak New-AzureRmAutoscaleProfile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b3894-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="b3894-114">Son komutu $Profile 1 ve $Profile 2 ' deki profilleri kullanarak otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3894-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="b3894-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3894-115">PARAMETERS</span></span>

### <span data-ttu-id="b3894-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b3894-116">-AutoscaleProfile</span></span>
<span data-ttu-id="b3894-117">Otomatik ölçeklendirme ayarına eklenecek profillerin listesini belirtir veya profil eklemek için $Null.</span><span class="sxs-lookup"><span data-stu-id="b3894-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3894-118">-DefaultProfile</span></span>
<span data-ttu-id="b3894-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3894-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3894-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="b3894-120">-DisableSetting</span></span>
<span data-ttu-id="b3894-121">Varolan bir otomatik ölçeklendirme ayarını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="b3894-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3894-122">-InputObject</span></span>
<span data-ttu-id="b3894-123">Otomatik ölçek ayarının tam özelliği</span><span class="sxs-lookup"><span data-stu-id="b3894-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="b3894-124">-Location</span></span>
<span data-ttu-id="b3894-125">Otomatik ölçeklendirme ayarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3894-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3894-126">-Name</span></span>
<span data-ttu-id="b3894-127">Oluşturulacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3894-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-128">-Bildirim</span><span class="sxs-lookup"><span data-stu-id="b3894-128">-Notification</span></span>
<span data-ttu-id="b3894-129">Virgülle ayrılmış bildirimlerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3894-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3894-130">-ResourceGroupName</span></span>
<span data-ttu-id="b3894-131">Otomatik ölçeklendirme ayarıyla ilişkili kaynak için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3894-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-132">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="b3894-132">-TargetResourceId</span></span>
<span data-ttu-id="b3894-133">Otomatik ölçeklendirme için kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3894-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3894-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3894-134">-Confirm</span></span>
<span data-ttu-id="b3894-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3894-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3894-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3894-136">-WhatIf</span></span>
<span data-ttu-id="b3894-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3894-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3894-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3894-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3894-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3894-139">CommonParameters</span></span>
<span data-ttu-id="b3894-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3894-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3894-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3894-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3894-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3894-142">INPUTS</span></span>

### <span data-ttu-id="b3894-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3894-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="b3894-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b3894-144">System.String</span></span>

### <span data-ttu-id="b3894-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3894-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b3894-146">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleProfile, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b3894-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b3894-147">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleNotification, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b3894-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b3894-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3894-148">OUTPUTS</span></span>

### <span data-ttu-id="b3894-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b3894-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="b3894-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3894-150">NOTES</span></span>

## <span data-ttu-id="b3894-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3894-151">RELATED LINKS</span></span>

[<span data-ttu-id="b3894-152">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3894-152">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="b3894-153">Yeni-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b3894-153">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="b3894-154">Yeni-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="b3894-154">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="b3894-155">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3894-155">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


