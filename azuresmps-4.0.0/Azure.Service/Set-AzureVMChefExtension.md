---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106045"
---
# <span data-ttu-id="f2405-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2405-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="f2405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2405-102">SYNOPSIS</span></span>
<span data-ttu-id="f2405-103">Sanal makineye Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2405-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="f2405-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2405-104">SYNTAX</span></span>

### <span data-ttu-id="f2405-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2405-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2405-106">UX</span><span class="sxs-lookup"><span data-stu-id="f2405-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2405-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2405-107">DESCRIPTION</span></span>
<span data-ttu-id="f2405-108">**Set-AzureVMChefExtension** cmdlet 'i sanal makineye Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2405-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="f2405-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2405-109">EXAMPLES</span></span>

### <span data-ttu-id="f2405-110">Örnek 1: Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f2405-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="f2405-111">Bu komut Windows sanal makinesine bir şef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="f2405-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="f2405-112">Sanal makine geldiğinde, bootstrapped ve üzerinde Apache çalışır.</span><span class="sxs-lookup"><span data-stu-id="f2405-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="f2405-113">Örnek 2: önyükleme içeren Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f2405-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="f2405-114">Bu komut, Windows sanal makinesine Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2405-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="f2405-115">Sanal makine başlatıldığında, bootstrapped ve üzerinde Apache çalışır.</span><span class="sxs-lookup"><span data-stu-id="f2405-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="f2405-116">Önyükleme sonrasında, sanal makine JSON biçiminde belirtilen *BootstrapOptions* 'e başvurur.</span><span class="sxs-lookup"><span data-stu-id="f2405-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="f2405-117">Örnek 3: Windows sanal makinesine bir GEF uzantısı ekleme ve Apache ve GIT 'i yükleme</span><span class="sxs-lookup"><span data-stu-id="f2405-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="f2405-118">Bu komut, Windows sanal makinesine Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2405-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="f2405-119">Sanal makine başlatıldığında, bootstrapped ve Apache ve GIT yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f2405-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="f2405-120">Client. RB 'yi belirtmezseniz, Chef sunucu URL 'sini ve doğrulama istemci adını sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f2405-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="f2405-121">Örnek 4: Linux sanal makinesine Chef uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f2405-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="f2405-122">Bu komut, bir Linux sanal makinesine Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2405-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="f2405-123">Sanal makine başlatıldığında, bootstrapped.</span><span class="sxs-lookup"><span data-stu-id="f2405-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="f2405-124">Client. RB 'yi belirtmezseniz, Chef sunucu URL 'sini ve kuruluşunu sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f2405-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="f2405-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2405-125">PARAMETERS</span></span>

### <span data-ttu-id="f2405-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="f2405-126">-BootstrapOptions</span></span>
<span data-ttu-id="f2405-127">JavaScript nesne gösterimi (JSON) biçimindeki önyükleme seçeneklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="f2405-128">-Bootstrapsürümü</span><span class="sxs-lookup"><span data-stu-id="f2405-128">-BootstrapVersion</span></span>
<span data-ttu-id="f2405-129">Uzantıyla birlikte yüklenen Chef istemcisi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="f2405-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="f2405-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="f2405-131">Çef-hizmetin çalıştığı sıklığı (dakika cinsinden) belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="f2405-132">Bu durumda, hizmetin Azure VM 'de yüklü olmasını istemiyorsanız, bu alanda değeri 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f2405-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2405-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="f2405-133">-ChefServerUrl</span></span>
<span data-ttu-id="f2405-134">Chef sunucusunun URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="f2405-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="f2405-135">-ClientRb</span></span>
<span data-ttu-id="f2405-136">Chef istemcisinin tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="f2405-137">-Daemon</span><span class="sxs-lookup"><span data-stu-id="f2405-137">-Daemon</span></span>
<span data-ttu-id="f2405-138">Katılımsız yürütme için Chef-Client hizmetini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="f2405-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="f2405-139">Düğüm platformu Windows olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f2405-139">The node platform should be Windows.</span></span>
<span data-ttu-id="f2405-140">İzin verilen seçenekler: ' none ', ' Service ' ve ' Task '.</span><span class="sxs-lookup"><span data-stu-id="f2405-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="f2405-141">yok-şu anda Chef-Client hizmetinin bir hizmet olarak yapılandırılmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="f2405-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="f2405-142">hizmet-istemci arka planda otomatik olarak çalışmak için Chef-Client yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="f2405-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="f2405-143">Görev: Chef-Client 'ı, yarı bir görev olarak arka planda otomatik olarak çalışacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="f2405-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="f2405-144">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f2405-144">-InformationAction</span></span>
<span data-ttu-id="f2405-145">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2405-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f2405-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2405-147">'A</span><span class="sxs-lookup"><span data-stu-id="f2405-147">Continue</span></span>
- <span data-ttu-id="f2405-148">Manıza</span><span class="sxs-lookup"><span data-stu-id="f2405-148">Ignore</span></span>
- <span data-ttu-id="f2405-149">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f2405-149">Inquire</span></span>
- <span data-ttu-id="f2405-150">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f2405-150">SilentlyContinue</span></span>
- <span data-ttu-id="f2405-151">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f2405-151">Stop</span></span>
- <span data-ttu-id="f2405-152">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f2405-152">Suspend</span></span>

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

### <span data-ttu-id="f2405-153">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f2405-153">-InformationVariable</span></span>
<span data-ttu-id="f2405-154">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-154">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2405-155">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="f2405-155">-JsonAttribute</span></span>
<span data-ttu-id="f2405-156">Chef-Client ' A ilk çalıştırmaya eklenecek bir JSON dizesi.</span><span class="sxs-lookup"><span data-stu-id="f2405-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="f2405-157">Örneğin,-JsonAttribute ' {"foo": "çubuk"} '</span><span class="sxs-lookup"><span data-stu-id="f2405-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="f2405-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="f2405-158">-Linux</span></span>
<span data-ttu-id="f2405-159">Bu cmdlet 'in Linux tabanlı bir sanal makine oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2405-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="f2405-160">-OrganizasyonAdı</span><span class="sxs-lookup"><span data-stu-id="f2405-160">-OrganizationName</span></span>
<span data-ttu-id="f2405-161">Chef uzantısının kuruluş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="f2405-162">-Profil</span><span class="sxs-lookup"><span data-stu-id="f2405-162">-Profile</span></span>
<span data-ttu-id="f2405-163">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2405-164">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f2405-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2405-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="f2405-165">-RunList</span></span>
<span data-ttu-id="f2405-166">Chef düğümü çalışma listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="f2405-167">-Parola</span><span class="sxs-lookup"><span data-stu-id="f2405-167">-Secret</span></span>
<span data-ttu-id="f2405-168">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="f2405-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f2405-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="f2405-169">-SecretFile</span></span>
<span data-ttu-id="f2405-170">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="f2405-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f2405-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="f2405-171">-ValidationClientName</span></span>
<span data-ttu-id="f2405-172">Doğrulama istemcisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="f2405-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="f2405-173">-ValidationPem</span></span>
<span data-ttu-id="f2405-174">Chef doğrulayıcısı. pem dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-174">Specifies the Chef validator .pem file path.</span></span>

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

### <span data-ttu-id="f2405-175">-Version</span><span class="sxs-lookup"><span data-stu-id="f2405-175">-Version</span></span>
<span data-ttu-id="f2405-176">Chef uzantısının sürüm numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="f2405-177">-VM</span><span class="sxs-lookup"><span data-stu-id="f2405-177">-VM</span></span>
<span data-ttu-id="f2405-178">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2405-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2405-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="f2405-179">-Windows</span></span>
<span data-ttu-id="f2405-180">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2405-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="f2405-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2405-181">CommonParameters</span></span>
<span data-ttu-id="f2405-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2405-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2405-183">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2405-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2405-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2405-184">INPUTS</span></span>

## <span data-ttu-id="f2405-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2405-185">OUTPUTS</span></span>

## <span data-ttu-id="f2405-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2405-186">NOTES</span></span>

## <span data-ttu-id="f2405-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2405-187">RELATED LINKS</span></span>

[<span data-ttu-id="f2405-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2405-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="f2405-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2405-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


