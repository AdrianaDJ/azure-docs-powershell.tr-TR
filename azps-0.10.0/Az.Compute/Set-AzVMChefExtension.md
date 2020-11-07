---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 3bedeb243b79cada713889145771d45511cb7b7f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936842"
---
# <span data-ttu-id="2d086-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2d086-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="2d086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d086-102">SYNOPSIS</span></span>
<span data-ttu-id="2d086-103">Sanal makineye bir şef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="2d086-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="2d086-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d086-104">SYNTAX</span></span>

### <span data-ttu-id="2d086-105">UX</span><span class="sxs-lookup"><span data-stu-id="2d086-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d086-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="2d086-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d086-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d086-107">DESCRIPTION</span></span>
<span data-ttu-id="2d086-108">**Set-AzureVMChefExtension** cmdlet 'i sanal makineye Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="2d086-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="2d086-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d086-109">EXAMPLES</span></span>

### <span data-ttu-id="2d086-110">Örnek 1: Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="2d086-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="2d086-111">Bu komut, WindowsVM001 adındaki Windows sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="2d086-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="2d086-112">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="2d086-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2d086-113">Örnek 2: Linux sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="2d086-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="2d086-114">Bu komut, LinuxVM001 adındaki bir Linux sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="2d086-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="2d086-115">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="2d086-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2d086-116">Örnek 3: önyükleme seçenekleriyle Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="2d086-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="2d086-117">Bu komut, WindowsVM002 adlı bir Windows sanal makinesine Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="2d086-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="2d086-118">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="2d086-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="2d086-119">Önyükleme sonrasında, sanal makine JSON biçiminde belirtilen BootstrapOptions 'e başvurur.</span><span class="sxs-lookup"><span data-stu-id="2d086-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="2d086-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d086-120">PARAMETERS</span></span>

### <span data-ttu-id="2d086-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2d086-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="2d086-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="2d086-122">-BootstrapOptions</span></span>
<span data-ttu-id="2d086-123">Client_rb seçeneğinde yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="2d086-124">-Bootstrapsürümü</span><span class="sxs-lookup"><span data-stu-id="2d086-124">-BootstrapVersion</span></span>
<span data-ttu-id="2d086-125">Önyükleme yapılandırmasının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="2d086-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="2d086-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="2d086-127">Çef-hizmetin çalıştığı sıklığı (dakika cinsinden) belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="2d086-128">Bu durumda, hizmetin Azure VM 'de yüklü olmasını istemiyorsanız, bu alanda değeri 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2d086-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="2d086-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="2d086-129">-ChefServerUrl</span></span>
<span data-ttu-id="2d086-130">URL olarak Chef sunucu bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="2d086-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="2d086-131">-ClientRb</span></span>
<span data-ttu-id="2d086-132">Chef istemcisinin tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="2d086-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="2d086-133">-Daemon</span></span>
<span data-ttu-id="2d086-134">Katılımsız yürütme için Chef-Client hizmetini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="2d086-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="2d086-135">Düğüm platformu Windows olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2d086-135">The node platform should be Windows.</span></span>
<span data-ttu-id="2d086-136">İzin verilen seçenekler: ' none ', ' Service ' ve ' Task '.</span><span class="sxs-lookup"><span data-stu-id="2d086-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="2d086-137">yok-şu anda Chef-Client hizmetinin bir hizmet olarak yapılandırılmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="2d086-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="2d086-138">hizmet-istemci arka planda otomatik olarak çalışmak için Chef-Client yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="2d086-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="2d086-139">Görev: Chef-Client 'ı, yarı bir görev olarak arka planda otomatik olarak çalışacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="2d086-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="2d086-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d086-140">-DefaultProfile</span></span>
<span data-ttu-id="2d086-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d086-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d086-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="2d086-142">-JsonAttribute</span></span>
<span data-ttu-id="2d086-143">Chef-Client ' A ilk çalıştırmaya eklenecek bir JSON dizesi.</span><span class="sxs-lookup"><span data-stu-id="2d086-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="2d086-144">Örneğin,-JsonAttribute ' {"foo": "çubuk"} '</span><span class="sxs-lookup"><span data-stu-id="2d086-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="2d086-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="2d086-145">-Linux</span></span>
<span data-ttu-id="2d086-146">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d086-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="2d086-147">-Konum</span><span class="sxs-lookup"><span data-stu-id="2d086-147">-Location</span></span>
<span data-ttu-id="2d086-148">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2d086-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d086-149">-Name</span></span>
<span data-ttu-id="2d086-150">Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="2d086-151">-OrganizasyonAdı</span><span class="sxs-lookup"><span data-stu-id="2d086-151">-OrganizationName</span></span>
<span data-ttu-id="2d086-152">Chef uzantısının kuruluş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="2d086-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d086-153">-ResourceGroupName</span></span>
<span data-ttu-id="2d086-154">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="2d086-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="2d086-155">-RunList</span></span>
<span data-ttu-id="2d086-156">Chef düğümü çalışma listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="2d086-157">-Parola</span><span class="sxs-lookup"><span data-stu-id="2d086-157">-Secret</span></span>
<span data-ttu-id="2d086-158">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="2d086-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="2d086-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="2d086-159">-SecretFile</span></span>
<span data-ttu-id="2d086-160">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="2d086-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="2d086-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2d086-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="2d086-162">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-162">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="2d086-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="2d086-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="2d086-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="2d086-164">-ValidationPem</span></span>
<span data-ttu-id="2d086-165">Chef doğrulayıcısı. pem dosya yolunu belirtir</span><span class="sxs-lookup"><span data-stu-id="2d086-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="2d086-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="2d086-166">-VMName</span></span>
<span data-ttu-id="2d086-167">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d086-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2d086-168">Bu cmdlet, bu parametrenin belirttiği sanal makine için Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="2d086-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2d086-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="2d086-169">-Windows</span></span>
<span data-ttu-id="2d086-170">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d086-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="2d086-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d086-171">-Confirm</span></span>
<span data-ttu-id="2d086-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d086-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d086-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d086-173">-WhatIf</span></span>
<span data-ttu-id="2d086-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d086-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2d086-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d086-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d086-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d086-176">CommonParameters</span></span>
<span data-ttu-id="2d086-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d086-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d086-178">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d086-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d086-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d086-179">INPUTS</span></span>

### <span data-ttu-id="2d086-180">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2d086-180">None</span></span>
<span data-ttu-id="2d086-181">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2d086-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d086-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d086-182">OUTPUTS</span></span>

### <span data-ttu-id="2d086-183">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2d086-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2d086-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d086-184">NOTES</span></span>

## <span data-ttu-id="2d086-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d086-185">RELATED LINKS</span></span>

[<span data-ttu-id="2d086-186">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2d086-186">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="2d086-187">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2d086-187">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
