---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107398"
---
# New-WAPackVM

## SYNOPSIS
Sanal makine oluşturur.

## INDEKI

### CreateVMFromTemplate (varsayılan)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Yeni-WAPackVM** cmdlet 'i sanal makine oluşturur.

## ÖRNEKLERDEN

### Örnek 1: şablon kullanarak Windows işletim sistemi için sanal makine oluşturma
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

İlk komut bir **PSCredential** nesnesi oluşturur ve $Credentials değişkeninde depolar.
Cmdlet bir hesap ve parola sorar.
Daha fazla bilgi için yazın `Get-Help Get-Credential` .

İkinci komut ContosoTemplate04 adındaki sanal makine şablonunu **Get-WAPackVMTemplate** cmdlet 'ini kullanarak alır ve ardından $Template değişkeninde depolar.

Son komutu, $Template değişkeninde depolanan şablona dayalı olarak ContosoV023 adlı bir sanal makine oluşturur.
Komut *Windows* parametresini belirtir ve bu nedenle sanal makine Windows işletim sisteminin bir sürümünü çalışmalıdır.

### Örnek 2: şablon kullanarak Linux işletim sistemi için sanal makine oluşturma
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

İlk komut bir **PSCredential** nesnesi oluşturur ve $Credentials değişkeninde depolar.

İkinci komut ContosoTemplate19 adındaki sanal makine şablonunu **Get-WAPackVMTemplate** cmdlet 'ini kullanarak alır ve ardından $Template değişkeninde depolar.

Son komutu, $Template değişkeninde depolanan şablona dayalı olarak ContosoV028 adlı bir sanal makine oluşturur.
Komut, *Linux* parametresini belirtir ve bu nedenle sanal makinenin Linux işletim sisteminin bir sürümünü çalıştırması gerekir.

### Örnek 3: işletim sistemi diskinden ve boyut profilinden sanal makine oluşturma
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

İlk komut, **Get-wapackkvmosdisk** cmdlet 'ini kullanarak $OSDisk, contosodee

İkinci komut, **Get-WAPackVMSizeProfile** cmdlet 'ini kullanarak, düz Sizevm adlı boyut profilini alır ve $SizeProfile değişkeninde depolar.

Son komutu, $OSDisk depolanan işletim sistemi diskinden ve $SizeProfile depolanan boyut profilinde ContosoV073 adlı bir sanal makine oluşturur.

## PARAMETRELERINE

### -\Administrators Sshkey
Yönetici hesabının güvenli kabuk (SSH) anahtarını belirtir.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Cmdlet 'in Linux işletim sistemini çalıştırmak için bir sanal makine oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Sanal makine için bir ad belirtir.

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

### -OSDisk
Bir işletim sistemi diskini **VirtualHardDisk** nesnesi olarak belirtir.
İşletim sistemi disketi edinmek için **Get-WAPackVMOSDisk** cmdlet 'ini kullanın.

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
Ürün anahtarını belirtir.
Ürün anahtarı, ürün lisansını tanımlayan 25 basamaklı bir sayıdır.
Sanal makineye veya konağa yüklemeyi planladığınız bir işletim sistemi için ürün anahtarı kullanın.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
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

### -Şablon
Şablon belirtir.
Cmdlet, belirttiğiniz şablona göre bir sanal makine oluşturur.
Şablon nesnesi almak için Get-WAPackVMTemplate cmdlet 'ini kullanın.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Yerel yönetici hesabının kimlik bilgilerini belirtir.
**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.
Daha fazla bilgi için yazın `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
Bir sanal makinenin bir boyut profilini **HardwareProfile** nesnesi olarak belirtir.
Boyut profili edinmek için **Get-WAPackVMSizeProfile** cmdlet 'ini kullanın.

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Sanal ağ belirtir.
Cmdlet, sanal makineyi belirttiğiniz sanal ağa bağlar.
Sanal ağ edinmek için **Get-WAPackVNet** cmdlet 'ini kullanın.

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Cmdlet 'in Windows işletim sistemini çalıştırmak için bir sanal makine oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Restart-WAPackVM](./Restart-WAPackVM.md)

[Özgeçmiş-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Başlangıç-WAPackVM](./Start-WAPackVM.md)

[Dur-WAPackVM](./Stop-WAPackVM.md)

[Askıya al-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


