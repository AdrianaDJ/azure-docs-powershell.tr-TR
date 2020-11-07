---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 22efab85694d7d2af359052b264a9aa932816f4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752695"
---
# <span data-ttu-id="e3b9a-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="e3b9a-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="e3b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b9a-103">Sanal makineye bir şef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="e3b9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3b9a-104">SYNTAX</span></span>

### <span data-ttu-id="e3b9a-105">UX</span><span class="sxs-lookup"><span data-stu-id="e3b9a-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b9a-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="e3b9a-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b9a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3b9a-107">DESCRIPTION</span></span>
<span data-ttu-id="e3b9a-108">**Set-AzVMChefExtension** cmdlet 'i sanal makineye Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="e3b9a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3b9a-109">EXAMPLES</span></span>

### <span data-ttu-id="e3b9a-110">Örnek 1: Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3b9a-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="e3b9a-111">Bu komut, WindowsVM001 adındaki Windows sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="e3b9a-112">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="e3b9a-113">Örnek 2: Linux sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3b9a-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="e3b9a-114">Bu komut, LinuxVM001 adındaki bir Linux sanal makinesine bir Çef uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="e3b9a-115">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="e3b9a-116">Örnek 3: önyükleme seçenekleriyle Windows sanal makinesine bir GEF uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="e3b9a-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="e3b9a-117">Bu komut, WindowsVM002 adlı bir Windows sanal makinesine Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="e3b9a-118">Sanal makine başlatıldığında, sanal makineyi Apache çalıştırmak için Bootstraps.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="e3b9a-119">Önyükleme sonrasında, sanal makine JSON biçiminde belirtilen BootstrapOptions 'e başvurur.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="e3b9a-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3b9a-120">PARAMETERS</span></span>

### <span data-ttu-id="e3b9a-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e3b9a-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="e3b9a-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="e3b9a-122">-BootstrapOptions</span></span>
<span data-ttu-id="e3b9a-123">Client_rb seçeneğinde yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="e3b9a-124">-Bootstrapsürümü</span><span class="sxs-lookup"><span data-stu-id="e3b9a-124">-BootstrapVersion</span></span>
<span data-ttu-id="e3b9a-125">Önyükleme yapılandırmasının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="e3b9a-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="e3b9a-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="e3b9a-127">Çef-hizmetin çalıştığı sıklığı (dakika cinsinden) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="e3b9a-128">Bu durumda, hizmetin Azure VM 'de yüklü olmasını istemiyorsanız, bu alanda değeri 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="e3b9a-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="e3b9a-129">-ChefServerUrl</span></span>
<span data-ttu-id="e3b9a-130">URL olarak Chef sunucu bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="e3b9a-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="e3b9a-131">-ClientRb</span></span>
<span data-ttu-id="e3b9a-132">Chef istemcisinin tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="e3b9a-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="e3b9a-133">-Daemon</span></span>
<span data-ttu-id="e3b9a-134">Katılımsız yürütme için Chef-Client hizmetini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="e3b9a-135">Düğüm platformu Windows olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-135">The node platform should be Windows.</span></span>
<span data-ttu-id="e3b9a-136">İzin verilen seçenekler: ' none ', ' Service ' ve ' Task '.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="e3b9a-137">yok-şu anda Chef-Client hizmetinin bir hizmet olarak yapılandırılmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="e3b9a-138">hizmet-istemci arka planda otomatik olarak çalışmak için Chef-Client yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="e3b9a-139">Görev: Chef-istemciyi, arka planda zamanlanmış görev olarak otomatik olarak çalışacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

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

### <span data-ttu-id="e3b9a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b9a-140">-DefaultProfile</span></span>
<span data-ttu-id="e3b9a-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b9a-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="e3b9a-142">-JsonAttribute</span></span>
<span data-ttu-id="e3b9a-143">Chef-Client ' A ilk çalıştırmaya eklenecek bir JSON dizesi.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="e3b9a-144">Örneğin,-JsonAttribute ' {"foo": "çubuk"} '</span><span class="sxs-lookup"><span data-stu-id="e3b9a-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="e3b9a-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="e3b9a-145">-Linux</span></span>
<span data-ttu-id="e3b9a-146">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="e3b9a-147">-Konum</span><span class="sxs-lookup"><span data-stu-id="e3b9a-147">-Location</span></span>
<span data-ttu-id="e3b9a-148">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="e3b9a-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3b9a-149">-Name</span></span>
<span data-ttu-id="e3b9a-150">Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="e3b9a-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e3b9a-151">-NoWait</span></span>
<span data-ttu-id="e3b9a-152">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e3b9a-153">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e3b9a-154">-OrganizasyonAdı</span><span class="sxs-lookup"><span data-stu-id="e3b9a-154">-OrganizationName</span></span>
<span data-ttu-id="e3b9a-155">Chef uzantısının kuruluş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="e3b9a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b9a-156">-ResourceGroupName</span></span>
<span data-ttu-id="e3b9a-157">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="e3b9a-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="e3b9a-158">-RunList</span></span>
<span data-ttu-id="e3b9a-159">Chef düğümü çalışma listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="e3b9a-160">-Parola</span><span class="sxs-lookup"><span data-stu-id="e3b9a-160">-Secret</span></span>
<span data-ttu-id="e3b9a-161">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="e3b9a-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="e3b9a-162">-SecretFile</span></span>
<span data-ttu-id="e3b9a-163">Veri paketi öğe değerlerini şifrelemek ve şifrelerini çözmek için kullanılan şifreleme anahtarını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="e3b9a-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e3b9a-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="e3b9a-165">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-165">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="e3b9a-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="e3b9a-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="e3b9a-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="e3b9a-167">-ValidationPem</span></span>
<span data-ttu-id="e3b9a-168">Chef doğrulayıcısı. pem dosya yolunu belirtir</span><span class="sxs-lookup"><span data-stu-id="e3b9a-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="e3b9a-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="e3b9a-169">-VMName</span></span>
<span data-ttu-id="e3b9a-170">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e3b9a-171">Bu cmdlet, bu parametrenin belirttiği sanal makine için Chef uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3b9a-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="e3b9a-172">-Windows</span></span>
<span data-ttu-id="e3b9a-173">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="e3b9a-174">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3b9a-174">-Confirm</span></span>
<span data-ttu-id="e3b9a-175">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b9a-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b9a-176">-WhatIf</span></span>
<span data-ttu-id="e3b9a-177">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b9a-178">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b9a-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b9a-179">CommonParameters</span></span>
<span data-ttu-id="e3b9a-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b9a-181">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e3b9a-181">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b9a-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3b9a-182">INPUTS</span></span>

### <span data-ttu-id="e3b9a-183">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b9a-183">System.String</span></span>

### <span data-ttu-id="e3b9a-184">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3b9a-184">System.Boolean</span></span>

## <span data-ttu-id="e3b9a-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3b9a-185">OUTPUTS</span></span>

### <span data-ttu-id="e3b9a-186">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e3b9a-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e3b9a-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3b9a-187">NOTES</span></span>

## <span data-ttu-id="e3b9a-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3b9a-188">RELATED LINKS</span></span>

[<span data-ttu-id="e3b9a-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="e3b9a-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="e3b9a-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="e3b9a-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
