---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105724"
---
# <span data-ttu-id="46352-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46352-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="46352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46352-102">SYNOPSIS</span></span>
<span data-ttu-id="46352-103">Azure hizmetine iç yük dengeleyici ekler.</span><span class="sxs-lookup"><span data-stu-id="46352-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="46352-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46352-104">SYNTAX</span></span>

### <span data-ttu-id="46352-105">ServiceAndSlot (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46352-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="46352-106">Yalnızca subnetName</span><span class="sxs-lookup"><span data-stu-id="46352-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="46352-107">Subnetnameandıp</span><span class="sxs-lookup"><span data-stu-id="46352-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="46352-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="46352-108">DESCRIPTION</span></span>
<span data-ttu-id="46352-109">**Add-AzureInternalLoadBalancer** cmdlet 'ı bir Azure hizmetine iç yük dengeleyici yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="46352-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="46352-110">Sanal ağ için, iç yük dengeleyicinin bir alt ağını veya IP adresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46352-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="46352-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46352-111">EXAMPLES</span></span>

### <span data-ttu-id="46352-112">Örnek 1: iç yük dengeleyici ekleme</span><span class="sxs-lookup"><span data-stu-id="46352-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="46352-113">Bu komut, ContosoWebsite01 adlı hizmete ContosoILB adlı bir iç yük dengeleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="46352-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="46352-114">Örnek 2: belirtilen alt ağ için iç yük dengeleyici ekleme</span><span class="sxs-lookup"><span data-stu-id="46352-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="46352-115">Bu komut, ContosoWebsite01 adlı hizmete ContosoILB adlı bir iç yük dengeleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="46352-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="46352-116">Komut, Frontenvseçsubnet adlı alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="46352-117">Örnek 3: belirtilen alt ağ ve adres için iç yük dengeleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="46352-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="46352-118">Bu komut, ContosoWebsite01 adlı hizmete ContosoILB adlı bir iç yük dengeleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="46352-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="46352-119">Komut, Frontenvseçsubnet adlı alt ağı ve sanal ağın statik adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="46352-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46352-120">PARAMETERS</span></span>

### <span data-ttu-id="46352-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="46352-121">-InformationAction</span></span>
<span data-ttu-id="46352-122">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46352-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46352-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46352-124">'A</span><span class="sxs-lookup"><span data-stu-id="46352-124">Continue</span></span>
- <span data-ttu-id="46352-125">Manıza</span><span class="sxs-lookup"><span data-stu-id="46352-125">Ignore</span></span>
- <span data-ttu-id="46352-126">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="46352-126">Inquire</span></span>
- <span data-ttu-id="46352-127">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="46352-127">SilentlyContinue</span></span>
- <span data-ttu-id="46352-128">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="46352-128">Stop</span></span>
- <span data-ttu-id="46352-129">Biliriz</span><span class="sxs-lookup"><span data-stu-id="46352-129">Suspend</span></span>

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

### <span data-ttu-id="46352-130">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="46352-130">-InformationVariable</span></span>
<span data-ttu-id="46352-131">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="46352-132">-Internalloadbalancername</span><span class="sxs-lookup"><span data-stu-id="46352-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="46352-133">Bu cmdlet 'in eklediği iç yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="46352-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="46352-134">-Profile</span></span>
<span data-ttu-id="46352-135">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46352-136">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="46352-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46352-137">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="46352-137">-ServiceName</span></span>
<span data-ttu-id="46352-138">Bu cmdlet 'in iç yük dengeleyicisi eklediği hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

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

### <span data-ttu-id="46352-139">-Staticvnetıpaddress</span><span class="sxs-lookup"><span data-stu-id="46352-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="46352-140">Bu cmdlet 'in eklediği bir iç yük dengeleyicinin sanal ağ IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="46352-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="46352-141">-SubnetName</span></span>
<span data-ttu-id="46352-142">Bu cmdlet 'in eklediği iç yük dengeleyicinin alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46352-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="46352-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46352-143">CommonParameters</span></span>
<span data-ttu-id="46352-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46352-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46352-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46352-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46352-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46352-146">INPUTS</span></span>

## <span data-ttu-id="46352-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46352-147">OUTPUTS</span></span>

### <span data-ttu-id="46352-148">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="46352-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="46352-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46352-149">NOTES</span></span>

## <span data-ttu-id="46352-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46352-150">RELATED LINKS</span></span>

[<span data-ttu-id="46352-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46352-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="46352-152">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="46352-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="46352-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46352-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="46352-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46352-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


