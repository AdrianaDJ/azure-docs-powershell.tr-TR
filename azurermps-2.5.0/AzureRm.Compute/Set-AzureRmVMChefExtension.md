---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: 277790badbaeef02139034ffd32f639f90929133
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939939"
---
# <span data-ttu-id="f2280-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2280-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="f2280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2280-102">SYNOPSIS</span></span>
<span data-ttu-id="f2280-103">Sanal makineye bir şef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="f2280-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2280-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2280-104">SYNTAX</span></span>

### <span data-ttu-id="f2280-105">UX</span><span class="sxs-lookup"><span data-stu-id="f2280-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2280-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="f2280-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2280-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2280-107">DESCRIPTION</span></span>
<span data-ttu-id="f2280-108">**Set-AzureVMChefExtension** cmdlet 'i sanal makineye Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2280-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="f2280-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2280-109">EXAMPLES</span></span>

### <span data-ttu-id="f2280-110">Örnek 1: Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f2280-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="f2280-111">Bu komut, WindowsVM001 adındaki Windows sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="f2280-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="f2280-112">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="f2280-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="f2280-113">Örnek 2: Linux sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f2280-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="f2280-114">Bu komut, LinuxVM001 adındaki bir Linux sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="f2280-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="f2280-115">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="f2280-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="f2280-116">Örnek 3: önyükleme seçenekleriyle Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f2280-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="f2280-117">Bu komut, WindowsVM002 adlı bir Windows sanal makinesine Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2280-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="f2280-118">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="f2280-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="f2280-119">Önyükleme sonrasında, sanal makine JSON biçiminde belirtilen BootstrapOptions 'e başvurur.</span><span class="sxs-lookup"><span data-stu-id="f2280-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="f2280-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2280-120">PARAMETERS</span></span>

### <span data-ttu-id="f2280-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f2280-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="f2280-122">-BootstrapOptions</span></span>
<span data-ttu-id="f2280-123">Client_rb seçeneğinde yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="f2280-124">-Bootstrapsürümü</span><span class="sxs-lookup"><span data-stu-id="f2280-124">-BootstrapVersion</span></span>
<span data-ttu-id="f2280-125">Önyükleme yapılandırmasının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="f2280-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="f2280-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="f2280-127">Çef-hizmetin çalıştığı sıklığı (dakika cinsinden) belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="f2280-128">Bu durumda, hizmetin Azure VM 'de yüklü olmasını istemiyorsanız, bu alanda değeri 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f2280-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="f2280-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="f2280-129">-ChefServerUrl</span></span>
<span data-ttu-id="f2280-130">URL olarak Chef sunucu bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="f2280-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="f2280-131">-ClientRb</span></span>
<span data-ttu-id="f2280-132">Chef istemcisinin tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="f2280-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="f2280-133">-Daemon</span></span>
<span data-ttu-id="f2280-134">Katılımsız yürütme için Chef-Client hizmetini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="f2280-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="f2280-135">Düğüm platformu Windows olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f2280-135">The node platform should be Windows.</span></span>
<span data-ttu-id="f2280-136">İzin verilen seçenekler: ' none ', ' Service ' ve ' Task '.</span><span class="sxs-lookup"><span data-stu-id="f2280-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="f2280-137">yok-şu anda Chef-Client hizmetinin bir hizmet olarak yapılandırılmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="f2280-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="f2280-138">hizmet-istemci arka planda otomatik olarak çalışmak için Chef-Client yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="f2280-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="f2280-139">Görev: Chef-Client 'ı, yarı bir görev olarak arka planda otomatik olarak çalışacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="f2280-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2280-140">-DefaultProfile</span></span>
<span data-ttu-id="f2280-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2280-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="f2280-142">-JsonAttribute</span></span>
<span data-ttu-id="f2280-143">Chef-Client ' A ilk çalıştırmaya eklenecek bir JSON dizesi.</span><span class="sxs-lookup"><span data-stu-id="f2280-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="f2280-144">Örneğin,-JsonAttribute ' {"foo": "çubuk"} '</span><span class="sxs-lookup"><span data-stu-id="f2280-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="f2280-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="f2280-145">-Linux</span></span>
<span data-ttu-id="f2280-146">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2280-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="f2280-147">-Konum</span><span class="sxs-lookup"><span data-stu-id="f2280-147">-Location</span></span>
<span data-ttu-id="f2280-148">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2280-149">-Name</span></span>
<span data-ttu-id="f2280-150">Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-151">-OrganizasyonAdı</span><span class="sxs-lookup"><span data-stu-id="f2280-151">-OrganizationName</span></span>
<span data-ttu-id="f2280-152">Chef uzantısının kuruluş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="f2280-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2280-153">-ResourceGroupName</span></span>
<span data-ttu-id="f2280-154">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f2280-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="f2280-155">-RunList</span></span>
<span data-ttu-id="f2280-156">Chef düğümü çalışma listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="f2280-157">-Parola</span><span class="sxs-lookup"><span data-stu-id="f2280-157">-Secret</span></span>
<span data-ttu-id="f2280-158">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="f2280-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f2280-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="f2280-159">-SecretFile</span></span>
<span data-ttu-id="f2280-160">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="f2280-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f2280-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f2280-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="f2280-162">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-162">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="f2280-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="f2280-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="f2280-164">-ValidationPem</span></span>
<span data-ttu-id="f2280-165">Chef doğrulayıcısı. pem dosya yolunu belirtir</span><span class="sxs-lookup"><span data-stu-id="f2280-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="f2280-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2280-166">-VMName</span></span>
<span data-ttu-id="f2280-167">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2280-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f2280-168">Bu cmdlet, bu parametrenin belirttiği sanal makine için Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f2280-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="f2280-169">-Windows</span></span>
<span data-ttu-id="f2280-170">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2280-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="f2280-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2280-171">-Confirm</span></span>
<span data-ttu-id="f2280-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2280-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2280-173">-WhatIf</span></span>
<span data-ttu-id="f2280-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2280-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f2280-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2280-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2280-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2280-176">CommonParameters</span></span>
<span data-ttu-id="f2280-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2280-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2280-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2280-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2280-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2280-179">INPUTS</span></span>

### <span data-ttu-id="f2280-180">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f2280-180">None</span></span>
<span data-ttu-id="f2280-181">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f2280-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2280-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2280-182">OUTPUTS</span></span>

### <span data-ttu-id="f2280-183">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2280-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f2280-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2280-184">NOTES</span></span>

## <span data-ttu-id="f2280-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2280-185">RELATED LINKS</span></span>

[<span data-ttu-id="f2280-186">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2280-186">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="f2280-187">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2280-187">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
