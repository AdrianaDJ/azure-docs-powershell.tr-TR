---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106200"
---
# New-AzureVM

## SYNOPSIS
Azure sanal makinesi oluşturur.

## INDEKI

### ExistingService (varsayılan)
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### CreateService
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-AzureVM** cmdlet 'i var olan bir Azure hizmetine yeni bir sanal makine ekler ya da *Location* veya *affinitygroup* belirtilmişse geçerli abonelikte sanal makine ve hizmet oluşturur.

## ÖRNEKLERDEN

### Örnek 1: Windows yapılandırması için sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

Bu komut, Windows işletim sisteminin sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve belirtilen benzeşim grubunda sanal makine oluşturmak için kullanır.

### Örnek 2: Linux yapılandırması için sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

Bu komut, Linux için sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve belirtilen benzeşim grubunda sanal makine oluşturmak için kullanır.

### Örnek 3: sanal makine oluşturma ve veri disketi ekleme
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

İlk iki komut **Get-AzureVMImage** cmdlet 'ini kullanarak kullanılabilir resimleri alır ve bunlardan birini $Image değişkeninde depolar.

Bu komut, Windows işletim sisteminin sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve Azure veri disketiyle sanal makine oluşturmak için kullanır.

### Örnek 4: ayrılmış IP adresine sahip sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

Bu komut, Windows işletim sisteminin sanal makine yapılandırmasını temel alan bir sağlama yapılandırması oluşturur ve ayrılmış IP adresi içeren bir sanal makine oluşturmak için kullanır.

## PARAMETRELERINE

### -AffinityGroup
Bulut hizmetinin bulunduğu Azure benzeşim grubunu belirtir.
Bu parametre yalnızca bu cmdlet bir bulut hizmeti oluşturduğunda gereklidir.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentLabel
Dağıtım için bir etiket belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
Dağıtım adını belirtir.
Belirtilmemişse, bu cmdlet dağıtım adı olarak hizmet adını kullanır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DnsSettings
Yeni dağıtımın DNS ayarlarını tanımlayan bir DNS sunucusu nesnesi belirtir.

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

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

### -Informationvariable
Bir bilgi değişkeni belirtir.

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

### -Internalloadbalancerconfig
Dahili bir yük dengeleyici belirtir.
Bu parametre kullanılmaz.

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Konum
Yeni hizmeti barındıran konumu belirtir.
Hizmet zaten varsa, bu parametreyi belirtmeyin.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -Rezervedıpname
Ayrılmış IP adresinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Smardnsfqdn
Geriye doğru DNS için tam etki alanı adını belirtir.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceDescription
Yeni hizmetin açıklamasını belirtir.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceLabel
Yeni hizmet için bir etiket belirtir.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HizmetAdı
Yeni veya var olan hizmet adını belirtir.

Hizmet yoksa, bu cmdlet sizin için oluşturur.
Servisin oluşturulacağı yeri belirtmek için *Location* veya *affinitygroup* parametresini kullanın.

Hizmet varsa, *Location* veya *affinitygroup* parametresi gerekmez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM 'Ler
Oluşturulacak sanal makine nesnelerinin listesini belirtir.

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Vağ adı
Bu cmdlet 'in sanal makineyi dağıttığı sanal ağ adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForBoot
Bu cmdlet 'in sanal makinenin **Readyrole** durumuna ulaşmasını beklediğini belirtir.
Bu cmdlet beklenirken, sanal makine şu durumlardan birine gelirse başarısız olur: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)


