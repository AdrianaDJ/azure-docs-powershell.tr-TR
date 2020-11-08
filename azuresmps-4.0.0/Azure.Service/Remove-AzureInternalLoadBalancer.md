---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106475"
---
# <span data-ttu-id="fc3e8-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fc3e8-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="fc3e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3e8-103">İç yük dengeleyici yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="fc3e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc3e8-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fc3e8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc3e8-105">DESCRIPTION</span></span>
<span data-ttu-id="fc3e8-106">**Remove-AzureInternalLoadBalancer** cmdlet 'ı bir Azure hizmetinden iç yük dengeleyici yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="fc3e8-107">Herhangi bir uç nokta iç yük dengeleyiciye başvuruyorsa, bu cmdlet yapılandırmayı kaldıramaz.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="fc3e8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc3e8-108">EXAMPLES</span></span>

### <span data-ttu-id="fc3e8-109">Örnek 1: iç yük dengeleyici yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fc3e8-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="fc3e8-110">Bu komut, ContosoService adlı hizmetin iç yük dengeleyici yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="fc3e8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc3e8-111">PARAMETERS</span></span>

### <span data-ttu-id="fc3e8-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fc3e8-112">-InformationAction</span></span>
<span data-ttu-id="fc3e8-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fc3e8-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fc3e8-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc3e8-115">'A</span><span class="sxs-lookup"><span data-stu-id="fc3e8-115">Continue</span></span>
- <span data-ttu-id="fc3e8-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="fc3e8-116">Ignore</span></span>
- <span data-ttu-id="fc3e8-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fc3e8-117">Inquire</span></span>
- <span data-ttu-id="fc3e8-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fc3e8-118">SilentlyContinue</span></span>
- <span data-ttu-id="fc3e8-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fc3e8-119">Stop</span></span>
- <span data-ttu-id="fc3e8-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fc3e8-120">Suspend</span></span>

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

### <span data-ttu-id="fc3e8-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fc3e8-121">-InformationVariable</span></span>
<span data-ttu-id="fc3e8-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fc3e8-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="fc3e8-123">-Profile</span></span>
<span data-ttu-id="fc3e8-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc3e8-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc3e8-126">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="fc3e8-126">-ServiceName</span></span>
<span data-ttu-id="fc3e8-127">Bu cmdlet 'in iç yük dengeleyiciden kaldırıldığı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="fc3e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3e8-128">CommonParameters</span></span>
<span data-ttu-id="fc3e8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3e8-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc3e8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3e8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc3e8-131">INPUTS</span></span>

## <span data-ttu-id="fc3e8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc3e8-132">OUTPUTS</span></span>

### <span data-ttu-id="fc3e8-133">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="fc3e8-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="fc3e8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc3e8-134">NOTES</span></span>

## <span data-ttu-id="fc3e8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc3e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="fc3e8-136">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fc3e8-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="fc3e8-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fc3e8-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="fc3e8-138">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="fc3e8-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="fc3e8-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fc3e8-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


