---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: d0c63c0cba3c895ebdea92822a05c4d1f9c15056
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586933"
---
# <span data-ttu-id="09cf4-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="09cf4-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="09cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="09cf4-103">Sanal makineye bir şef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="09cf4-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09cf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09cf4-104">SYNTAX</span></span>

### <span data-ttu-id="09cf4-105">UX</span><span class="sxs-lookup"><span data-stu-id="09cf4-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09cf4-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="09cf4-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09cf4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="09cf4-107">DESCRIPTION</span></span>
<span data-ttu-id="09cf4-108">**Set-AzureVMChefExtension** cmdlet 'i sanal makineye Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="09cf4-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="09cf4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09cf4-109">EXAMPLES</span></span>

### <span data-ttu-id="09cf4-110">Örnek 1: Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="09cf4-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="09cf4-111">Bu komut, WindowsVM001 adındaki Windows sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="09cf4-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="09cf4-112">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="09cf4-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="09cf4-113">Örnek 2: Linux sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="09cf4-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="09cf4-114">Bu komut, LinuxVM001 adındaki bir Linux sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="09cf4-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="09cf4-115">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="09cf4-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="09cf4-116">Örnek 3: önyükleme seçenekleriyle Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="09cf4-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="09cf4-117">Bu komut, WindowsVM002 adlı bir Windows sanal makinesine Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="09cf4-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="09cf4-118">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="09cf4-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="09cf4-119">Önyükleme sonrasında, sanal makine JSON biçiminde belirtilen BootstrapOptions 'e başvurur.</span><span class="sxs-lookup"><span data-stu-id="09cf4-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="09cf4-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09cf4-120">PARAMETERS</span></span>

### <span data-ttu-id="09cf4-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="09cf4-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="09cf4-122">-BootstrapOptions</span></span>
<span data-ttu-id="09cf4-123">Client_rb seçeneğinde yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-124">-Bootstrapsürümü</span><span class="sxs-lookup"><span data-stu-id="09cf4-124">-BootstrapVersion</span></span>
<span data-ttu-id="09cf4-125">Önyükleme yapılandırmasının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="09cf4-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="09cf4-127">Çef-hizmetin çalıştığı sıklığı (dakika cinsinden) belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="09cf4-128">Bu durumda, hizmetin Azure VM 'de yüklü olmasını istemiyorsanız, bu alanda değeri 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="09cf4-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="09cf4-129">-ChefServerUrl</span></span>
<span data-ttu-id="09cf4-130">URL olarak Chef sunucu bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="09cf4-131">-ClientRb</span></span>
<span data-ttu-id="09cf4-132">Chef istemcisinin tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="09cf4-133">-Daemon</span></span>
<span data-ttu-id="09cf4-134">Katılımsız yürütme için Chef-Client hizmetini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="09cf4-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="09cf4-135">Düğüm platformu Windows olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="09cf4-135">The node platform should be Windows.</span></span>
<span data-ttu-id="09cf4-136">İzin verilen seçenekler: ' none ', ' Service ' ve ' Task '.</span><span class="sxs-lookup"><span data-stu-id="09cf4-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="09cf4-137">yok-şu anda Chef-Client hizmetinin bir hizmet olarak yapılandırılmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="09cf4-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="09cf4-138">hizmet-istemci arka planda otomatik olarak çalışmak için Chef-Client yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="09cf4-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="09cf4-139">Görev: Chef-Client 'ı, yarı bir görev olarak arka planda otomatik olarak çalışacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="09cf4-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09cf4-140">-DefaultProfile</span></span>
<span data-ttu-id="09cf4-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09cf4-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09cf4-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="09cf4-142">-JsonAttribute</span></span>
<span data-ttu-id="09cf4-143">Chef-Client ' A ilk çalıştırmaya eklenecek bir JSON dizesi.</span><span class="sxs-lookup"><span data-stu-id="09cf4-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="09cf4-144">Örneğin,-JsonAttribute ' {"foo": "çubuk"} '</span><span class="sxs-lookup"><span data-stu-id="09cf4-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="09cf4-145">-Linux</span></span>
<span data-ttu-id="09cf4-146">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-147">-Konum</span><span class="sxs-lookup"><span data-stu-id="09cf4-147">-Location</span></span>
<span data-ttu-id="09cf4-148">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="09cf4-149">-Name</span></span>
<span data-ttu-id="09cf4-150">Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-151">-OrganizasyonAdı</span><span class="sxs-lookup"><span data-stu-id="09cf4-151">-OrganizationName</span></span>
<span data-ttu-id="09cf4-152">Chef uzantısının kuruluş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-152">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09cf4-153">-ResourceGroupName</span></span>
<span data-ttu-id="09cf4-154">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="09cf4-155">-RunList</span></span>
<span data-ttu-id="09cf4-156">Chef düğümü çalışma listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-156">Specifies the Chef node run list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-157">-Parola</span><span class="sxs-lookup"><span data-stu-id="09cf4-157">-Secret</span></span>
<span data-ttu-id="09cf4-158">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="09cf4-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="09cf4-159">-SecretFile</span></span>
<span data-ttu-id="09cf4-160">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="09cf4-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="09cf4-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="09cf4-162">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-162">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="09cf4-163">-ValidationClientName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="09cf4-164">-ValidationPem</span></span>
<span data-ttu-id="09cf4-165">Chef doğrulayıcısı. pem dosya yolunu belirtir</span><span class="sxs-lookup"><span data-stu-id="09cf4-165">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="09cf4-166">-VMName</span></span>
<span data-ttu-id="09cf4-167">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="09cf4-168">Bu cmdlet, bu parametrenin belirttiği sanal makine için Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="09cf4-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="09cf4-169">-Windows</span></span>
<span data-ttu-id="09cf4-170">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cf4-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="09cf4-171">-Confirm</span></span>
<span data-ttu-id="09cf4-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09cf4-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09cf4-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09cf4-173">-WhatIf</span></span>
<span data-ttu-id="09cf4-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09cf4-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="09cf4-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09cf4-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09cf4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cf4-176">CommonParameters</span></span>
<span data-ttu-id="09cf4-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09cf4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cf4-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09cf4-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cf4-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09cf4-179">INPUTS</span></span>

## <span data-ttu-id="09cf4-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09cf4-180">OUTPUTS</span></span>

## <span data-ttu-id="09cf4-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09cf4-181">NOTES</span></span>

## <span data-ttu-id="09cf4-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09cf4-182">RELATED LINKS</span></span>

[<span data-ttu-id="09cf4-183">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="09cf4-183">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="09cf4-184">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="09cf4-184">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
