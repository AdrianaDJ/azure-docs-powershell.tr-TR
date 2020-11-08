---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105909"
---
# New-AzureQuickVM

## SYNOPSIS
Bir Azure sanal makinesini yapılandırır ve oluşturur.

## INDEKI

### Windows (varsayılan)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### UX
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-Azutalep Ickvm** cmdlet 'i, bir Azure sanal makinesini yapılandırır ve oluşturur.
Bu cmdlet, bir sanal makineyi mevcut bir Azure hizmetine dağıtabilir.
Bu cmdlet, alternatif olarak yeni sanal makineyi barındıran bir Azure hizmeti oluşturabilir.

## ÖRNEKLERDEN

### Örnek 1: sanal makine oluşturma
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

Bu komut, var olan hizmette Windows işletim sistemini çalıştıran bir sanal makine oluşturur.
Cmdlet, sanal makineyi belirtilen görüntüde temel alır.
Komut, *Waitforboot* parametresini belirtir.
Bu nedenle, cmdlet sanal makinenin başlamasını bekler.

### Örnek 2: sertifikaları kullanarak bir sanal makine oluşturma
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

İlk komut bir mağazadan sertifikaları alır ve $certs değişkeninde depolar.

İkinci komut, bir yansımadan varolan bir hizmette Windows işletim sistemini çalıştıran bir sanal makine oluşturur.
Varsayılan olarak, sanal makinede WinRM HTTPS dinleyicisi etkindir.
Komut, *Waitforboot* parametresini belirtir.
Bu nedenle, cmdlet sanal makinenin başlamasını bekler.
Komut, bir WinRM sertifikası yükler ve barındırılan hizmete X509Certificates.

### Örnek 3: Linux işletim sistemini çalıştıran bir sanal makine oluşturma
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

Bu komut, bir resimden Linux işletim sistemini çalıştıran bir sanal makine oluşturur.
Bu komut, yeni sanal makineyi barındırmak için bir hizmet oluşturur.
Komut, hizmetin konumunu belirtir.

### Örnek 4: sanal makine oluşturma ve yeni sanal makineyi barındıracak bir hizmet oluşturma
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

İlk komut **Get-AzureLocation** cmdlet 'ini kullanarak konumları alır ve bunları $Locations dizi değişkeninde depolar.

İkinci komut **Get-AzureVMImage** cmdlet 'ini kullanarak kullanılabilir resimleri alır ve bunları $Images dizi değişkeninde depolar.

Son komutu, VirtualMachine25 adında büyük bir sanal makine oluşturur.
Sanal makine Windows işletim sistemini çalıştırır.
$Images 'deki resimlerden birini temel alabilir.
Bu komut, yeni sanal makine için ContosoService03 adlı bir hizmet oluşturur.
Hizmet $Locations bir konumda.

### Örnek 5: ayrılmış IP adına sahip bir sanal makine oluşturma
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

İlk komut konumlar alır ve $Locations dizi değişkeninde depolar.

İkinci komut kullanılabilir resimleri alır ve $Images dizi değişkeninde depolar.

Son komutu, $Images resimlerden birini temel alan VirtualMachine27 adlı bir sanal makine oluşturur.
Komut, $Locations konumda bir hizmet oluşturur.
Sanal makinenin, daha önce $ipName değişkeninde depolanan ayrılmış bir IP adı vardır.

## PARAMETRELERINE

### -AdminUsername
Bu cmdlet 'in sanal makinede oluşturduğu yönetici hesabının kullanıcı adını belirtir.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AffinityGroup
Sanal makine için benzeşim grubunu belirtir.
Bu parametre veya *konum* parametresini yalnızca bu cmdlet sanal makine Için bir Azure hizmeti oluşturursa belirtin.

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

### -Kullanılabilirlik
Bu cmdlet 'in sanal makineyi oluşturduğu kullanılabilirlik kümesinin adını belirtir.

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

### -Sertifikalar
Bu cmdlet 'in hizmeti oluşturmak için kullandığı sertifikaların listesini belirtir.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Customveri dosyası
Sanal makine için bir veri dosyası belirtir.
Bu cmdlet, dosyanın içeriğini Base64 olarak kodlar.
Dosya 64 kilobayt uzunluğundan az olmalıdır.

Konuk işletim sistemi Windows işletim sistemdeydi, bu cmdlet bu verileri%SYSTEMDRIVE%\AzureData\CustomData.bin. adlı bir ikili dosya olarak kaydeder

Konuk işletim sistemi Linux ise, bu cmdlet ovf-env.xml dosyasını kullanarak verileri geçirir.
Yükleme bu dosyayı/var/lib/waagent dizinine kopyalar.
Aracı Ayrıca,/var/lib/waagent/customdata'de Base64 Ile kodlanmış verileri depolar.

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

### -DisableGuestAgent
Bu cmdlet 'in altyapıyı hizmet olarak (IaaS) Konuk aracısını sağlayan şekilde devre dışı bırakacağını gösterir.

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

### -DisableWinRMHttps
Bu cmdlet 'in HTTPS üzerinde Windows Uzaktan Yönetimi 'ni (WinRM) devre dışı bırakacağını gösterir.
Varsayılan olarak, HTTPS HTTPS üzerinden etkinleştirilir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Yeni dağıtımın DNS ayarlarını tanımlayan bir DNS sunucusu nesneleri dizisi belirtir.
Bir **DNSServer** nesnesi oluşturmak Için, **New-AzureDns** cmdlet 'ini kullanın.

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Bu cmdlet 'in HTTP üzerinden WinRM 'yi etkinleştirdiğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
İşletim sistemi diskinin ana bilgisayar önbelleğe alma modunu belirtir.
Geçerli değerler: 

- Özelliğinin
- Yazma

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

### -GörüntüAdı
İşletim sistemi disketini oluşturmak için bu cmdlet 'in kullandığı disk görüntüsünün adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Instancesize
Örneğin boyutunu belirtir.
Geçerli değerler: 

- ExtraSmall
- Küçük
- Düzey
- 13
- Çok büyük
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

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

### -Linux
Bu cmdlet 'in Linux tabanlı bir sanal makine oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Bu cmdlet 'in sanal makinede oluşturduğu Linux yönetim hesabının kullanıcı adını belirtir.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Sanal makineyi barındıran Azure veri merkezi 'ni belirtir.
Bu parametreyi belirtirseniz, cmdlet belirtilen konumda bir Azure hizmeti oluşturur.
Bu *parametreyi, yalnızca* bu cmdlet sanal makine Için bir Azure hizmeti oluşturursa belirtin.

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

### -MediaLocation
Bu cmdlet 'in sanal makineler disklerini oluşturduğu Azure depolama konumunu belirtir.

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

### -Ad
Bu cmdlet 'in oluşturduğu sanal makinenin adını belirtir.

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

### -NoExportPrivateKey
Bu yapılandırmanın özel anahtarı yükleymediğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowinrmenvseçnokta
Bu cmdlet 'in sanal makine için WinRM uç noktası eklemediğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parola
Yönetim hesabının parolasını belirtir.

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
Ayrılmış IP adını belirtir.

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
Geriye doğru DNS arama için tam nitelikli etki alanı adını belirtir.

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

### -HizmetAdı
Bu cmdlet 'in yeni sanal makineyi eklediği yeni veya mevcut bir Azure hizmetinin adını belirtir.

Yeni bir hizmet belirtirseniz, bu cmdlet 'ler bunu oluşturur.
Yeni hizmet oluşturmak için *konum* veya *affinitygroup* parametresini belirtmeniz gerekir.

Var olan bir hizmet belirtirseniz, *konum* veya *affinitygroup* belirtmeyin.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
SSH anahtar çiftlerini belirtir.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
SSH ortak anahtarlarını belirtir.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetNames
Sanal makine için alt ağ adları dizisini belirtir.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vağ adı
Sanal makine için sanal ağın adını belirtir.

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
Bu cmdlet 'in sanal makinenin State ReadyRole ulaşmasını beklediğini gösterir.
Sanal makine aşağıdaki durumlardan birine ulaşırsa cmdlet başarısız olur: FailedStartingVM, ProvisioningFailed veya ProvisioningTimeout.

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

### -Windows
Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Winrmcercertificate
Bu cmdlet 'in bir WinRM uç noktasına ilişki kurduğu sertifikayı belirtir.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Barındırılan bir hizmete dağıtılan x509 sertifikalarının dizisini belirtir.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
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

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureDns](./New-AzureDns.md)


