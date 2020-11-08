---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275167"
---
# <span data-ttu-id="b9e2a-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b9e2a-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="b9e2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e2a-103">Cihazda bir tetik yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="b9e2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9e2a-104">SYNTAX</span></span>

### <span data-ttu-id="b9e2a-105">FileEventTriggerParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b9e2a-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9e2a-106">Dönemtimertriggerparameterset</span><span class="sxs-lookup"><span data-stu-id="b9e2a-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e2a-107">Fileeventtriggerresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b9e2a-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e2a-108">Dönemtimertriggerresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b9e2a-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e2a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9e2a-109">DESCRIPTION</span></span>
<span data-ttu-id="b9e2a-110">**New-AzStackEdgeTrigger** cmdlet 'ı yığın uç cihazında bir tetik yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="b9e2a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9e2a-111">EXAMPLES</span></span>

### <span data-ttu-id="b9e2a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9e2a-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="b9e2a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9e2a-113">PARAMETERS</span></span>

### <span data-ttu-id="b9e2a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b9e2a-114">-AsJob</span></span>
<span data-ttu-id="b9e2a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b9e2a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9e2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e2a-116">-DefaultProfile</span></span>
<span data-ttu-id="b9e2a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e2a-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="b9e2a-118">-DeviceName</span></span>
<span data-ttu-id="b9e2a-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="b9e2a-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e2a-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="b9e2a-120">-FileEvent</span></span>
<span data-ttu-id="b9e2a-121">FileEvent tetikleyicisini yapılandırmak için bu Switch parametresini iletin</span><span class="sxs-lookup"><span data-stu-id="b9e2a-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="b9e2a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9e2a-122">-Name</span></span>
<span data-ttu-id="b9e2a-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="b9e2a-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e2a-124">-Dönembir TimerEvent</span><span class="sxs-lookup"><span data-stu-id="b9e2a-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="b9e2a-125">Bu Switch parametresini, Dönemtimerevent tetikleyicisini yapılandırmak için geçir</span><span class="sxs-lookup"><span data-stu-id="b9e2a-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="b9e2a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e2a-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9e2a-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b9e2a-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e2a-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b9e2a-128">-RoleName</span></span>
<span data-ttu-id="b9e2a-129">Hangi olayların yükseltilecektir rol.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="b9e2a-130">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="b9e2a-130">-Schedule</span></span>
<span data-ttu-id="b9e2a-131">Süreölçer olayının oluşturulması gereken dönemsel sıklık.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="b9e2a-132">Gün (1 ve 365 arasında), saat (1 ile 23 arasında) veya dakika (1 ile 59 arasında) arasında bir zamanlama belirtin.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="b9e2a-133">-Shareıd</span><span class="sxs-lookup"><span data-stu-id="b9e2a-133">-ShareId</span></span>
<span data-ttu-id="b9e2a-134">Dosya olay tetikleyicisinde geçirilecek dosya paylaşımı KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="b9e2a-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="b9e2a-135">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="b9e2a-135">-ShareName</span></span>
<span data-ttu-id="b9e2a-136">Dosya olay tetikleyicisinde geçirilecek dosya paylaşımı KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="b9e2a-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="b9e2a-137">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="b9e2a-137">-StartTime</span></span>
<span data-ttu-id="b9e2a-138">Geçerli tetik sonucu veren günün saati.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="b9e2a-139">Zamanlama, saniye ile belirtilen zamanın başvurusuyla hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="b9e2a-140">Saat dilimi belirtilmezse, süre Device saat diliminde olduğu kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="b9e2a-141">Değer her zaman UTC saati olarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="b9e2a-142">-Konu</span><span class="sxs-lookup"><span data-stu-id="b9e2a-142">-Topic</span></span>
<span data-ttu-id="b9e2a-143">Dönemsel olayların IoT cihazında yayımlandığı konu.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="b9e2a-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="b9e2a-144">-Confirm</span></span>
<span data-ttu-id="b9e2a-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e2a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e2a-146">-WhatIf</span></span>
<span data-ttu-id="b9e2a-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9e2a-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e2a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e2a-149">CommonParameters</span></span>
<span data-ttu-id="b9e2a-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e2a-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e2a-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9e2a-152">INPUTS</span></span>

### <span data-ttu-id="b9e2a-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b9e2a-153">None</span></span>

## <span data-ttu-id="b9e2a-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9e2a-154">OUTPUTS</span></span>

### <span data-ttu-id="b9e2a-155">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b9e2a-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="b9e2a-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9e2a-156">NOTES</span></span>

## <span data-ttu-id="b9e2a-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9e2a-157">RELATED LINKS</span></span>
