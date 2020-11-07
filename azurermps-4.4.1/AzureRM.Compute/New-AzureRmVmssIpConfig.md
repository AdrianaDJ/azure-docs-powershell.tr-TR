---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 1ea3da37c0844d155f8f837f2a00064fafbf9f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764571"
---
# <span data-ttu-id="21376-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="21376-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="21376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21376-102">SYNOPSIS</span></span>
<span data-ttu-id="21376-103">Bir VMSS ağ arabirimi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21376-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21376-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21376-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21376-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21376-105">DESCRIPTION</span></span>
<span data-ttu-id="21376-106">**Yeni-AzureRmVmssIpConfig** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) ağ arabirimi IÇIN bir IP yapılandırması nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21376-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="21376-107">Bu cmdlet 'teki yapılandırmayı Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet 'inin *IP* yapılandırması parametresi olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="21376-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="21376-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21376-108">EXAMPLES</span></span>

### <span data-ttu-id="21376-109">Örnek 1: bir VMSS arabirimi için IP yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="21376-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="21376-110">Bu komut, ContosoVmssInterface02 adlı bir IP yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21376-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="21376-111">Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.</span><span class="sxs-lookup"><span data-stu-id="21376-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="21376-112">Komut $IPConfiguration değişkeninde, daha sonra **Add-Azurermvmssnetworkınterfaceconfiguration** ile kullanmak için yapılandırma ayarlarını depolar.</span><span class="sxs-lookup"><span data-stu-id="21376-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="21376-113">Örnek 2: NAT havuz ayarlarını içeren bir IP yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="21376-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="21376-114">Bu komut ContosoVmssInterface03 adlı bir IP yapılandırma nesnesi oluşturur ve daha sonra kullanmak üzere $IPConfiguration değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="21376-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="21376-115">Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.</span><span class="sxs-lookup"><span data-stu-id="21376-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="21376-116">Komut, $IPConfiguration değişkeninde yapılandırma ayarlarını daha sonra kullanmak üzere depolar.</span><span class="sxs-lookup"><span data-stu-id="21376-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="21376-117">Komut, *Loadbalancerınboundnatpoolsid* ve *Loadbalancerbackendaddresspoolsid* parametrelerinin değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="21376-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21376-118">PARAMETERS</span></span>

### <span data-ttu-id="21376-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="21376-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="21376-120">Yük dengeleyicilerde arka uç adres havuzlarına başvurular dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="21376-121">Ölçek kümesi, genel ve bir iç yük dengeleyicinin arka uç adres havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="21376-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="21376-122">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="21376-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21376-123">-DefaultProfile</span></span>
<span data-ttu-id="21376-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21376-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21376-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="21376-125">-DnsSetting</span></span>
<span data-ttu-id="21376-126">Publicıp adreslerine uygulanacak DNS ayarları.</span><span class="sxs-lookup"><span data-stu-id="21376-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="21376-127">Publicıp adreslerine uygulanacak DNS ayarlarının etki alanı adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="21376-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="21376-128">Etki alanı adı etiketi ve VM dizinini birleştirme, oluşturulacak genel IP adresi kaynaklarının etki alanı adı etiketlerdir.</span><span class="sxs-lookup"><span data-stu-id="21376-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-129">-ID</span><span class="sxs-lookup"><span data-stu-id="21376-129">-Id</span></span>
<span data-ttu-id="21376-130">Bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="21376-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="21376-132">Yük dengeleyicileri gelen ağ adresi çevirisi (NAT) havuzlarına başvurular dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="21376-133">Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="21376-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="21376-134">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="21376-134">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-135">-Loadbalancerınboundnatpoolsid</span><span class="sxs-lookup"><span data-stu-id="21376-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="21376-136">Yük dengeleyicilerde gelen NAT havuzlarına başvuru dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="21376-137">Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="21376-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="21376-138">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="21376-138">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="21376-139">-Name</span></span>
<span data-ttu-id="21376-140">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-140">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-141">-Birincil</span><span class="sxs-lookup"><span data-stu-id="21376-141">-Primary</span></span>
<span data-ttu-id="21376-142">Ağ arabiriminin birden fazla IP yapılandırması olması durumunda birincil IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="21376-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="21376-144">IP yapılandırmasını IPv4 veya IPv6 olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="21376-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="21376-145">Varsayılan olarak IPv4 alınır.</span><span class="sxs-lookup"><span data-stu-id="21376-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="21376-146">Olası değerler: ' IPv4 ' ve ' IPv6 '.</span><span class="sxs-lookup"><span data-stu-id="21376-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-147">-Publicipadresconfigurationıdintimeout ınminutes</span><span class="sxs-lookup"><span data-stu-id="21376-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="21376-148">Genel IP adresinin Boşta durma zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="21376-148">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-149">-Publicıpaddressconfigurationname</span><span class="sxs-lookup"><span data-stu-id="21376-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="21376-150">Publicıp adresi yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="21376-150">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="21376-151">-SubnetId</span></span>
<span data-ttu-id="21376-152">Yapılandırmanın, VMSS ağ arabirimini oluşturduğu alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="21376-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21376-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="21376-153">-Confirm</span></span>
<span data-ttu-id="21376-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21376-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21376-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21376-155">-WhatIf</span></span>
<span data-ttu-id="21376-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21376-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21376-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21376-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21376-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21376-158">CommonParameters</span></span>
<span data-ttu-id="21376-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21376-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21376-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21376-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21376-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21376-161">INPUTS</span></span>

## <span data-ttu-id="21376-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21376-162">OUTPUTS</span></span>

## <span data-ttu-id="21376-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21376-163">NOTES</span></span>

## <span data-ttu-id="21376-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21376-164">RELATED LINKS</span></span>

[<span data-ttu-id="21376-165">Add-Azurermvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="21376-165">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


