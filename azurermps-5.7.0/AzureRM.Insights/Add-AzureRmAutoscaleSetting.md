---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 08e7558bb357c930749cf4a93bfa428560c64395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594480"
---
# <span data-ttu-id="156cd-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="156cd-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="156cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156cd-102">SYNOPSIS</span></span>
<span data-ttu-id="156cd-103">Otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="156cd-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="156cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="156cd-104">SYNTAX</span></span>

### <span data-ttu-id="156cd-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="156cd-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="156cd-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="156cd-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="156cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="156cd-107">DESCRIPTION</span></span>
<span data-ttu-id="156cd-108">**Add-AzureRmAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="156cd-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

<span data-ttu-id="156cd-109">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="156cd-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="156cd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="156cd-110">EXAMPLES</span></span>

### <span data-ttu-id="156cd-111">Örnek 1: otomatik ölçeklendirme ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="156cd-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="156cd-112">İlk iki komut New-AzureRmAutoscaleRule kullanarak iki otomatik ölçeklendirme kuralı, $Rule 1 ve $Rule 2 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="156cd-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="156cd-113">Üçüncü ve dördüncü komutlarda, $Rule 1 ve $Rule 2 kullanarak otomatik ölçeklendirme profilleri, $Profile 1 ve $Profile 2 kullanarak New-AzureRmAutoscaleProfile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="156cd-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="156cd-114">Son komutu $Profile 1 ve $Profile 2 ' deki profilleri kullanarak otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="156cd-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="156cd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="156cd-115">PARAMETERS</span></span>

### <span data-ttu-id="156cd-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="156cd-116">-AutoscaleProfile</span></span>
<span data-ttu-id="156cd-117">Otomatik ölçeklendirme ayarına eklenecek profillerin listesini belirtir veya profil eklemek için $Null.</span><span class="sxs-lookup"><span data-stu-id="156cd-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: AutoscaleProfiles

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156cd-118">-DefaultProfile</span></span>
<span data-ttu-id="156cd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="156cd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="156cd-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="156cd-120">-DisableSetting</span></span>
<span data-ttu-id="156cd-121">Varolan bir otomatik ölçeklendirme ayarını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="156cd-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="156cd-122">-Location</span></span>
<span data-ttu-id="156cd-123">Otomatik ölçeklendirme ayarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="156cd-123">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="156cd-124">-Name</span></span>
<span data-ttu-id="156cd-125">Oluşturulacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="156cd-125">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-126">-Bildirim</span><span class="sxs-lookup"><span data-stu-id="156cd-126">-Notification</span></span>
<span data-ttu-id="156cd-127">Virgülle ayrılmış bildirimlerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="156cd-127">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: Notifications

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156cd-128">-ResourceGroupName</span></span>
<span data-ttu-id="156cd-129">Otomatik ölçeklendirme ayarıyla ilişkili kaynak için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="156cd-129">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-130">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="156cd-130">-SettingSpec</span></span>
<span data-ttu-id="156cd-131">Bir **Otomatik ölçek ayarı** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="156cd-131">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="156cd-132">**Otomatik ölçek ayarı** nesnesi almak için Get-AzureRmAutoscaleSetting cmdlet 'ini kullanabilir veya Windows PowerShell betiği içinde bir tane oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="156cd-132">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-133">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="156cd-133">-TargetResourceId</span></span>
<span data-ttu-id="156cd-134">Otomatik ölçeklendirme için kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="156cd-134">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156cd-135">CommonParameters</span></span>
<span data-ttu-id="156cd-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="156cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156cd-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156cd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156cd-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="156cd-138">INPUTS</span></span>

### <span data-ttu-id="156cd-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="156cd-139">None</span></span>
<span data-ttu-id="156cd-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="156cd-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="156cd-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="156cd-141">OUTPUTS</span></span>

### <span data-ttu-id="156cd-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="156cd-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="156cd-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="156cd-143">NOTES</span></span>

## <span data-ttu-id="156cd-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="156cd-144">RELATED LINKS</span></span>

[<span data-ttu-id="156cd-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="156cd-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="156cd-146">Yeni-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="156cd-146">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="156cd-147">Yeni-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="156cd-147">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="156cd-148">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="156cd-148">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


