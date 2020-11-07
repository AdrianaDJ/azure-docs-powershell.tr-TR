---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a24b5e5d4cce1e33536b7977590add11a6d7cb39
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936759"
---
# <span data-ttu-id="5f3c6-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5f3c6-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5f3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3c6-103">Cihazda bir tetik yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="5f3c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f3c6-104">SYNTAX</span></span>

### <span data-ttu-id="5f3c6-105">FileEventTriggerParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f3c6-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f3c6-106">Dönemtimertriggerparameterset</span><span class="sxs-lookup"><span data-stu-id="5f3c6-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f3c6-107">Fileeventtriggerresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5f3c6-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f3c6-108">Dönemtimertriggerresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5f3c6-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f3c6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f3c6-109">DESCRIPTION</span></span>
<span data-ttu-id="5f3c6-110">**New-AzDataBoxEdgeTrigger** cmdlet 'ı, veri kutusu Edge cihazında bir tetik yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="5f3c6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f3c6-111">EXAMPLES</span></span>

### <span data-ttu-id="5f3c6-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f3c6-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="5f3c6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f3c6-113">PARAMETERS</span></span>

### <span data-ttu-id="5f3c6-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="5f3c6-114">-AsJob</span></span>
<span data-ttu-id="5f3c6-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5f3c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f3c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f3c6-116">-DefaultProfile</span></span>
<span data-ttu-id="5f3c6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f3c6-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="5f3c6-118">-DeviceName</span></span>
<span data-ttu-id="5f3c6-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="5f3c6-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="5f3c6-120">-FileEvent</span></span>
<span data-ttu-id="5f3c6-121">FileEvent tetikleyicisini yapılandırmak için bu Switch parametresini iletin</span><span class="sxs-lookup"><span data-stu-id="5f3c6-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f3c6-122">-Name</span></span>
<span data-ttu-id="5f3c6-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="5f3c6-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-124">-Dönembir TimerEvent</span><span class="sxs-lookup"><span data-stu-id="5f3c6-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="5f3c6-125">Bu Switch parametresini, Dönemtimerevent tetikleyicisini yapılandırmak için geçir</span><span class="sxs-lookup"><span data-stu-id="5f3c6-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f3c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="5f3c6-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5f3c6-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="5f3c6-128">-RoleName</span></span>
<span data-ttu-id="5f3c6-129">Hangi olayların yükseltilecektir rol.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-130">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="5f3c6-130">-Schedule</span></span>
<span data-ttu-id="5f3c6-131">Süreölçer olayının oluşturulması gereken dönemsel sıklık.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="5f3c6-132">Gün (1 ve 365 arasında), saat (1 ile 23 arasında) veya dakika (1 ile 59 arasında) arasında bir zamanlama belirtin.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-133">-Shareıd</span><span class="sxs-lookup"><span data-stu-id="5f3c6-133">-ShareId</span></span>
<span data-ttu-id="5f3c6-134">Dosya olay tetikleyicisinde geçirilecek dosya paylaşımı KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="5f3c6-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-135">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="5f3c6-135">-ShareName</span></span>
<span data-ttu-id="5f3c6-136">Dosya olay tetikleyicisinde geçirilecek dosya paylaşımı KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="5f3c6-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-137">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="5f3c6-137">-StartTime</span></span>
<span data-ttu-id="5f3c6-138">Geçerli tetik sonucu veren günün saati.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="5f3c6-139">Zamanlama, saniye ile belirtilen zamanın başvurusuyla hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="5f3c6-140">Saat dilimi belirtilmezse, süre Device saat diliminde olduğu kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="5f3c6-141">Değer her zaman UTC saati olarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-142">-Konu</span><span class="sxs-lookup"><span data-stu-id="5f3c6-142">-Topic</span></span>
<span data-ttu-id="5f3c6-143">Dönemsel olayların IoT cihazında yayımlandığı konu.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3c6-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f3c6-144">-Confirm</span></span>
<span data-ttu-id="5f3c6-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f3c6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f3c6-146">-WhatIf</span></span>
<span data-ttu-id="5f3c6-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f3c6-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f3c6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f3c6-149">CommonParameters</span></span>
<span data-ttu-id="5f3c6-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f3c6-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f3c6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f3c6-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f3c6-152">INPUTS</span></span>

### <span data-ttu-id="5f3c6-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f3c6-153">None</span></span>

## <span data-ttu-id="5f3c6-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f3c6-154">OUTPUTS</span></span>

### <span data-ttu-id="5f3c6-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5f3c6-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5f3c6-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f3c6-156">NOTES</span></span>

## <span data-ttu-id="5f3c6-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f3c6-157">RELATED LINKS</span></span>
