---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764833"
---
# <span data-ttu-id="d5393-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d5393-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="d5393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5393-102">SYNOPSIS</span></span>
<span data-ttu-id="d5393-103">Otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5393-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5393-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5393-104">SYNTAX</span></span>

### <span data-ttu-id="d5393-105">Güncelleştirme semantiğinin Add-AzureRmAutoscaleSetting cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="d5393-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5393-106">Oluşturma semantiğinin Add-AzureRmAutoscaleSetting cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="d5393-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5393-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5393-107">DESCRIPTION</span></span>
<span data-ttu-id="d5393-108">**Add-AzureRmAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5393-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="d5393-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5393-109">EXAMPLES</span></span>

### <span data-ttu-id="d5393-110">Örnek 1: otomatik ölçeklendirme ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5393-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="d5393-111">İlk iki komut New-AzureRmAutoscaleRule kullanarak iki otomatik ölçeklendirme kuralı, $Rule 1 ve $Rule 2 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5393-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="d5393-112">Üçüncü ve dördüncü komutlarda, $Rule 1 ve $Rule 2 kullanarak otomatik ölçeklendirme profilleri, $Profile 1 ve $Profile 2 kullanarak New-AzureRmAutoscaleProfile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d5393-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="d5393-113">Son komutu $Profile 1 ve $Profile 2 ' deki profilleri kullanarak otomatik ölçeklendirme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5393-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="d5393-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5393-114">PARAMETERS</span></span>

### <span data-ttu-id="d5393-115">-Otomatik ölçek profilleri</span><span class="sxs-lookup"><span data-stu-id="d5393-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="d5393-116">Otomatik ölçeklendirme ayarına eklenecek profillerin listesini belirtir veya profil eklemek için $Null.</span><span class="sxs-lookup"><span data-stu-id="d5393-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="d5393-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="d5393-117">-DisableSetting</span></span>
<span data-ttu-id="d5393-118">Varolan bir otomatik ölçeklendirme ayarını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d5393-118">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="d5393-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="d5393-119">-Location</span></span>
<span data-ttu-id="d5393-120">Otomatik ölçeklendirme ayarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5393-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5393-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5393-121">-Name</span></span>
<span data-ttu-id="d5393-122">Oluşturulacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5393-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5393-123">-Bildirimler</span><span class="sxs-lookup"><span data-stu-id="d5393-123">-Notifications</span></span>
<span data-ttu-id="d5393-124">Virgülle ayrılmış bildirimlerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5393-124">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="d5393-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d5393-125">-ResourceGroup</span></span>
<span data-ttu-id="d5393-126">Otomatik ölçeklendirme ayarıyla ilişkili kaynak için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5393-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5393-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="d5393-127">-SettingSpec</span></span>
<span data-ttu-id="d5393-128">Bir **Otomatik ölçek ayarı** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5393-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="d5393-129">**Otomatik ölçek ayarı** nesnesi almak için Get-AzureRmAutoscaleSetting cmdlet 'ini kullanabilir veya Windows PowerShell betiği içinde bir tane oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5393-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5393-130">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="d5393-130">-TargetResourceId</span></span>
<span data-ttu-id="d5393-131">Otomatik ölçeklendirme için kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5393-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5393-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5393-132">-DefaultProfile</span></span>
<span data-ttu-id="d5393-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5393-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5393-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5393-134">CommonParameters</span></span>
<span data-ttu-id="d5393-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5393-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5393-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5393-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5393-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5393-137">INPUTS</span></span>

## <span data-ttu-id="d5393-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5393-138">OUTPUTS</span></span>

### <span data-ttu-id="d5393-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d5393-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="d5393-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5393-140">NOTES</span></span>

## <span data-ttu-id="d5393-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5393-141">RELATED LINKS</span></span>

[<span data-ttu-id="d5393-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d5393-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="d5393-143">Yeni-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="d5393-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="d5393-144">Yeni-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="d5393-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="d5393-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d5393-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


