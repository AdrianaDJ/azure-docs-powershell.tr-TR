---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106191"
---
# <span data-ttu-id="2424c-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="2424c-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="2424c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2424c-102">SYNOPSIS</span></span>
<span data-ttu-id="2424c-103">Sanal makine otomatik düzeltme eki için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2424c-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="2424c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2424c-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2424c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2424c-105">DESCRIPTION</span></span>
<span data-ttu-id="2424c-106">**New-AzureVMSqlServerAutoPatchingConfig** cmdlet 'i, sanal makine otomatik düzeltme eki için bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2424c-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="2424c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2424c-107">EXAMPLES</span></span>

### <span data-ttu-id="2424c-108">Örnek 1: otomatik düzeltme 'yi yapılandırmak için yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2424c-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="2424c-109">Bu komut, set-AzureVMSqlServerExtension kullanarak otomatik düzeltme eki yapılandırmak için kullanılabilecek yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2424c-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="2424c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2424c-110">PARAMETERS</span></span>

### <span data-ttu-id="2424c-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="2424c-111">-DayOfWeek</span></span>
<span data-ttu-id="2424c-112">Güncelleştirmelerin yüklenmesi gereken haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2424c-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="2424c-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2424c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2424c-114">Gününü</span><span class="sxs-lookup"><span data-stu-id="2424c-114">Sunday</span></span>
- <span data-ttu-id="2424c-115">Den</span><span class="sxs-lookup"><span data-stu-id="2424c-115">Monday</span></span>
- <span data-ttu-id="2424c-116">Salı</span><span class="sxs-lookup"><span data-stu-id="2424c-116">Tuesday</span></span>
- <span data-ttu-id="2424c-117">Günü</span><span class="sxs-lookup"><span data-stu-id="2424c-117">Wednesday</span></span>
- <span data-ttu-id="2424c-118">Per</span><span class="sxs-lookup"><span data-stu-id="2424c-118">Thursday</span></span>
- <span data-ttu-id="2424c-119">Cuma</span><span class="sxs-lookup"><span data-stu-id="2424c-119">Friday</span></span>
- <span data-ttu-id="2424c-120">Günü</span><span class="sxs-lookup"><span data-stu-id="2424c-120">Saturday</span></span>
- <span data-ttu-id="2424c-121">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="2424c-121">Everyday</span></span>

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

### <span data-ttu-id="2424c-122">-Enable</span><span class="sxs-lookup"><span data-stu-id="2424c-122">-Enable</span></span>
<span data-ttu-id="2424c-123">Sanal makine için otomatik düzeltme özelliğinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2424c-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="2424c-124">Otomatik Düzeltme 'yi etkinleştirirseniz cmdlet Windows güncelleştirmesini etkileşimli moda koyar.</span><span class="sxs-lookup"><span data-stu-id="2424c-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="2424c-125">Otomatik Düzeltme ekini devre dışı bırakırsanız, Windows Update ayarları değişmez.</span><span class="sxs-lookup"><span data-stu-id="2424c-125">If you disable automated patching, Windows Update settings will not change.</span></span>

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

### <span data-ttu-id="2424c-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2424c-126">-InformationAction</span></span>
<span data-ttu-id="2424c-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2424c-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2424c-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2424c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2424c-129">'A</span><span class="sxs-lookup"><span data-stu-id="2424c-129">Continue</span></span>
- <span data-ttu-id="2424c-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="2424c-130">Ignore</span></span>
- <span data-ttu-id="2424c-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="2424c-131">Inquire</span></span>
- <span data-ttu-id="2424c-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="2424c-132">SilentlyContinue</span></span>
- <span data-ttu-id="2424c-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="2424c-133">Stop</span></span>
- <span data-ttu-id="2424c-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="2424c-134">Suspend</span></span>

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

### <span data-ttu-id="2424c-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="2424c-135">-InformationVariable</span></span>
<span data-ttu-id="2424c-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2424c-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2424c-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="2424c-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="2424c-138">Bakım penceresinin süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2424c-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="2424c-139">Otomatik Düzeltme Eki, bu pencerenin dışında bir sanal makine kullanılabilirliğini etkileyebilecek bir eylem gerçekleştirmekten kaçınacaktır.</span><span class="sxs-lookup"><span data-stu-id="2424c-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="2424c-140">Yalnızca 30 dakikalık artış vardır.</span><span class="sxs-lookup"><span data-stu-id="2424c-140">Only 30 minutes increments are allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2424c-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="2424c-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="2424c-142">Bakım penceresinin başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2424c-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="2424c-143">Bu kez, güncelleştirmelerin yüklenmeye başlaması ve saate yuvarlanacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2424c-143">This time defines when updates start installing and is rounded to the hour.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2424c-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="2424c-144">-PatchCategory</span></span>
<span data-ttu-id="2424c-145">Önemli güncelleştirmelerin dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2424c-145">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="2424c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2424c-146">CommonParameters</span></span>
<span data-ttu-id="2424c-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2424c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2424c-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2424c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2424c-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2424c-149">INPUTS</span></span>

## <span data-ttu-id="2424c-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2424c-150">OUTPUTS</span></span>

### <span data-ttu-id="2424c-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="2424c-151">AutoPatchingSettings</span></span>
<span data-ttu-id="2424c-152">Bu cmdlet, otomatik düzeltme için ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="2424c-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="2424c-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2424c-153">NOTES</span></span>

## <span data-ttu-id="2424c-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2424c-154">RELATED LINKS</span></span>

[<span data-ttu-id="2424c-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2424c-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="2424c-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2424c-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="2424c-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2424c-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


