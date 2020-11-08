---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105967"
---
# Set-AzureEnvironment

## SYNOPSIS
Azure ortamının özelliklerini değiştirir.

## INDEKI

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureEnvironment** cmdlet 'ı bir Azure ortamının özelliklerini değiştirir.
Yeni özellik değerleriyle ortamı temsil eden bir nesne döndürür.
Ortam ve özellik değerlerini değiştirmek için diğer parametreleri belirlemek için **ad** parametresini kullanın.
**Set-AzureEnvironment** ' i kullanarak Azure ortamının adını değiştirebilirsiniz.

Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.
Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.
Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

Not: Azurecyüksek veya AzureChinaCloud ortamlarının özelliklerini değiştirmeyin.
Oluşturduğunuz özel ortamların değerlerini değiştirmek için bu cmdlet 'i kullanın.

## ÖRNEKLERDEN

### Örnek 1: ortam özelliklerini değiştirme
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

Bu komut, ContosoEnv ortamının **Publishsettingsfileurl** ve **storageendpoint** özelliklerinin değerlerini değiştirir.

## PARAMETRELERINE

### -Activedirectoryenvseçnokta
Azure Active Directory kimlik doğrulaması uç noktasını belirtilen değerle değiştirir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Activedirectoryserviceendpointresourceıd
Azure Active Directory tarafından yönetilen bir yönetim API 'sinin kaynak KIMLIĞINI belirtir.

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

### -AdTenant
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

### -AzureKeyVaultDnsSuffix
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

### -AzureKeyVaultServiceEndpointResourceId
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

### -EnableAdfsAuthentication
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryEndpoint
Azure Resource Manager galerisinin uç noktasını belirtilen değerle değiştirir.
Galeri uç noktası, kaynak grubu Galeri şablonlarının konumudur.
Azure Kaynak grupları ve galeri şablonları hakkında daha fazla bilgi için [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052)yardım konusuna bakın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphEndpoint
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPortalUrl 'Si
Azure yönetim portalının URL 'sini belirtilen değerle değiştirir.

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

### -Ad
Değiştirilecek ortamı tanımlar.
Bu parametre gereklidir.
Parametre değeri büyük/küçük harfe duyarlıdır.
Joker karakterler kullanılamaz.

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

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -PublishSettingsFileUrl
Belirtilen ortamdaki yayımlama ayarları dosyalarının URL 'sini değiştirir.
Azure yayımlama ayarları dosyası, hesabınızla ilgili bilgileri içeren bir XML dosyasıdır ve Windows PowerShell 'in sizin adınıza Azure hesabınızda oturum açmasını sağlayan bir yönetim sertifikasıdır.

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

### -ResourceManagerEndpoint
Hesap ile ilişkili kaynak gruplarıyla ilgili veriler de içinde olmak üzere, Azure Resource Manager verilerinin uç noktasını değiştirir.
Azure Resource Manager hakkında daha fazla bilgi için [Azure Resource Manager cmdlet 'lerinin](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) ve [Kaynak Yöneticisi ile Windows PowerShell](https://go.microsoft.com/fwlink/?LinkID=394767)  'in ( https://go.microsoft.com/fwlink/?LinkID=394767) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
Belirtilen ortamdaki Azure hizmeti uç noktasının URL 'sini değiştirir.
Azure hizmeti uç noktası, uygulamanızın Genel Azure platformu tarafından yönetilip yönetilmediğini, Çin 'de 21Vianet tarafından sağlanan Azure 'u veya özel bir Azure yüklemesini belirler.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlDatabaseDnsSuffix
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

### -StorageEndpoint
Belirtilen ortamdaki depolama hizmetlerinin varsayılan uç noktasını değiştirir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerDnsSuffix
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### Microsoft. Windowsazme. Commands. Utilities. Common. WindowsAzureEnvironment

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)


