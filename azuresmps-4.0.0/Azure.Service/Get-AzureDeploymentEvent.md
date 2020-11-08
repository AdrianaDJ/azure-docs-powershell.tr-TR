---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105650"
---
# <span data-ttu-id="bffa8-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="bffa8-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="bffa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bffa8-102">SYNOPSIS</span></span>
<span data-ttu-id="bffa8-103">Azure 'un başlattığı olaylar hakkında, bu etkiyi gerçekleştiren sanal makineleri ve bulut hizmetlerini getirir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="bffa8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bffa8-104">SYNTAX</span></span>

### <span data-ttu-id="bffa8-105">GetDeploymentEventBySlot (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bffa8-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bffa8-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="bffa8-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bffa8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bffa8-107">DESCRIPTION</span></span>
<span data-ttu-id="bffa8-108">**Get-AzureDeploymentEvent** cmdlet 'ı, Azure 'un bu etkiyi gerçekleştiren olaylarla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="bffa8-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="bffa8-109">Bu olaylar, planlanmış bakım olaylarını içerir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="bffa8-110">Bu cmdlet, rolün etkinlik örneğini veya sanal makinesini tanımlayan olayların listesini, etkisinin nedenini ve olayın başlangıç saatini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bffa8-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="bffa8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bffa8-111">EXAMPLES</span></span>

### <span data-ttu-id="bffa8-112">2</span><span class="sxs-lookup"><span data-stu-id="bffa8-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="bffa8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bffa8-113">PARAMETERS</span></span>

### <span data-ttu-id="bffa8-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bffa8-114">-DeploymentName</span></span>
<span data-ttu-id="bffa8-115">Bu cmdlet 'in olayları aldığı dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa8-116">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="bffa8-116">-EndTime</span></span>
<span data-ttu-id="bffa8-117">Bu cmdlet 'in aldığı zamanlanmış olayların bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa8-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bffa8-118">-InformationAction</span></span>
<span data-ttu-id="bffa8-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bffa8-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bffa8-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bffa8-121">'A</span><span class="sxs-lookup"><span data-stu-id="bffa8-121">Continue</span></span>
- <span data-ttu-id="bffa8-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="bffa8-122">Ignore</span></span>
- <span data-ttu-id="bffa8-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="bffa8-123">Inquire</span></span>
- <span data-ttu-id="bffa8-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="bffa8-124">SilentlyContinue</span></span>
- <span data-ttu-id="bffa8-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="bffa8-125">Stop</span></span>
- <span data-ttu-id="bffa8-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="bffa8-126">Suspend</span></span>

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

### <span data-ttu-id="bffa8-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="bffa8-127">-InformationVariable</span></span>
<span data-ttu-id="bffa8-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bffa8-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="bffa8-129">-Profile</span></span>
<span data-ttu-id="bffa8-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bffa8-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bffa8-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa8-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="bffa8-132">-ServiceName</span></span>
<span data-ttu-id="bffa8-133">Bu cmdlet 'in zamanlanmış olayları aldığı barındırılan hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa8-134">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="bffa8-134">-Slot</span></span>
<span data-ttu-id="bffa8-135">Bu cmdlet 'in zamanlanmış olayları aldığı dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="bffa8-136">Geçerli değerler: hazırlama ve üretim.</span><span class="sxs-lookup"><span data-stu-id="bffa8-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="bffa8-137">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa8-138">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="bffa8-138">-StartTime</span></span>
<span data-ttu-id="bffa8-139">Bu cmdlet 'in aldığı zamanlanmış olayların başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa8-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffa8-140">CommonParameters</span></span>
<span data-ttu-id="bffa8-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bffa8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffa8-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bffa8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffa8-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bffa8-143">INPUTS</span></span>

## <span data-ttu-id="bffa8-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bffa8-144">OUTPUTS</span></span>

## <span data-ttu-id="bffa8-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bffa8-145">NOTES</span></span>

## <span data-ttu-id="bffa8-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bffa8-146">RELATED LINKS</span></span>

[<span data-ttu-id="bffa8-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="bffa8-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


