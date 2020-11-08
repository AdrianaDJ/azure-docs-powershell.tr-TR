---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106382"
---
# <span data-ttu-id="bad56-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="bad56-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="bad56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bad56-102">SYNOPSIS</span></span>
<span data-ttu-id="bad56-103">Azure sanal makinesi için sağlama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="bad56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bad56-104">SYNTAX</span></span>

### <span data-ttu-id="bad56-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bad56-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bad56-106">UX</span><span class="sxs-lookup"><span data-stu-id="bad56-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bad56-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="bad56-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bad56-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bad56-108">DESCRIPTION</span></span>
<span data-ttu-id="bad56-109">**Add-AzureProvisioningConfig** cmdlet 'ı bir Azure sanal makine yapılandırmasına sağlama yapılandırma bilgilerini ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="bad56-110">Sanal makine oluşturmak için yapılandırma nesnesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bad56-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="bad56-111">Bu cmdlet tek başına Windows sunucuları, Active Directory etki alanına bağlı Windows sunucuları ve Linux tabanlı sunucular gibi farklı sağlama yapılandırmalarını destekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="bad56-112">Active Directory etki alanı Birleşik sunucusu oluşturmak için, Active Directory etki alanının tam etki alanı adını ve sanal makineye etki alanına katılma izni olan bir kullanıcının etki alanı kimlik bilgilerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="bad56-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="bad56-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bad56-113">EXAMPLES</span></span>

### <span data-ttu-id="bad56-114">Örnek 1: tek başına sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bad56-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="bad56-115">Bu komut, **New-AzureVMConfig** cmdlet 'ini kullanarak bir sanal makine yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bad56-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="bad56-116">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bad56-117">Geçerli cmdlet, Windows işletim sistemini çalıştıran bir sanal makine için sağlama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="bad56-118">Yapılandırma, yönetici kullanıcı adını ve parolasını içerir.</span><span class="sxs-lookup"><span data-stu-id="bad56-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="bad56-119">Komut, yapılandırmayı sanal makineyi oluşturan **New-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="bad56-120">Örnek 2: etki alanına bağlı bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bad56-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="bad56-121">Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bad56-122">Geçerli cmdlet, contoso etki alanına katılması için bir sanal makinenin sağlama yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="bad56-123">Bu komut, sanal makineye etki alanına katılmak için gereken kullanıcı adını ve parolayı içerir.</span><span class="sxs-lookup"><span data-stu-id="bad56-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="bad56-124">Yapılandırma, kullanıcının ilk oturum açmada Kullanıcı parolasını değiştirmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="bad56-125">Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bad56-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="bad56-126">Örnek 3: Linux tabanlı sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bad56-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="bad56-127">Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bad56-128">Geçerli cmdlet, Linux işletim sistemini çalıştıran bir sanal makine için sağlama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="bad56-129">Yapılandırma, kök kullanıcı adını ve parolasını içerir.</span><span class="sxs-lookup"><span data-stu-id="bad56-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="bad56-130">Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bad56-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="bad56-131">Örnek 4: WinRM için sertifikaları içeren bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bad56-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="bad56-132">İlk komut sertifika deposundaki sertifikaları alır ve bunları $certs dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bad56-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="bad56-133">İkinci komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bad56-134">Geçerli cmdlet, WinRM için sertifikaları içeren sağlama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="bad56-135">Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bad56-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="bad56-136">Örnek 5: HTTP üzerinden WinRM 'ye sahip bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bad56-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="bad56-137">Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bad56-138">Geçerli cmdlet, HTTP üzerinden WinRM 'ye sahip sağlama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="bad56-139">Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bad56-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="bad56-140">Örnek 6: WinRM HTTPS üzerinden devre dışı bırakılmış bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bad56-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="bad56-141">Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bad56-142">Geçerli cmdlet, HTTPS üzerinden WinRM 'yi devre dışı bırakan sağlama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="bad56-143">Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bad56-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="bad56-144">Örnek 7: anahtar dışarı aktarma olmadan sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bad56-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="bad56-145">İlk komut sertifika deposundaki sertifikaları alır ve bunları $certs dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bad56-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="bad56-146">İkinci komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bad56-147">Geçerli cmdlet, sertifikaları içeren ve özel anahtarları dışarı aktarmaz bir sanal makine için sağlama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bad56-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="bad56-148">Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bad56-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="bad56-149">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bad56-149">PARAMETERS</span></span>

### <span data-ttu-id="bad56-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="bad56-150">-AdminUsername</span></span>
<span data-ttu-id="bad56-151">Bu yapılandırmanın sanal makinede oluşturduğu yönetici hesabının kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-152">-Sertifikalar</span><span class="sxs-lookup"><span data-stu-id="bad56-152">-Certificates</span></span>
<span data-ttu-id="bad56-153">Bu yapılandırmanın sanal makinede yüklediği sertifika kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-154">-Customveri dosyası</span><span class="sxs-lookup"><span data-stu-id="bad56-154">-CustomDataFile</span></span>
<span data-ttu-id="bad56-155">Sanal makine için bir veri dosyası belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="bad56-156">Bu cmdlet, dosyanın içeriğini Base64 olarak kodlar.</span><span class="sxs-lookup"><span data-stu-id="bad56-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="bad56-157">Dosya 64 kilobayt uzunluğundan az olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bad56-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="bad56-158">Konuk işletim sistemi Windows işletim sistemdeydi, bu yapılandırma bu verileri%SYSTEMDRIVE%\AzureData\CustomData.bin. adlı bir ikili dosya olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bad56-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="bad56-159">Konuk işletim sistemi Linux ise, bu yapılandırma ovf-env.xml dosyasını kullanarak verileri geçirir.</span><span class="sxs-lookup"><span data-stu-id="bad56-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="bad56-160">Yapılandırma, dosyayı/var/lib/waagent dizinine kopyalar.</span><span class="sxs-lookup"><span data-stu-id="bad56-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="bad56-161">Aracı Ayrıca,/var/lib/waagent/customdata'de Base64 Ile kodlanmış verileri depolar.</span><span class="sxs-lookup"><span data-stu-id="bad56-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="bad56-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="bad56-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="bad56-163">Bu yapılandırmanın otomatik güncelleştirmeleri devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="bad56-164">-DisableGuestAgent</span></span>
<span data-ttu-id="bad56-165">Bu yapılandırmanın, altyapıyı bir hizmet (IaaS) Konuk Aracısı olarak devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="bad56-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="bad56-166">-DisableSSH</span></span>
<span data-ttu-id="bad56-167">Bu yapılandırmanın, SSH 'in devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="bad56-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="bad56-169">Bu yapılandırmanın HTTPS üzerinde Windows Uzaktan Yönetimi 'ni (WinRM) devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="bad56-170">Varsayılan olarak, HTTPS HTTPS üzerinden etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bad56-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-171">-Etki alanı</span><span class="sxs-lookup"><span data-stu-id="bad56-171">-Domain</span></span>
<span data-ttu-id="bad56-172">Bilgisayarı etki alanına ekleme izni olan hesabın etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="bad56-173">-DomainPassword</span></span>
<span data-ttu-id="bad56-174">Bilgisayarı etki alanına ekleme iznine sahip olan kullanıcı hesabının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="bad56-175">-DomainUserName</span></span>
<span data-ttu-id="bad56-176">Bilgisayarı etki alanına ekleme iznine sahip olan kullanıcı hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="bad56-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="bad56-178">Bu yapılandırmanın HTTP üzerinden WinRM 'yi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-179">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bad56-179">-InformationAction</span></span>
<span data-ttu-id="bad56-180">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bad56-181">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bad56-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bad56-182">'A</span><span class="sxs-lookup"><span data-stu-id="bad56-182">Continue</span></span>
- <span data-ttu-id="bad56-183">Manıza</span><span class="sxs-lookup"><span data-stu-id="bad56-183">Ignore</span></span>
- <span data-ttu-id="bad56-184">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="bad56-184">Inquire</span></span>
- <span data-ttu-id="bad56-185">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="bad56-185">SilentlyContinue</span></span>
- <span data-ttu-id="bad56-186">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="bad56-186">Stop</span></span>
- <span data-ttu-id="bad56-187">Biliriz</span><span class="sxs-lookup"><span data-stu-id="bad56-187">Suspend</span></span>

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

### <span data-ttu-id="bad56-188">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="bad56-188">-InformationVariable</span></span>
<span data-ttu-id="bad56-189">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bad56-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="bad56-190">-JoinDomain</span></span>
<span data-ttu-id="bad56-191">Katılacak etki alanının tam etki alanı adını (FQDN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="bad56-192">-Linux</span></span>
<span data-ttu-id="bad56-193">Bu yapılandırmanın bir Linux yapılandırması oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-193">Indicates that this configuration creates a Linux configuration.</span></span>

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

### <span data-ttu-id="bad56-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="bad56-194">-LinuxUser</span></span>
<span data-ttu-id="bad56-195">Bu yapılandırmanın sanal makinede oluşturduğu Linux yönetim hesabının kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

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

### <span data-ttu-id="bad56-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="bad56-196">-MachineObjectOU</span></span>
<span data-ttu-id="bad56-197">Yapılandırma bilgisayar hesabını oluştururken kuruluş biriminin (OU) tam nitelikli adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="bad56-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="bad56-199">Bu yapılandırmanın özel anahtarı yükleymediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="bad56-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="bad56-201">Bu yapılandırmanın uzak masaüstü uç noktası olmadan bir sanal makine oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="bad56-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="bad56-203">Bu yapılandırmanın, SSH uç noktası olmadan bir sanal makine oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="bad56-204">-NoSSHPassword</span></span>
<span data-ttu-id="bad56-205">Bu yapılandırmanın, SSH parolası olmadan bir sanal makine oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-206">-Nowinrmenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="bad56-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="bad56-207">Bu yapılandırmanın sanal makine için WinRM uç noktası eklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-208">-Parola</span><span class="sxs-lookup"><span data-stu-id="bad56-208">-Password</span></span>
<span data-ttu-id="bad56-209">Yönetici hesabının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-209">Specifies the password of the administrator account.</span></span>

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

### <span data-ttu-id="bad56-210">-Profil</span><span class="sxs-lookup"><span data-stu-id="bad56-210">-Profile</span></span>
<span data-ttu-id="bad56-211">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bad56-212">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bad56-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bad56-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="bad56-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="bad56-214">Sanal makinenin, kullanıcının ilk oturum açmada parolasını değiştirmesini gerektirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="bad56-215">-SSHKeyPairs</span></span>
<span data-ttu-id="bad56-216">SSH anahtar çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-216">Specifies SSH key pairs.</span></span>

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

### <span data-ttu-id="bad56-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="bad56-217">-SSHPublicKeys</span></span>
<span data-ttu-id="bad56-218">SSH ortak anahtarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-218">Specifies SSH public keys.</span></span>

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

### <span data-ttu-id="bad56-219">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="bad56-219">-TimeZone</span></span>
<span data-ttu-id="bad56-220">Sanal makinenin saat dilimini (örneğin, Pasifik standart saati veya Kanada Merkezi Standart Saati) belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-221">-VM</span><span class="sxs-lookup"><span data-stu-id="bad56-221">-VM</span></span>
<span data-ttu-id="bad56-222">Bir sanal makine nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="bad56-223">-Windows</span></span>
<span data-ttu-id="bad56-224">Bu yapılandırmanın, Windows işletim sistemini çalıştıran tek başına bir sanal makine oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

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

### <span data-ttu-id="bad56-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="bad56-225">-WindowsDomain</span></span>
<span data-ttu-id="bad56-226">Bu yapılandırmanın, Active Directory etki alanına bağlı Windows Server 'ı oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bad56-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-227">-Winrmcercertificate</span><span class="sxs-lookup"><span data-stu-id="bad56-227">-WinRMCertificate</span></span>
<span data-ttu-id="bad56-228">Bu yapılandırmanın WinRM uç noktasıyla ilişkilendiğinde bir sertifika belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="bad56-229">-X509Certificates</span></span>
<span data-ttu-id="bad56-230">Barındırılan bir hizmete dağıtılan x509 sertifikalarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad56-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad56-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad56-231">CommonParameters</span></span>
<span data-ttu-id="bad56-232">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bad56-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad56-233">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad56-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad56-234">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bad56-234">INPUTS</span></span>

## <span data-ttu-id="bad56-235">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bad56-235">OUTPUTS</span></span>

## <span data-ttu-id="bad56-236">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bad56-236">NOTES</span></span>

## <span data-ttu-id="bad56-237">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bad56-237">RELATED LINKS</span></span>

[<span data-ttu-id="bad56-238">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="bad56-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="bad56-239">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="bad56-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


