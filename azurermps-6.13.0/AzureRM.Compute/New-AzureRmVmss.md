---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 9f6135917f2e6cbfc05511637b3b20bd126d54b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572898"
---
# New-AzureRmVmss

## SYNOPSIS
Bir VMSS oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### DefaultParameter (varsayılan)
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmVmss** cmdlet 'i Azure 'Da sanal makine ölçek KÜMESI (VMSS) oluşturur.
`SimpleParameterSet`Önceden ayarlanmış BIR VMSS ve ilişkili kaynakları hızlı şekilde oluşturmak için basit parametre kümesi () kullanın. `DefaultParameter`Vmsubnet 'in her bileşenini ve oluşturmadan önce her ilişkili kaynağı tam olarak yapılandırmanız gerektiğinde daha gelişmiş senaryolar için varsayılan parametre kümesi 'ni () kullanın.

## ÖRNEKLERDEN

### Örnek 1: **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzureRmVmss -Credential $vmCred -VMScaleSetName $vmssName
```

Yukarıdaki komut, adla aşağıdakileri oluşturur `$vmssName` :
* Kaynak grubu
* Sanal ağ
* Bir yük dengeleyici
* Genel bir IP
* 2 örnek içeren VMSS

VMSS 'deki VM 'Ler için seçilen varsayılan görüntü `2016-Datacenter Windows Server``Standard_DS1_v2`

### Örnek 2: **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

Yukarıdaki karmaşık örnek bir VMSS oluşturur, bunun anlamı aşağıda verilmiştir:
* İlk komut belirtilen ad ve konuma sahip bir kaynak grubu oluşturur.
* İkinci komut, depolama hesabı oluşturmak için **New-AzureRmStorageAccount** cmdlet 'ini kullanır.
* Üçüncü komut, **Get-AzureRmStorageAccount** cmdlet 'ini kullanarak ikinci komutta oluşturulmuş depolama hesabını alır ve sonucu $STOAccount değişkeninde depolar.
* Beşinci komut, bir alt ağ oluşturmak için **New-AzureRmVirtualNetworkSubnetConfig** cmdlet 'ini kullanır ve sonucu $SubNet adlı değişkende depolar.
* Altıncı komut, sanal bir ağ oluşturmak için **New-AzureRmVirtualNetwork** cmdlet 'ini kullanır ve sonucu $VNET adlı değişkende depolar.
* Yedinci komutu, altıncı komutta oluşturulan sanal ağ hakkında bilgi almak için **Get-AzureRmVirtualNetwork** kullanır ve $VNET adlı değişkende bu bilgileri depolar.
* Sekizinci ve dokuzuncu komutu, bu genel IP adresinden bilgi oluşturmak ve almak için **New-azurermpublicıpaddress** ve **Get-azurermpublicıpaddress** kullanır.
* Komutlar $PubIP adlı değişkende bilgileri depolar.
* Onuncu komutu, ön uç yük dengeleyicisi oluşturmak için **New-Azurermloadbalancerfrontendıconfıg** cmdlet 'ini kullanır ve sonucu $frontend adlı değişkende depolar.
* Onventh komutu, **Yeni-AzureRmLoadBalancerBackendAddressPoolConfig** öğesini kullanarak arka uç adres havuzu yapılandırması oluşturur ve sonucu $BackendAddressPool değişkeninde depolar.
* İkinci komut, bir yoklama oluşturmak için **New-AzureRmLoadBalancerProbeConfig** öğesini kullanır ve $Probe adlı değişkende yoklama bilgilerini depolar.
* Üçüncü on komutu, yük dengeleyici gelen ağ adresi çevirisi (NAT) havuz yapılandırması oluşturmak için **New-Azurermloadbalancerınboundnatpoolconfig** cmdlet 'ini kullanır.
* On on komutu, yük dengeleyici kural yapılandırması oluşturmak için **New-AzureRmLoadBalancerRuleConfig** öğesini kullanır ve sonucu $LBRule değişkeninde depolar.
* On beşinci komut, bir yük dengeleyici oluşturmak için **New-AzureRmLoadBalancer** cmdlet 'ini kullanır ve sonucu $ActualLb adlı değişkende depolar.
* Altıncı komut **Get-AzureRmLoadBalancer** 'ı kullanarak on beşinci komutta oluşturulmuş yük dengeleyici hakkında bilgi alır ve $ExpectedLb adlı değişkende bu bilgileri depolar.
* On yedi komutu, bir VMSS IP yapılandırması oluşturmak için **New-AzureRmVmssIPConfig** cmdlet 'ini kullanır ve $IPCfg adlı değişkende bu bilgileri depolar.
* Sekizinci on komutu, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.
* Nıneon komutu, VMSS 'yi oluşturmak için **New-AzureRmVmss** cmdlet 'ini kullanır.

## PARAMETRELERINE

### -AllocationMethod
Ölçek kümesinin genel IP adresi için ayırma yöntemi (statik veya dinamik).  Değer sağlanmadıysa, ayırma statik olur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iş
Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.

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

### -BackendPoolName
Bu ölçek kümesi için yük dengeleyicide kullanılacak arka uç adres havuzunun adı.  Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip yeni bir arka uç havuzu oluşturulur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Backendbağlantınoktası
Ölçek kümesi yük dengeleyici tarafından ölçek kümesindeki VM 'lerle iletişim kurmak için kullanılan arka uç bağlantı noktası numaraları.  Değer belirtilmezse, 3389 ve 5985 bağlantı noktaları Windows VM 'ler için kullanılır ve Linux VM 'Ler için bağlantı noktası 22 kullanılır.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Bu ölçek kümesindeki VM 'Ler için yönetici kimlik bilgileri (Kullanıcı adı ve parola).

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Veri disklerinin boyutunu GB cinsinden belirtir.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -DomainNameLabel
Bu ölçek kümesi için genel Fully-Qualified etki alanı adı (FQDN) için etki alanı adı etiketi. Bu, etki alanı adının ölçek kümesine otomatik olarak atandığı ilk bileşenidir. Otomatik olarak atanan etki alanı adları formu ( <DomainNameLabel> . <Location> . cloudapp.azure.com). Değer sağlanmadıysa, varsayılan etki alanı adı etiketi <ScaleSetName> ve <ResourceGroupName> .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frontenvseçpoolname
Ölçek kümesi yük dengeleyicisinde kullanılacak ön uç adres havuzunun adı.  Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir ön uç adres havuzu oluşturulur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GörüntüAdı
Bu ölçek kümesindeki VM 'Lerin adı. Değer sağlanmazsa, "Windows Server 2016 DataCenter" resmi kullanılır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Ölçek kümesindeki VM görüntülerinin sayısı.  Değer sağlanmazsa, 2 örnek oluşturulacaktır.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Bu ölçek kümesiyle kullanılacak yük dengeleyicinin adı.  Değer belirtilmemişse, ölçek kümesiyle aynı adı kullanan yeni bir yük dengeleyici oluşturulur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Bu ölçek kümesinin oluşturulacağı Azure konumu.  Değer belirtilmemişse, konum, parametrelerde başvurulan diğer kaynakların konumundan çıkarılacaktır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Natbackendbağlantınoktası
Gelen ağ adresi çevirisi için arka uç bağlantı noktası.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publicıpaddressname
Bu ölçek kümesiyle kullanılacak ortak IP adresi adı.  Değer sağlanmadıysa ölçek kümesiyle aynı ada sahip yeni bir genel IPAddress oluşturulur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS 'nin kaynak grubunun adını belirtir.  Değer belirtilmemişse, ölçek kümesiyle aynı ad kullanılarak yeni bir ResourceGroup oluşturulur.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecurityGroupName
Bu ölçek kümesine uygulanacak ağ güvenlik grubunun adı.  Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip bir varsayılan ağ güvenlik grubu oluşturulur ve ölçek kümesine uygulanır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Tek bir yerleştirme grubunda ölçek kümesi oluşturmak için bunu kullanın; varsayılan, birden çok gruptur

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Bu ScaleSet 'in kullanacağı alt ağın adres öneki. Değer sağlanmazsa varsayılan alt ağ ayarları (192.168.1.0/24) uygulanacaktır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Bu ölçek kümesiyle kullanılacak alt ağın adı.  Değer sağlanmadıysa, ölçek kümesiyle aynı adla yeni bir alt ağ oluşturulur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Parametre varsa, ölçek kümesindeki VM 'ler (lar) otomatik olarak oluşturulan bir yönetilen sistem kimliğine atanır.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
Bu ölçek kümesindeki VM örnekleri için yükseltme ilkesi modu.  Yükseltme ilkesi otomatik, El Ile veya çalışırken yükseltme belirleyebilir.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Useratandidentity
Ölçek kümesindeki VM 'ler 'e atanması gereken yönetilen hizmet kimliğinin adı.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Bu cmdlet 'in oluşturduğu VMSS 'in özelliklerini içeren **VirtualMachineScaleSet** nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Bu ölçek kümesiyle birlikte kullanılacak sanal ağın adı.  Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir sanal ağ oluşturulur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Bu ölçek kümesindeki VM örneklerinin boyutu.  Boyut belirtilmemişse varsayılan boyut (Standard_DS1_v2) kullanılır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
Bu ölçek kümesiyle kullanılan sanal ağın adres öneki.  Değer sağlanmadıysa varsayılan sanal ağ adresi önek ayarları (192.168.0.0/16) kullanılacaktır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bölge
Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet
Parametreler: VirtualMachineScaleSet (ByValue)

### System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Başlangıç-AzureRmVmss](./Start-AzureRmVmss.md)

[Dur-AzureRmVmss](./Stop-AzureRmVmss.md)

[Güncelleştirme-AzureRmVmss](./Update-AzureRmVmss.md)


