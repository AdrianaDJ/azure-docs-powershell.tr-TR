---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 33b7308841fe9f9886b07eb19e14b97108cd2673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752511"
---
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Hassas verileri şifreler.

## INDEKI

### ByFactoryName (varsayılan)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azverifactoryencryptvalue** cmdlet 'i parola veya Microsoft SQL Server bağlantı dizesi gibi hassas verileri şifreler ve şifrelenmiş bir değer döndürür.

## ÖRNEKLERDEN

### Örnek 1: ODBC dışı bağlantı dizesini şifreleme
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak belirtilen bağlantı dizesini bir **SecureString** nesnesine dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.
Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .
İzin verilen değerler: SQL Server veya Oracle bağlantı dizesi.
İkinci komut, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Value depolanan nesne için şifreli bir değer oluşturur.

### Örnek 2: Windows kimlik doğrulaması kullanan ODBC olmayan bir bağlantı dizesini şifreleyin.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

İlk komut, **ConvertTo-SecureString** kullanarak belirtilen bağlantı dizesini güvenli bir dize nesnesine dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.
İkinci komut, Windows kimlik doğrulamasını (Kullanıcı adı ve parola) biriktirmek için Get-Credential cmdlet 'ini kullanır ve bu **PSCredential** nesnesini $Credential değişkenine depolar.
Daha fazla bilgi için yazın `Get-Help Get-Credential` .
Üçüncü komut, $Value depolanan nesne için, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential şifreli bir değer oluşturur.

### Örnek 3: dosya sistemi bağlantılı hizmeti için sunucu adını ve kimlik bilgilerini şifrele
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

İlk komut, **ConvertTo-SecureString** kullanarak belirtilen dizeyi güvenli bir dizeye dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.
İkinci komut, Windows kimlik doğrulamasını (Kullanıcı adı ve parola) biriktirmek için **Get-Credential** kullanır ve sonra bu **PSCredential** nesnesini $Credential değişkeninde depolar.
Üçüncü komut, $Value depolanan nesne için, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential şifreli bir değer oluşturur.

### Örnek 4: ".
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

**ConvertTo-SecureString** komutu belirtilen dizeyi güvenli dizeye dönüştürür.
**New-Object** komutu, güvenli Kullanıcı adı ve parola dizelerini kullanarak bir PSCredential nesnesi oluşturur.
Bunun yerine, **Get-Credential** komutunu kullanarak Windows kimlik doğrulamasını (Kullanıcı adı ve parola) toplayabilirsiniz ve ardından önceki örneklerde gösterildiği gibi $Credential değişkeninde döndürülen **PSCredential** nesnesini depolayabilirsiniz.
**Yeni-Azverifactoryencryptvalue** komutu, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential depolanan nesne için şifreli bir değer oluşturur.

### Örnek 5: ODBC bağlantılı hizmeti için kimlik bilgilerini şifreleme
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

**ConvertTo-SecureString** komutu belirtilen dizeyi güvenli dizeye dönüştürür.
**Yeni-Azverifactoryencryptvalue** komutu, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $value depolanan nesne için şifreli bir değer oluşturur.

## PARAMETRELERINE

### -AuthenticationType
Veri kaynağına bağlanmak için kullanılacak kimlik doğrulama türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- WINDOWS
- Ana
- Belirtmeden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Kullanılacak Windows kimlik doğrulama kimlik bilgilerini (Kullanıcı adı ve parola) belirtir.
Bu cmdlet burada belirttiğiniz kimlik bilgileri şifreler.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Veritabanı
Bağlı hizmetin veritabanı adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikası için verileri şifreler.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Veri Fabrikası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikası için verileri şifreler.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayName
Ağ geçidinin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği ağ geçidi verilerini şifreler.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credentialvalue
Açık veritabanı bağlantısı (ODBC) bağlantı dizesinin kimlik bilgileri olmayan kısmını belirtir.
Bu parametre yalnızca ODBC bağlantılı hizmeti için geçerlidir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği grubun verilerini şifreler.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sunucu
Bağlı hizmetin sunucu adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
Bağlı hizmet türünü belirtir.
Bu cmdlet, bu parametrenin belirttiği bağlantılı hizmet türü için verileri şifreler.
Bu parametre için kabul edilebilir değerler şunlardır:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Değer
Şifrelenecek değeri belirtir.
Şirket içi bir SQL Server bağlantılı hizmeti ve şirket içi Oracle bağlantılı hizmeti için bir bağlantı dizesi kullanın.
Şirket içi ODBC bağlantılı hizmeti için, bağlantı dizesinin kimlik bilgileri bölümünü kullanın.
Şirket içi dosya sistemi bağlantılı hizmetinde, dosya sistemi ağ geçidi bilgisayarında yerelyse, yerel veya localhost kullanın ve dosya sistemi ağ geçidi bilgisayarından farklı bir \\ \\ sunucucudır, ServerName kullanın.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası

### System. String

## ÇıKıŞLAR

### System. String

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Yeni-Azveri Factoryencryptvalue](./New-AzDataFactoryEncryptValue.md)


