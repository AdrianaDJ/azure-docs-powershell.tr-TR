---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106340"
---
# <span data-ttu-id="bcf98-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bcf98-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="bcf98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcf98-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf98-103">İç yük dengeleyici yapılandırmasının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="bcf98-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="bcf98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcf98-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bcf98-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcf98-105">DESCRIPTION</span></span>
<span data-ttu-id="bcf98-106">**Get-AzureInternalLoadBalancer** cmdlet 'ı bir Azure hizmeti için iç yük dengeleyici yapılandırmasının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="bcf98-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="bcf98-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcf98-107">EXAMPLES</span></span>

### <span data-ttu-id="bcf98-108">Örnek 1: iç yük dengeleyicinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="bcf98-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="bcf98-109">Bu komut, **Get-AzureService** cmdlet 'Ini kullanarak contososervice adlı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="bcf98-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="bcf98-110">Komut bu hizmeti, ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bcf98-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bcf98-111">Geçerli cmdlet, bu hizmet için iç yük dengeleyicinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="bcf98-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="bcf98-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcf98-112">PARAMETERS</span></span>

### <span data-ttu-id="bcf98-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bcf98-113">-InformationAction</span></span>
<span data-ttu-id="bcf98-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcf98-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bcf98-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bcf98-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bcf98-116">'A</span><span class="sxs-lookup"><span data-stu-id="bcf98-116">Continue</span></span>
- <span data-ttu-id="bcf98-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="bcf98-117">Ignore</span></span>
- <span data-ttu-id="bcf98-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="bcf98-118">Inquire</span></span>
- <span data-ttu-id="bcf98-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="bcf98-119">SilentlyContinue</span></span>
- <span data-ttu-id="bcf98-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="bcf98-120">Stop</span></span>
- <span data-ttu-id="bcf98-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="bcf98-121">Suspend</span></span>

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

### <span data-ttu-id="bcf98-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="bcf98-122">-InformationVariable</span></span>
<span data-ttu-id="bcf98-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcf98-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bcf98-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="bcf98-124">-Profile</span></span>
<span data-ttu-id="bcf98-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcf98-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bcf98-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bcf98-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bcf98-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="bcf98-127">-ServiceName</span></span>
<span data-ttu-id="bcf98-128">Bu cmdlet 'in dahili yük dengeleyicinin ayrıntılarını aldığı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcf98-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

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

### <span data-ttu-id="bcf98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf98-129">CommonParameters</span></span>
<span data-ttu-id="bcf98-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcf98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf98-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf98-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf98-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcf98-132">INPUTS</span></span>

## <span data-ttu-id="bcf98-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcf98-133">OUTPUTS</span></span>

### <span data-ttu-id="bcf98-134">Microsoft. Windowsazme. Commands. ServiceManagement. model. ınternalloadbalancercontext</span><span class="sxs-lookup"><span data-stu-id="bcf98-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="bcf98-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcf98-135">NOTES</span></span>

## <span data-ttu-id="bcf98-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcf98-136">RELATED LINKS</span></span>

[<span data-ttu-id="bcf98-137">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bcf98-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="bcf98-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="bcf98-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="bcf98-139">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="bcf98-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="bcf98-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bcf98-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="bcf98-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bcf98-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


