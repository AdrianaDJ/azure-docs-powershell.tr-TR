---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105914"
---
# <span data-ttu-id="79a9e-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="79a9e-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="79a9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="79a9e-103">İç yük dengeleyici yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79a9e-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="79a9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79a9e-104">SYNTAX</span></span>

### <span data-ttu-id="79a9e-105">ServiceAndSlot (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79a9e-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="79a9e-106">Yalnızca subnetName</span><span class="sxs-lookup"><span data-stu-id="79a9e-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="79a9e-107">Subnetnameandıp</span><span class="sxs-lookup"><span data-stu-id="79a9e-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="79a9e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79a9e-108">DESCRIPTION</span></span>
<span data-ttu-id="79a9e-109">**New-AzureInternalLoadBalancerConfig** cmdlet 'ı bir **ınternalloadbalancerconfig** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79a9e-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="79a9e-110">Bir Azure sanal makine dağıtımını oluştururken iç yük dengeleyici yapılandırması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a9e-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="79a9e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79a9e-111">EXAMPLES</span></span>

### <span data-ttu-id="79a9e-112">Örnek 1: iç yük dengeleyici yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="79a9e-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="79a9e-113">Bu komut, Frontenvseçsubnet adlı alt ağ için bir iç yük dengeleyici yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79a9e-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="79a9e-114">Bu komut, sanal makine dağıtımında kullanmanız için yapılandırmayı $IlbConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="79a9e-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="79a9e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79a9e-115">PARAMETERS</span></span>

### <span data-ttu-id="79a9e-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="79a9e-116">-InformationAction</span></span>
<span data-ttu-id="79a9e-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a9e-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="79a9e-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79a9e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79a9e-119">'A</span><span class="sxs-lookup"><span data-stu-id="79a9e-119">Continue</span></span>
- <span data-ttu-id="79a9e-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="79a9e-120">Ignore</span></span>
- <span data-ttu-id="79a9e-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="79a9e-121">Inquire</span></span>
- <span data-ttu-id="79a9e-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="79a9e-122">SilentlyContinue</span></span>
- <span data-ttu-id="79a9e-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="79a9e-123">Stop</span></span>
- <span data-ttu-id="79a9e-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="79a9e-124">Suspend</span></span>

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

### <span data-ttu-id="79a9e-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="79a9e-125">-InformationVariable</span></span>
<span data-ttu-id="79a9e-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a9e-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="79a9e-127">-Internalloadbalancername</span><span class="sxs-lookup"><span data-stu-id="79a9e-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="79a9e-128">Bu cmdlet 'in yapılandırmada eklediği iç yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a9e-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="79a9e-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="79a9e-129">-Profile</span></span>
<span data-ttu-id="79a9e-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a9e-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79a9e-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="79a9e-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79a9e-132">-Staticvnetıpaddress</span><span class="sxs-lookup"><span data-stu-id="79a9e-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="79a9e-133">Bu cmdlet 'in yapılandırmada eklediği iç yük dengeleyicinin sanal ağ IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a9e-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a9e-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="79a9e-134">-SubnetName</span></span>
<span data-ttu-id="79a9e-135">İç yük dengeleyicinin alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a9e-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a9e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a9e-136">CommonParameters</span></span>
<span data-ttu-id="79a9e-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79a9e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a9e-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a9e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a9e-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79a9e-139">INPUTS</span></span>

## <span data-ttu-id="79a9e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79a9e-140">OUTPUTS</span></span>

### <span data-ttu-id="79a9e-141">Microsoft. Windowsazde. Commands. ServiceManagement. model. ınternalloadbalancerconfig</span><span class="sxs-lookup"><span data-stu-id="79a9e-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="79a9e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79a9e-142">NOTES</span></span>

## <span data-ttu-id="79a9e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79a9e-143">RELATED LINKS</span></span>

[<span data-ttu-id="79a9e-144">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79a9e-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79a9e-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79a9e-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79a9e-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79a9e-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79a9e-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79a9e-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


