---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109636"
---
# Update-AzFunctionApp

## SYNOPSIS
İşlev uygulamasını güncelleştirir.

## INDEKI

### ByName (varsayılan)
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Tanım
İşlev uygulamasını güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: güncelleştirme işlevi uygulama barındırma planı.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

Bu komut işlev uygulaması barındırma planını güncelleştirir.

### Örnek 2: işlev uygulaması için SystemAssigned yönetilen kimliği ayarlayın.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

Bu komut, bir işlev uygulaması için SystemAssigned yönetilen kimliğini ayarlar.

### Örnek 3: güncelleştirme işlevi uygulama uygulaması öngörüleri.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

Bu komut, App Application Insights işlevini güncelleştirir.

### Örnek 3: bir işlev uygulamasından yönetilen kimliği kaldırın.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

Bu komut bir işlev uygulamasından yönetilen kimliği kaldırır.

## PARAMETRELERINE

### -Applicationınsightskey
Application Insights 'ın alt yapısı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Applicationınsightsname
İşlev uygulamasına eklenecek mevcut App Insights projesinin adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iş
Cmdlet 'i arka plan işi olarak çalıştırır.

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

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityId
İşlev uygulamasıyla ilişkili kullanıcı kimliklerinin listesini belirtir.
Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
İşlev uygulaması için kullanılan kimliğin türünü belirtir.
' None ' türü işlev uygulamasından tüm kimlikleri kaldırır.
Bu parametre için kabul edilebilir değerler şunlardır:-SystemAssigned-Useratandı-yok

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
İşlev uygulamasının adı.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
İşlemi başlatır ve işlem tamamlanmadan hemen döner.
İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.

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

### -PlanName
Hizmet planının adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Azure aboneliği KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketleri.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ISite

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ISite

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Kaynak konumu.
  - `CloningInfoSourceWebAppId <String>`: Kaynak uygulamanın ARM kaynak KIMLIĞI. Uygulama kaynak KIMLIĞI, diğer yuvalarda üretim yuvaları ve/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} için/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} form.
  - `[Kind <String>]`: Kaynak türü.
  - `[Tag <IResourceTags>]`: Kaynak etiketleri.
    - `[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.
  - `[ClientAffinityEnabled <Boolean?>]`: istemci <code>true</code> benzeşimini etkinleştirmek için; <code>false</code> istemci isteklerini aynı aynı aynı oturumda yönlendiren oturum benzeşimi tanımlama bilgilerini göndermeyi durdurmak için. Varsayılan <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> istemci sertifikası kimlik doğrulamasını etkinleştirmek için (TLS karşılıklı kimlik doğrulaması); Aksi takdirde <code>false</code> . Varsayılan <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: istemci sertifikası kimlik doğrulaması virgülle ayrılmış dışlama yolları
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Kopyalanan uygulama için uygulama ayarı geçersiz kılmaları. Belirtilmişse, bu ayarlar kaynak uygulamadan kopyalanan ayarları geçersiz kılar. Aksi takdirde, kaynak uygulamadaki uygulama ayarları korunur.
    - `[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> kaynak uygulamadan özel konak adları kopyalamak için; Aksi halde <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: kaynak <code>true</code> uygulamayı kaynak uygulamadan kopyalamak için; Aksi halde <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> kaynak ve hedef uygulama için yük dengelemeyi yapılandırmak için.
  - `[CloningInfoCorrelationId <String>]`: Kopyalama işleminin bağıntı KIMLIĞI. Bu KIMLIK birden çok klonlama işlemini aynı anlık görüntüyü kullanacak şekilde bir araya getirir.
  - `[CloningInfoHostingEnvironment <String>]`: App Service ortamı.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> hedef uygulamanın üzerine yazmak için; Aksi takdirde <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Kaynak uygulama EX 'ın konumu: Batı ABD veya Kuzey Avrupa
  - `[CloningInfoTrafficManagerProfileId <String>]`: Varsa, kullanılacak Traffic Manager profilinin kaynak KIMLIĞI. Traffic Manager kaynak KIMLIĞI/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Oluşturulacak Traffic Manager profilinin adı. Bu yalnızca Traffic Manager profili yoksa gereklidir.
  - `[Config <ISiteConfig>]`: Uygulamanın yapılandırması.
    - `IsPushEnabled <Boolean>`: Itme uç noktasının etkinleştirilip etkinleştirilmediğini belirten bayrağı alır veya ayarlar.
    - `[ActionMinProcessExecutionTime <String>]`: İşlemin önüne geçmeden önce işlemin yürütülmesi gereken minimum süre
    - `[ActionType <AutoHealActionType?>]`: Önceden tanımlanmış eylem gerçekleştirilmelidir.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> her zaman açık etkinleştirilirse; Aksi takdirde <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: API tanımının URL 'SI.
    - `[ApiManagementConfigId <String>]`: APIM-Api tanımlayıcı.
    - `[AppCommandLine <String>]`: Başlatılacak uygulama komut satırı.
    - `[AppSetting <INameValuePair[]>]`: Uygulama ayarları.
      - `[Name <String>]`: Çift adı.
      - `[Value <String>]`: Çift değer.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> Otomatik Heal etkinleştirilmişse; Aksi takdirde <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Yuva adı otomatik takas et.
    - `[ConnectionString <IConnStringInfo[]>]`: Bağlantı dizeleri.
      - `[ConnectionString <String>]`: Bağlantı dizesi değeri.
      - `[Name <String>]`: Bağlantı dizesinin adı.
      - `[Type <ConnectionStringType?>]`: Veritabanı türü.
    - `[CorAllowedOrigin <String[]>]`: Çapraz kaynak çağrıları yapmasına izin verilmesi gereken kaynak listesini alır veya ayarlar (örneğin: http://example.com:12345) . Tümüne izin vermek için "*" kullanın.
    - `[CorSupportCredentials <Boolean?>]`: Kimlik bilgilerinin bulunduğu CORS isteklerine izin verilip verilmediğini alır veya ayarlar. https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsDaha fazla bilgi için bkz.
    - `[CustomActionExe <String>]`: Çalıştırılabilir dosya.
    - `[CustomActionParameter <String>]`: Çalıştırılabilirin parametreleri.
    - `[DefaultDocument <String[]>]`: Varsayılan belgeler.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> ayrıntılı hata günlüğü etkinleştirilmişse; Aksi takdirde <code>false</code> .
    - `[DocumentRoot <String>]`: Belge kökü.
    - `[DynamicTagsJson <String>]`: İtme kaydı uç noktasındaki Kullanıcı taleplerini değerlendirilecek dinamik etiket listesini içeren bir JSON dizesini alır veya ayarlar.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Rampa kuralları listesi.
      - `[ActionHostName <String>]`: Karar verirse trafiğin yönlendirileceği bir yuvanın ana bilgisayarı. Yani. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Özel karar algoritması, TiPCallback site uzantısında hangi URL belirtibileceğine sağlanabilir. Scaffold ve sözleşmeler için TiPCallback site uzantısına bakın.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage.
      - `[ChangeStep <Double?>]`: Otomatik artırma senaryosunda, bu, <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> veya         <code>MaxReroutePercentage</code> . Site ölçümleri, her N dakikada bir işaretlenmelidir <code>ChangeIntervalInMinutes</code> . \nözel karar algoritması, Ýpucu <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: ReroutePercentage 'in hangi üst sınıra kalacağını belirtir.
      - `[MinReroutePercentage <Double?>]`: ReroutePercentage 'in üzerinde kalacağı alt sınırı belirtir.
      - `[Name <String>]`: Yönlendirme kuralının adı. Önerilen ad, denemeler sırasında trafiği alacak olan yuvanın üzerine gelmek olacaktır.
      - `[ReroutePercentage <Double?>]`: Yönlendirileceği trafiğin yüzdesi <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: FTP/FTPS hizmetinin durumu
    - `[HandlerMapping <IHandlerMapping[]>]`: İşleyici eşlemeleri.
      - `[Argument <String>]`: Betik işlemcisine geçirilecek komut satırı bağımsız değişkenleri.
      - `[Extension <String>]`: Bu uzantıya sahip istekler belirtilen FastCGI uygulaması kullanılarak işlenecek.
      - `[ScriptProcessor <String>]`: FastCGI uygulamasının mutlak yolu.
    - `[HealthCheckPath <String>]`: Sağlık denetleme yolu
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: istemcilerin http 2.0 üzerinden bağlanmasına olanak tanımak için bir Web sitesi yapılandırır
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> http günlüğü etkinleştirilmişse; Aksi takdirde <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Main için IP güvenlik kısıtlamaları.
      - `[Action <String>]`: Bu IP aralığına erişim izni verin veya erişimi reddedin.
      - `[Description <String>]`: IP kısıtlama kuralı açıklaması.
      - `[IPAddress <String>]`: IP adresi güvenlik kısıtlamasının geçerlilik olduğu.         Saf IPv4 adresi (gerekli AltAğMaskesi özelliği) veya IPv4/maske (önde gelen bit eşleşmesi) gibi CıDR gösterimi biçiminde olabilir. CıDR için AltAğMaskesi özelliği belirtilmemelidir.
      - `[Name <String>]`: IP kısıtlama kuralı adı.
      - `[Priority <Int32?>]`: IP kısıtlama kuralının önceliği.
      - `[SubnetMask <String>]`: Kısıtlamanın geçerli olduğu IP adresi aralığı için alt ağ maskesi.
      - `[SubnetTrafficTag <Int32?>]`: (iç) alt ağ trafiği etiketi
      - `[Tag <IPFilterTag?>]`: Bu IP Filtresinin hangi şekilde kullanılacağını tanımlar. Bu, proxy 'lerde IP filtrelemesinin desteklenmesi için kullanılır.
      - `[VnetSubnetResourceId <String>]`: Sanal ağ kaynağı kimliği
      - `[VnetTrafficTag <Int32?>]`: (iç) VNET trafiği etiketi
    - `[JavaContainer <String>]`: Java kapsayıcısı.
    - `[JavaContainerVersion <String>]`: Java kapsayıcı sürümü.
    - `[JavaVersion <String>]`: Java sürümü.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: İzin verilen maksimum MB cinsinden disk boyutu kullanımı.
    - `[LimitMaxMemoryInMb <Int64?>]`: MB cinsinden izin verilen en fazla bellek kullanımı.
    - `[LimitMaxPercentageCpu <Double?>]`: İzin verilen en yüksek CPU kullanımı yüzdesi.
    - `[LinuxFxVersion <String>]`: Linux uygulama çerçevesi ve sürümü
    - `[LoadBalancing <SiteLoadBalancing?>]`: Site yük dengelemesi.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> Yerel MySQL 'yı etkinleştirmek için; Aksi takdirde <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP günlükleri Dizin boyutu sınırını aşıyor.
    - `[MachineKeyDecryption <String>]`: Şifre çözme için kullanılan algoritma.
    - `[MachineKeyDecryptionKey <String>]`: Şifre çözme anahtarı.
    - `[MachineKeyValidation <String>]`: MachineKey doğrulama.
    - `[MachineKeyValidationKey <String>]`: Geçerlilik anahtarı.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Yönetilen ardışık düzen modu.
    - `[ManagedServiceIdentityId <Int32?>]`: Yönetilen hizmet kimliği kimliği
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL istekleri için gereken en düşük TLS sürümünü yapılandırır
    - `[NetFrameworkVersion <String>]`: .NET Framework sürümü.
    - `[NodeVersion <String>]`: Node.js sürümü.
    - `[NumberOfWorker <Int32?>]`: Çalışan sayısı.
    - `[PhpVersion <String>]`: PHP sürümü.
    - `[PowerShellVersion <String>]`: PowerShell sürümü.
    - `[PreWarmedInstanceCount <Int32?>]`: Ön ödeme örneklerinin sayısı.         Bu ayar yalnızca tüketim ve esnek planlar için geçerlidir
    - `[PublishingUsername <String>]`: Kullanıcı adı yayımlanıyor.
    - `[PushKind <String>]`: Kaynak türü.
    - `[PythonVersion <String>]`: Python sürümü.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Uzaktan hata ayıklama etkinse; Aksi takdirde <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Uzaktan hata ayıklama sürümü.
    - `[RequestCount <Int32?>]`: İstek sayısı.
    - `[RequestTimeInterval <String>]`: Zaman aralığı.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> istek izleme etkinleştirilmişse; Aksi takdirde <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: İstek izleme süre sonu.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: SCM için IP güvenlik kısıtlamaları.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: SCM 'nin Main kullanması için IP güvenlik kısıtlamaları.
    - `[ScmType <ScmType?>]`: SCM türü.
    - `[SlowRequestCount <Int32?>]`: İstek sayısı.
    - `[SlowRequestTimeInterval <String>]`: Zaman aralığı.
    - `[SlowRequestTimeTaken <String>]`: Geçen süre.
    - `[TagWhitelistJson <String>]`: İtme kaydı uç noktası tarafından kullanılmak üzere, beyaz listelenen etiket listesini içeren bir JSON dizesini alır veya ayarlar.
    - `[TagsRequiringAuth <String>]`: İtme kaydı uç noktasında kullanılacak kullanıcı kimlik doğrulaması gerektiren etiket listesini içeren bir JSON dizesini alır veya ayarlar.         Etiketler alfasayısal karakterler ve aşağıdakiler: ' _ ', ' @ ', ' # ', '. ', ': ', '-'.         Doğrulama, PushRequestHandler ' de gerçekleştirilmelidir.
    - `[TracingOption <String>]`: İzleme seçenekleri.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Özel baytları temel alan bir kural.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Durum kodlarına dayalı bir kural.
      - `[Count <Int32?>]`: İstek sayısı.
      - `[Status <Int32?>]`: HTTP durum kodu.
      - `[SubStatus <Int32?>]`: Sub durumu talep edin.
      - `[TimeInterval <String>]`: Zaman aralığı.
      - `[Win32Status <Int32?>]`: Win32 hata kodu.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 bit çalışan işlemini kullanmak için; Aksi halde <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Sanal uygulamalar.
      - `[PhysicalPath <String>]`: Fiziksel yol.
      - `[PreloadEnabled <Boolean?>]`: önceden <code>true</code> önyüklemesi etkinleştirilmişse; Aksi takdirde <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Sanal uygulama için sanal dizinler.
        - `[PhysicalPath <String>]`: Fiziksel yol.
        - `[VirtualPath <String>]`: Sanal uygulamanın yolu.
      - `[VirtualPath <String>]`: Sanal yol.
    - `[VnetName <String>]`: Sanal ağ adı.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket etkinleştirilmişse; Aksi takdirde <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon App Framework ve sürümü
    - `[XManagedServiceIdentityId <Int32?>]`: Açık yönetilen hizmet kimliği kimliği
  - `[ContainerSize <Int32?>]`: İşlev kapsayıcısının boyutu.
  - `[DailyMemoryTimeQuota <Int32?>]`: İzin verilen maksimum günlük bellek süresi kotası (yalnızca dinamik uygulamalarda uygulanabilir).
  - `[Enabled <Boolean?>]`: <code>true</code> uygulama etkinleştirilmişse; Aksi takdirde <code>false</code> . Bu değeri false olarak ayarlamak uygulamayı devre dışı bırakır (uygulamayı çevrimdışı duruma getirin).
  - `[HostNameSslState <IHostNameSslState[]>]`: Ana bilgisayar adı SSL durumları, uygulamanın ana bilgisayar adlarının SSL bağlarını yönetmek için kullanılır.
    - `[HostType <HostType?>]`: Ana bilgisayar adının standart mı yoksa havuz ana bilgisayar adı mı olduğunu belirtir.
    - `[Name <String>]`Hostname.
    - `[SslState <SslState?>]`: SSL türü.
    - `[Thumbprint <String>]`: SSL sertifikası parmak izi.
    - `[ToUpdate <Boolean?>]`: <code>true</code> Var olan konak adını güncelleştirecek şekilde ayarla.
    - `[VirtualIP <String>]`: IP tabanlı SSL etkinleştirilmişse ana bilgisayar adına atanan sanal IP adresi.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> uygulamanın genel ana bilgisayar adlarını devre dışı bırakmak için; Aksi takdirde <code>false</code> .          Bu <code>true</code> uygulamaya yalnızca API yönetim işlemi aracılığıyla erişilebilir.
  - `[HostingEnvironmentProfileId <String>]`: App Service ortamının kaynak KIMLIĞI.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: yalnızca https isteklerini kabul edecek bir Web sitesi yapılandırır. Http isteklerini yeniden yönlendirme sorunları
  - `[HyperV <Boolean?>]`: Hyper-V korumalı alanı.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Yönetilen hizmet kimliğinin türü.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Kaynakla ilişkili kullanıcı kimliklerinin listesi. Kullanıcı kimliği sözlüğü anahtar başvurularının formda ARM kaynak kimlikleri olur: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.
  - `[IsXenon <Boolean?>]`: Geçersiz: Hyper-V korumalı alanı.
  - `[RedundancyMode <RedundancyMode?>]`: Site artıklık modu
  - `[Reserved <Boolean?>]`: <code>true</code> tahsis edilmişse; Aksi takdirde <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> uygulama DURDURULDUĞUNDA SCM (KUDU) sitesini durdurmak için; Aksi takdirde <code>false</code> . Varsayılan değer <code>false</code> .
  - `[ServerFarmId <String>]`: İlişkili App Service planının kaynak KIMLIĞI,: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}" olarak biçimlendirilir.

## ILGILI BAĞLANTıLAR

