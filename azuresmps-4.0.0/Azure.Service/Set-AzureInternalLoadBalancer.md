---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105954"
---
# <span data-ttu-id="f9e0c-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9e0c-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="f9e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e0c-103">Bir Azure hizmetinde iç yük dengeleyici yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="f9e0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9e0c-104">SYNTAX</span></span>

### <span data-ttu-id="f9e0c-105">ServiceAndSlot (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9e0c-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9e0c-106">Yalnızca subnetName</span><span class="sxs-lookup"><span data-stu-id="f9e0c-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f9e0c-107">Subnetnameandıp</span><span class="sxs-lookup"><span data-stu-id="f9e0c-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f9e0c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9e0c-108">DESCRIPTION</span></span>
<span data-ttu-id="f9e0c-109">**Set-AzureInternalLoadBalancer** cmdlet 'ı bir Azure hizmetinde iç yük dengeleyici yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="f9e0c-110">Sanal ağ için, iç yük dengeleyicinin bir alt ağını veya IP adresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="f9e0c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9e0c-111">EXAMPLES</span></span>

### <span data-ttu-id="f9e0c-112">2</span><span class="sxs-lookup"><span data-stu-id="f9e0c-112">1:</span></span>
```

```

## <span data-ttu-id="f9e0c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9e0c-113">PARAMETERS</span></span>

### <span data-ttu-id="f9e0c-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f9e0c-114">-InformationAction</span></span>
<span data-ttu-id="f9e0c-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f9e0c-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f9e0c-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9e0c-117">'A</span><span class="sxs-lookup"><span data-stu-id="f9e0c-117">Continue</span></span>
- <span data-ttu-id="f9e0c-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="f9e0c-118">Ignore</span></span>
- <span data-ttu-id="f9e0c-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f9e0c-119">Inquire</span></span>
- <span data-ttu-id="f9e0c-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f9e0c-120">SilentlyContinue</span></span>
- <span data-ttu-id="f9e0c-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f9e0c-121">Stop</span></span>
- <span data-ttu-id="f9e0c-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f9e0c-122">Suspend</span></span>

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

### <span data-ttu-id="f9e0c-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f9e0c-123">-InformationVariable</span></span>
<span data-ttu-id="f9e0c-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f9e0c-125">-Internalloadbalancername</span><span class="sxs-lookup"><span data-stu-id="f9e0c-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="f9e0c-126">Bu cmdlet 'in değiştirdiği iç yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f9e0c-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="f9e0c-127">-Profile</span></span>
<span data-ttu-id="f9e0c-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9e0c-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9e0c-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="f9e0c-130">-ServiceName</span></span>
<span data-ttu-id="f9e0c-131">Bu cmdlet 'in dahili yük dengeleyicisinin değiştirdiği hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0c-132">-Staticvnetıpaddress</span><span class="sxs-lookup"><span data-stu-id="f9e0c-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="f9e0c-133">Dahili bir yük dengeleyicinin sanal ağ IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0c-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f9e0c-134">-SubnetName</span></span>
<span data-ttu-id="f9e0c-135">İç yük dengeleyicinin alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e0c-136">CommonParameters</span></span>
<span data-ttu-id="f9e0c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9e0c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e0c-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9e0c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e0c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9e0c-139">INPUTS</span></span>

## <span data-ttu-id="f9e0c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9e0c-140">OUTPUTS</span></span>

## <span data-ttu-id="f9e0c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9e0c-141">NOTES</span></span>

## <span data-ttu-id="f9e0c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9e0c-142">RELATED LINKS</span></span>

[<span data-ttu-id="f9e0c-143">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9e0c-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="f9e0c-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9e0c-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="f9e0c-145">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="f9e0c-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="f9e0c-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9e0c-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


