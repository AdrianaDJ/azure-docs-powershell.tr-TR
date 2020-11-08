---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: 894a52d5dba7e5d2d0ce129c471b64fdb7fd831e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103601"
---
# <span data-ttu-id="d1687-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d1687-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="d1687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1687-102">SYNOPSIS</span></span>
<span data-ttu-id="d1687-103">Otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1687-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="d1687-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1687-104">SYNTAX</span></span>

### <span data-ttu-id="d1687-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d1687-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1687-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d1687-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1687-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1687-107">DESCRIPTION</span></span>
<span data-ttu-id="d1687-108">**Add-AzAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1687-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="d1687-109">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="d1687-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d1687-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1687-110">EXAMPLES</span></span>

### <span data-ttu-id="d1687-111">Örnek 1: otomatik ölçeklendirme ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d1687-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="d1687-112">İlk iki komut New-AzAutoscaleRule kullanarak iki otomatik ölçeklendirme kuralı, $Rule 1 ve $Rule 2 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1687-112">The first two commands use New-AzAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="d1687-113">Üçüncü ve dördüncü komutlarda, $Rule 1 ve $Rule 2 kullanarak otomatik ölçeklendirme profilleri, $Profile 1 ve $Profile 2 kullanarak New-AzAutoscaleProfile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d1687-113">The third and fourth commands use New-AzAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="d1687-114">Son komutu $Profile 1 ve $Profile 2 ' deki profilleri kullanarak otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1687-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="d1687-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1687-115">PARAMETERS</span></span>

### <span data-ttu-id="d1687-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="d1687-116">-AutoscaleProfile</span></span>
<span data-ttu-id="d1687-117">Otomatik ölçeklendirme ayarına eklenecek profillerin listesini belirtir veya profil eklemek için $Null.</span><span class="sxs-lookup"><span data-stu-id="d1687-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="d1687-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1687-118">-DefaultProfile</span></span>
<span data-ttu-id="d1687-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d1687-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1687-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="d1687-120">-DisableSetting</span></span>
<span data-ttu-id="d1687-121">Varolan bir otomatik ölçeklendirme ayarını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d1687-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="d1687-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1687-122">-InputObject</span></span>
<span data-ttu-id="d1687-123">Otomatik ölçek ayarının tam özelliği</span><span class="sxs-lookup"><span data-stu-id="d1687-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="d1687-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="d1687-124">-Location</span></span>
<span data-ttu-id="d1687-125">Otomatik ölçeklendirme ayarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1687-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="d1687-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1687-126">-Name</span></span>
<span data-ttu-id="d1687-127">Oluşturulacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1687-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="d1687-128">-Bildirim</span><span class="sxs-lookup"><span data-stu-id="d1687-128">-Notification</span></span>
<span data-ttu-id="d1687-129">Virgülle ayrılmış bildirimlerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1687-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="d1687-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1687-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1687-131">Otomatik ölçeklendirme ayarıyla ilişkili kaynak için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1687-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="d1687-132">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="d1687-132">-TargetResourceId</span></span>
<span data-ttu-id="d1687-133">Otomatik ölçeklendirme için kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1687-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="d1687-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1687-134">-Confirm</span></span>
<span data-ttu-id="d1687-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1687-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1687-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1687-136">-WhatIf</span></span>
<span data-ttu-id="d1687-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1687-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1687-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1687-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1687-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1687-139">CommonParameters</span></span>
<span data-ttu-id="d1687-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1687-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1687-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d1687-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1687-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1687-142">INPUTS</span></span>

### <span data-ttu-id="d1687-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d1687-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="d1687-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d1687-144">System.String</span></span>

### <span data-ttu-id="d1687-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1687-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d1687-146">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleProfile, Microsoft. Azure. PowerShell. cmdlet. Monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d1687-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d1687-147">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleNotification, Microsoft. Azure. PowerShell. cmdlet. Monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d1687-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d1687-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1687-148">OUTPUTS</span></span>

### <span data-ttu-id="d1687-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d1687-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="d1687-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1687-150">NOTES</span></span>

## <span data-ttu-id="d1687-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1687-151">RELATED LINKS</span></span>

[<span data-ttu-id="d1687-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d1687-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="d1687-153">Yeni-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="d1687-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="d1687-154">Yeni-Azotomobil</span><span class="sxs-lookup"><span data-stu-id="d1687-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="d1687-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d1687-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


